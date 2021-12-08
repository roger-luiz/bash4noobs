## .tar

Compressão:

```console
roger@roger:~/files$ ls
keylogger.cpp  payload.py  script.js
roger@roger:~/files$ tar cf container.tar script.js payload.py keylogger.cpp
roger@roger:~/files$ ls
container.tar  keylogger.cpp  payload.py  script.js
roger@roger:~/files$
```
Extração:

```console
roger@roger:~/files$ ls
container.tar
roger@roger:~/files$ tar xf container.tar
roger@roger:~/files$ ls
container.tar  keylogger.cpp  payload.py  script.js
roger@roger:~/files$
```

## .tar.gz

Compressão:

```console
roger@roger:~/files$ ls -F
images-jpg/  images-png/  images-svg/
roger@roger:~/files$ tar czf images.tar.gz images-jpg/ images-png/ images-svg/
roger@roger:~/files$ ls
images-jpg  images-png  images-svg  images.tar.gz
roger@roger:~/files$
```

Extração:

```console
roger@roger:~/files$ ls
images.tar.gz
roger@roger:~/files$ tar xzf images.tar.gz
roger@roger:~/files$ ls -F
images-jpg/  images-png/  images-svg/  images.tar.gz
roger@roger:~/files$
```

## .tar.bz2

Compressão

```console
roger@roger:~/files$ ls
flappy-bird
roger@roger:~/files$ ls flappy-bird/
LICENSE.md  README.md  package.json  public  src
roger@roger:~/files$ tar cjf project.tar.bz2 flappy-bird/
roger@roger:~/files$ ls
flappy-bird  project.tar.bz2
roger@roger:~/files$
```

Extração

```console
roger@roger:~/files$ ls
project.tar.bz2
roger@roger:~/files$ tar xjf project.tar.bz2
roger@roger:~/files$ ls
flappy-bird  project.tar.bz2
roger@roger:~/files$
```

## .gz

Compressão

```console
roger@roger:~/files$ ls
exploit.py  trojan.cpp
roger@roger:~/files$ gzip exploit.py trojan.cpp
roger@roger:~/files$ ls
exploit.py.gz  trojan.cpp.gz
roger@roger:~/files$
```

Extração

```console
roger@roger:~/files$ ls
exploit.py.gz  trojan.cpp.gz
roger@roger:~/files$ gzip -d exploit.py trojan.cpp
roger@roger:~/files$ ls
exploit.py  trojan.cpp
roger@roger:~/files$
```