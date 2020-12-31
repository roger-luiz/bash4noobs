## ps

```console
abantes@AB4NT5S:~$ ps
  PID TTY          TIME CMD
    7 tty1     00:00:04 bash
  291 tty1     00:00:00 ps
abantes@AB4NT5S:~$
```

```console
abantes@AB4NT5S:~$ ps -A
  PID TTY          TIME CMD
    1 ?        00:00:00 init
    6 tty1     00:00:00 init
    7 tty1     00:00:04 bash
  297 tty1     00:00:00 ps
abantes@AB4NT5S:~$
```

## top

```console
top - 12:42:10 up  1:47,  0 users,  load average: 0.52, 0.58, 0.59
Tasks:   4 total,   1 running,   3 sleeping,   0 stopped,   0 zombie
%Cpu(s): 14.2 us, 82.7 sy,  0.0 ni,  1.0 id,  0.0 wa,  2.1 hi,  0.0 si,  0.0 st
KiB Mem :  1946152 total,   398572 free,  1318228 used,   229352 buff/cache
KiB Swap:  6029312 total,  5765304 free,   264008 used.   494192 avail Mem

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU %MEM     TIME+ COMMAND
    1 root      20   0    8936    156    112 S   0.0  0.0   0:00.21 init
    6 root      20   0    8936    132     88 S   0.0  0.0   0:00.00 init
    7 abantes   20   0   17180   2544   2436 S   0.0  0.1   0:04.46 bash
  295 abantes   20   0   17632   2040   1512 R   0.0  0.1   0:00.07 top
```