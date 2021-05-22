```console
roger@roger:~$ mkdir images
roger@roger:~$ ls
images
roger@roger:~$
```

```console
roger@roger:~$ mkdir images videos songs
roger@roger:~$ ls
images  songs  videos
roger@roger:~$
```

```console
roger@roger:~$ mkdir -p backup/images/png
roger@roger:~$ ls
backup
roger@roger:~$ cd backup/
roger@roger:~/backup$ ls
images
roger@roger:~/backup$ cd images/
roger@roger:~/backup/images$ ls
png
roger@roger:~/backup/images$ cd png/
roger@roger:~/backup/images/png$ pwd
/home/abantes/backup/images/png
roger@roger:~/backup/images/png$
```