---
name: فرم گزارش آزمایش سوم
about: برای نوشتن گزارش آزمایشگاه از این تمپلیت استفاده کنید
title: Session 3 Report
labels: documentation
assignees: fshahinfar1

---

Team Name: `[FILL HERE]`

Student Name of member 1: `[FILL HERE]`
Student No. of member 1: `[FILL HERE]`

Student Name of member 2: `[FILL HERE]`
Student No. of member 2: `[FILL HERE]`

- [ ] Read Session Contents.

### Section 3.3.1
- [ ] Investigate the /proc/ directory
    1. ![Capture1](https://user-images.githubusercontent.com/45646480/128890997-a4a6e2fb-e598-48f6-82c2-7b2231929f75.JPG)

### Section 3.3.2

- [ ] Do 5 subtasks from 1 to 5:
    1. ![Capture0](https://user-images.githubusercontent.com/45646480/128891653-e459005e-3df1-41ee-8e4c-720eba7cd88e.JPG)
    1. ![Capture2](https://user-images.githubusercontent.com/45646480/128891071-2ca1a814-e3b6-42e7-b532-0db899eac1e0.JPG)
    1. ![Capture3](https://user-images.githubusercontent.com/45646480/128891358-1e881e7b-bbb7-4f55-9e3d-4d2d2ac60977.JPG)
    1. ![Capture5](https://user-images.githubusercontent.com/45646480/128891792-ed7f6c40-0695-4883-ac19-98574fd31d96.JPG)
    1. ![Capture4](https://user-images.githubusercontent.com/45646480/128891500-cdbd24c9-e862-4d45-94c0-7b35421152c2.JPG)

## Section 3.3.3

- [ ] Write (in English or Persian) about each file in /proc/(PID) directory:
    1. `[FILL HERE with description about cmdline]` This  read-only  file holds the complete command line for the process, unless the process is a zombie.  In the latter case, there is nothing in this file: that is, a read on this file will return 0 characters.  The command-line arguments appear in this file as a set of strings separated by null bytes ('\0'), with a further null byte  after the last string.
    1. `[FILL HERE with description about environ]` This file contains the initial environment that was set when the currently executing program was started via execve.The entries are separated by null  bytes  ('\0'), and there may be a null byte at the end.
    1. `[FILL HERE with description about stat]` Status information about the process lile pid, ppid, state, ... . This is used by ps.
    1. `[FILL HERE with description about status]` Provides much of the information in /proc/[pid]/stat and /proc/[pid]/statm in a format that's easier for humans to parse like PID, PPID, THREADS, STATE, ... .
    1. `[FILL HERE with description about statm]` Provides information about memory usage, measured in pages such as size, resident, shared, ... .
    1. `[FILL HERE with description about cwd]` This is a symbolic link to the current working directory of the process.  To find out the current working directory of process 20, for instance, you can do this:
     $ cd /proc/20/cwd; /bin/pwd
    1. `[FILL HERE with description about exe]` Under Linux 2.2 and later, this file is a symbolic link containing the actual pathname of the executed command.  This symbolic link can be dereferenced normally; attempting  to  open it will open the executable.  You can even type /proc/[pid]/exe to run another copy of the same executable that is being run by process [pid]. 
    1. `[FILL HERE with description about root]` UNIX and Linux support the idea of a per-process root of the filesystem, set by the chroot(2) system call.  This file is a symbolic link that points to the process's root directory, and behaves in the same way as exe, and fd/*.

- [ ] Place your script for shwoing PID of running porcesses and their name here:
    - ![Capture6](https://user-images.githubusercontent.com/45646480/128892249-27b35c9f-777a-47eb-9166-2be6abe764d8.JPG)

- [ ] Place your source code for a program that shows details of a program by receiving PID:
    - [ ] `[FILL HERE with you source code]`

### Section 3.3.4

- [ ] Write (in English or Persian) about each file in /proc/ directory:
    1. `[FILL HERE with description about meminfo]` This is one of the more commonly used files in the /proc/ directory, as it reports a large amount of valuable information about the system's RAM usage.
    1. `[FILL HERE with description about version]` This file specifies the version of the Linux kernel, the version of gcc used to compile the kernel, and the time of kernel compilation. It also contains the kernel compiler's user name (in parentheses).
    1. `[FILL HERE with description about uptime]` This file contains information detailing how long the system has been on since its last restart. The output of /proc/uptime is quite minimal:
350735.47 234388.90
    1. `[FILL HERE with description about stat]` This file keeps track of a variety of different statistics about the system since it was last restarted. The contents of /proc/stat, which can be quite long.
    1. `[FILL HERE with description about mount]` This file provides a list of all mounts in use by the system. The first column specifies the device that is mounted, the second column reveals the mount point, and the third column tells the file system type, and the fourth column tells you if it is mounted read-only (ro) or read-write (rw). The fifth and sixth columns are dummy values designed to match the format used in /etc/mtab.
    1. `[FILL HERE with description about net directory (or file)]` This directory provides a comprehensive look at various networking parameters and statistics. Each directory and virtual file within this directory describes aspects of the system's network configuration.
    1. `[FILL HERE with description about loadavg]` This file provides a look at the load average in regard to both the CPU and IO over time, as well as additional data used by uptime and other commands.
    1. `[FILL HERE with description about interrupts]` This file records the number of interrupts per IRQ on the x86 architecture.
    1. `[FILL HERE with description about ioports]` The output of /proc/ioports provides a list of currently registered port regions used for input or output communication with a device. This file can be quite long. 
    1. `[FILL HERE with description about filesystem]` This file displays a list of the file system types currently supported by the kernel.
The first column signifies whether the file system is mounted on a block device. Those beginning with nodev are not mounted on a device. The second column lists the names of the file systems supported.
    1. `[FILL HERE with description about cpuinfo]` This virtual file identifies the type of processor used by your system. have informations like processor, cpu family,model name, cpu MHz and ... .
    1. `[FILL HERE with description about cmdline]` This file shows the parameters passed to the kernel at the time it is started. A sample /proc/cmdline file looks like the following:
ro root=/dev/VolGroup00/LogVol00 rhgb quiet 3

- [ ] pictures:

![proc1](https://user-images.githubusercontent.com/45646480/128893002-c4b009ed-ffea-4df9-a133-6abc7c11ff2d.JPG)


![proc2](https://user-images.githubusercontent.com/45646480/128893025-dadb6ee4-c9bf-4f07-8164-48654de6fb4f.JPG)


![proc3](https://user-images.githubusercontent.com/45646480/128893043-a228811e-8bde-4772-ae24-97b8e6c4625b.JPG)


![proc4](https://user-images.githubusercontent.com/45646480/128893051-497df07b-3d2b-4309-b91d-343aa343b98c.JPG)


![proc5](https://user-images.githubusercontent.com/45646480/128893057-9f2883ad-9876-41ef-984e-457108189434.JPG)


- [ ] Place your source code for a program that shows details of processor:
    - [ ] `[FILL HERE with you source code]`

- [ ] Place your source code for a program that shows details of memory management sub-system:
    - [ ] `[FILL HERE with you source code]`

- [ ] Write your description about five important files at /proc/sys/kernel:
    - [ ] `[FILL HERE with you descript for 1st file]`
    - [ ] `[FILL HERE with you descript for 2nd file]`
    - [ ] `[FILL HERE with you descript for 3rd file]`
    - [ ] `[FILL HERE with you descript for 4th file]`
    - [ ] `[FILL HERE with you descript for 5th file]`

- [ ] Write your description about /proc/self file
    - [ ] `[FILL HERE with you description]`


## Source Code Submission

please submit all your codes in a zip file

 - [ ] `Zip File HERE`
