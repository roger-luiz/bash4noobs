## .tar

Compressão:

```console
abantes@AB4NT5S:~/files$ ls
keylogger.cpp  payload.py  script.js
abantes@AB4NT5S:~/files$ tar cf container.tar script.js payload.py keylogger.cpp
abantes@AB4NT5S:~/files$ ls
container.tar  keylogger.cpp  payload.py  script.js
abantes@AB4NT5S:~/files$
```
Extração:

```console
abantes@AB4NT5S:~/files$ ls
container.tar
abantes@AB4NT5S:~/files$ tar xf container.tar
abantes@AB4NT5S:~/files$ ls
container.tar  keylogger.cpp  payload.py  script.js
abantes@AB4NT5S:~/files$
```

## .tar.gz

Compressão:

```console
abantes@AB4NT5S:~/files$ ls -F
images-jpg/  images-png/  images-svg/
abantes@AB4NT5S:~/files$ tar czf images.tar.gz images-jpg/ images-png/ images-svg/
abantes@AB4NT5S:~/files$ ls
images-jpg  images-png  images-svg  images.tar.gz
abantes@AB4NT5S:~/files$
```

Extração:

```console
abantes@AB4NT5S:~/files$ ls
images.tar.gz
abantes@AB4NT5S:~/files$ tar xzf images.tar.gz
abantes@AB4NT5S:~/files$ ls -F
images-jpg/  images-png/  images-svg/  images.tar.gz
abantes@AB4NT5S:~/files$
```

## .tar.bz2

Compressão

```console
abantes@AB4NT5S:~/files$ ls
flappy-bird
abantes@AB4NT5S:~/files$ ls flappy-bird/
LICENSE.md  README.md  package.json  public  src
abantes@AB4NT5S:~/files$ tar cjf project.tar.bz2 flappy-bird/
abantes@AB4NT5S:~/files$ ls
flappy-bird  project.tar.bz2
abantes@AB4NT5S:~/files$
```

Extração

```console
abantes@AB4NT5S:~/files$ ls
project.tar.bz2
abantes@AB4NT5S:~/files$ tar xjf project.tar.bz2
abantes@AB4NT5S:~/files$ ls
flappy-bird  project.tar.bz2
abantes@AB4NT5S:~/files$
```

## .gz

Compressão

```console
abantes@AB4NT5S:~/files$ ls
exploit.py  trojan.cpp
abantes@AB4NT5S:~/files$ gzip exploit.py trojan.cpp
abantes@AB4NT5S:~/files$ ls
exploit.py.gz  trojan.cpp.gz
abantes@AB4NT5S:~/files$
```

Extração

```console
abantes@AB4NT5S:~/files$ ls
exploit.py.gz  trojan.cpp.gz
abantes@AB4NT5S:~/files$ gzip -d exploit.py trojan.cpp
abantes@AB4NT5S:~/files$ ls
exploit.py  trojan.cpp
abantes@AB4NT5S:~/files$
```