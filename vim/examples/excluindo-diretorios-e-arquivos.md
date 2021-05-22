```console
roger@roger:~/files$ ls
docs  keylogger.cpp  payload.py  script.js
roger@roger:~/files$ rm keylogger.cpp
roger@roger:~/files$ ls
docs  payload.py  script.js
roger@roger:~/files$
```

```console
roger@roger:~/files$ ls
docs  payload.py  script.js
roger@roger:~/files$ rm -d docs/
roger@roger:~/files$ ls
payload.py  script.js
roger@roger:~/files$
```

```console
roger@roger:~/files$ ls
docs  image  keylloger.cpp  payload.py  script.js  web-docs
roger@roger:~/files$ rm -rf *
roger@roger:~/files$ ls
roger@roger:~/files$
```