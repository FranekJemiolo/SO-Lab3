Read-write semaphore implementation.
There are a few files included in patch
rwsem.c - in ipc server files
rwsem.c - in libc/sys-minix
rwsem.h - header
build_rwsem.sh - script that builds and reboots libraries
And few modified files:
ipc.h
inc.h
com.h
main.c
unistd.h
Makefile - in ipc/server
Makefile.inc

They are modified so our library will be open to users - they include some
declarations of methods and such.

Unfortunately I didn't had the time to fully complete the assignment -
there is something wrong with getting more than MAX_RWSEM rw-semaphores
- I think it is something wrong with removal (rwsemdel). So sorry about that.
I hope the rest works.

Oh and you will propably need to include rwsem.h in /usr/include/minix
and com.h also there plus unistd.h. The script does not do it because of .git
which is placed in /usr/src .
