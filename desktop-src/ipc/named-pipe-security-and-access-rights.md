---
Description: 'You can specify a security descriptor for a named pipe when you call the CreateNamedPipe function. The security descriptor controls access to both client and server ends of the named pipe.'
ms.assetid: 'f9ea97c9-9a97-4083-82d8-29ffb8be5a77'
title: Named Pipe Security and Access Rights
---

# Named Pipe Security and Access Rights

Windows security enables you to control access to named pipes. For more information about security, see [Access-Control Model](https://msdn.microsoft.com/library/windows/desktop/aa374876).

You can specify a [security descriptor](https://msdn.microsoft.com/library/windows/desktop/aa379563) for a named pipe when you call the [**CreateNamedPipe**](createnamedpipe.md) function. The security descriptor controls access to both client and server ends of the named pipe. If you specify **NULL**, the named pipe gets a default security descriptor. The ACLs in the default security descriptor for a named pipe grant full control to the LocalSystem account, administrators, and the creator owner. They also grant read access to members of the Everyone group and the anonymous account.

To retrieve a named pipe's security descriptor, call the [**GetSecurityInfo**](https://msdn.microsoft.com/library/windows/desktop/aa446654) function. To change the security descriptor of a named pipe, call the [**SetSecurityInfo**](https://msdn.microsoft.com/library/windows/desktop/aa379588) function.

When a thread calls [**CreateNamedPipe**](createnamedpipe.md) to open a handle to the server end of an existing named pipe, the system performs an access check before returning the handle. The access check compares the thread's access token and the requested [access rights](https://msdn.microsoft.com/library/windows/desktop/aa374902) against the DACL in the named pipe's security descriptor. In addition to the requested access rights, the DACL must allow the calling thread FILE\_CREATE\_PIPE\_INSTANCE access to the named pipe.

Similarly, when a client calls the [**CreateFile**](https://msdn.microsoft.com/library/windows/desktop/aa363858) or [**CallNamedPipe**](callnamedpipe.md) function to connect to the client end of a named pipe, the system performs an access check before granting access to the client.

The handle returned by the [**CreateNamedPipe**](createnamedpipe.md) function always has SYNCHRONIZE access. It also has GENERIC\_READ, GENERIC\_WRITE, or both, depending on the open mode of the pipe. The following are the access rights for each open mode.



| Open mode                           | Access rights                                              |
|-------------------------------------|------------------------------------------------------------|
| PIPE\_ACCESS\_DUPLEX (0x00000003)   | FILE\_GENERIC\_READ, FILE\_GENERIC\_WRITE, and SYNCHRONIZE |
| PIPE\_ACCESS\_INBOUND (0x00000001)  | FILE\_GENERIC\_READ and SYNCHRONIZE                        |
| PIPE\_ACCESS\_OUTBOUND (0x00000002) | FILE\_GENERIC\_WRITE and SYNCHRONIZE                       |



 

FILE\_GENERIC\_READ access for a named pipe combines the rights to read data from the pipe, read pipe attributes, read extended attributes, and read the pipe's DACL.

FILE\_GENERIC\_WRITE access for a named pipe combines the rights to write data to the pipe, append data to it, write pipe attributes, write extended attributes, and read the pipe's DACL. Because FILE\_APPEND\_DATA and FILE\_CREATE\_PIPE\_INSTANCE have the same definition, so FILE\_GENERIC\_WRITE enables permission to create the pipe. To avoid this problem, use the individual rights instead of using FILE\_GENERIC\_WRITE.

You can request the ACCESS\_SYSTEM\_SECURITY access right to a named pipe object if you want to read or write the object's SACL. For more information, see [Access-Control Lists (ACLs)](https://msdn.microsoft.com/library/windows/desktop/aa374872) and [SACL Access Right](https://msdn.microsoft.com/library/windows/desktop/aa379321).

To prevent remote users or users on a different terminal services session from accessing a named pipe, use the logon SID on the DACL for the pipe. The logon SID is used in run-as logons as well; it is the SID used to protect the per-session object namespace. For more information, see [Getting the Logon SID in C++](https://msdn.microsoft.com/library/windows/desktop/aa446670).

 

 


