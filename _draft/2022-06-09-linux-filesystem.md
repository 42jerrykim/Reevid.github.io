---
title: "[Linux] File Systems 종류- DebugFS, SecurityFS, PipeFS, SockFS"
category: Linux
Tag:
- Linux
- FileSystem
- DebugFS
- SecurityFS
- PipeFS
- SockFS
header:
  teaser: 
---

리눅스에는 다양한 목적을 가지고 있는 가상 파일 시스템을 가지고 있다. DebugFS, SecurityFS, PipeFS, SockFS는 중요한 파일 시스템이다.

# DebugFS

DebugFS는 디버깅을 위해서 사용되며 램 기반에 파일 시스템이다. DebugFS는 ProcFS, SysFS와 비슷한 점이 많다. 그러나 디버그 정보를 표사한다는것이 다르다. 다른 램기반의 파일시스템처럼 DebugFS는 kernel-user interface이다. DebugFS는 터미널에 "mount -t debugfs none /sys/kernel/debug" 명령어를 통해서 마운트 할 수 있다.

만약에 시스템이 부팅될때 DebugFS가 마운트하려면 `/etc/fstab`에 `debugfs /sys/kernel/debug debugfs defaults 0 0`을 추가 한다.

When configuring the Linux kernel, the name of this feature (DebugFS) is called "CONFIG_DEBUG_FS". Enabling this enables DebugFS.

This filesystem has various system-calls as seen below

debugfs_create_atomic_t() creates a debugfs file for reading/writing an atomic_t value
debugfs_create_blob() creates a debugfs file for reading a binary-blob
debugfs_create_bool() creates a debugfs file for reading/writing a boolean value
debugfs_create_dir() creates a directory
debugfs_create_file() writes a file on the filesystem
debugfs_create_regset32() creates a debugfs file that returns register values
debugfs_create_size_t() creates a debugfs file for reading/writing a size_t value
debugfs_create_symlink() creates a symbolic link
debugfs_create_u{8,16,32,64}() creates a debugfs file for reading/writing an unsigned *-bit value
debugfs_create_u32_array() creates a debugfs file to read an unsigned 32-bit array
debugfs_create_x{8,16,32,64}() creates a debugfs file for reading/writing an unsigned *-bit value
debugfs_initialized() determines if debugfs is or is not registered
debugfs_print_regs32() use seq_print to describe a set of registers
debugfs_remove deletes() a file or directory from DebugFS
debugfs_remove_recursive() recursively removes a directory
debugfs_rename() renames a debugfs directory or file


SecurityFS

SecurityFS is a virtual filesystem in memory for security kernel modules. Kernel security modules place their policies and other data here. The user-space sees SecurityFS as a part of SysFS. SecurityFS is mounted on /sys/kernel/security/. Some of the security modules read and write files here that are used for configuring the security modules. The Linux Security Modules (LSM) will manually mount SecurityFS because the LSMs read/write data on this pseudo-filesystem, unless the filesystem is already mounted.

The LSMs make a folder on the root of SecurityFS with their name on it. For example, AppArmor would make a directory titled "apparmor" at /sys/kernel/security/.

|![](https://www.linux.org/attachments/securityfs-png.1299/)|
|:---:|
|이미지|



PipeFS

PipeFS is a unique virtual filesystem. This filesystem is mounted inside the kernel rather than in the userspace. While most filesystems are mounted under "/", PipeFS is mounted on "pipe:", making PipeFS its own root (yes, a second root filesystem). This filesystem is one superblock and cannot exceed that amount system-wide. The entry point of this filesystem/second-root is the system-call "pipe()". Unlike the other virtual/pseudo filesystems, this one cannot be viewed.

Many of you may be wondering what purpose this PipeFS filesystem serves. Unix pipes (simply called pipes) use this filesystem. When a pipe is used (like this - ls | less), the pipe() system-call makes a new pipe object on this filesystem. Without this filesystem, pipes cannot be made. Also, threads and forks communicate together via pipes. Without PipeFS, processes could not fork and threads could not communicate. Network pipes also rely on this virtual/pseudo filesystem.


SockFS

SockFS is a RAM-located pseudo-filesystem for storing information about the sockets/ports as well as a compatibility layer. SockFS is also called the Socket FileSystem. Now, as for SockFS being a compatibility layer, the write() system-call writes data to sockets/ports (the same ports like port-21 for FTP). Now, it is important to know that these sockets use the TCP or UDP network protocol and write() is the same system-call for writing files on the hard-disk. So, the question is "how is this possible?". The answer - SockFS. When write() writes data on SockFS, the filesystem makes changes to the data to make it suitable for the sockets. So, write() is not interacting directly with the sockets. Instead, the SockFS filesystem is acting as a mediator between the system-call and the sockets.


TIP: If you want a list of all of the mounted filesystems, both "real" and virtual, type - cat /proc/filesystems. The filesystems will be listed in the second column.

In Linux and Unix, everything is a file descriptor or a process. Now, you can probably see that better considering that networking and pipes require a filesystem.

# 원문

* [PipeFS, SockFS, DebugFS, and SecurityFS](https://www.linux.org/threads/pipefs-sockfs-debugfs-and-securityfs.9638/)