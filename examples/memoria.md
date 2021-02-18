```console
roger@roger:~$ free
              total        used        free      shared  buff/cache   available
Mem:        1946152     1317364      399436       17720      229352      495056
Swap:       6029312      257668     5771644
roger@roger:~$
```

```console
roger@roger:~$ df
Filesystem     1K-blocks     Used Available Use% Mounted on
rootfs         487261824 28959972 458301852   6% /
none           487261824 28959972 458301852   6% /dev
none           487261824 28959972 458301852   6% /run
none           487261824 28959972 458301852   6% /run/lock
none           487261824 28959972 458301852   6% /run/shm
none           487261824 28959972 458301852   6% /run/user
tmpfs          487261824 28959972 458301852   6% /sys/fs/cgroup
C:\            487261824 28959972 458301852   6% /mnt/c
roger@roger:~$
```

```console
roger@roger:~$ df -m
Filesystem     1M-blocks  Used Available Use% Mounted on
rootfs            475842 28282    447560   6% /
none              475842 28282    447560   6% /dev
none              475842 28282    447560   6% /run
none              475842 28282    447560   6% /run/lock
none              475842 28282    447560   6% /run/shm
none              475842 28282    447560   6% /run/user
tmpfs             475842 28282    447560   6% /sys/fs/cgroup
C:\               475842 28282    447560   6% /mnt/c
roger@roger:~$
```