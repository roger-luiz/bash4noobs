## Movendo

```console
roger@roger:~/files$ ls
back-end  front-end  index.html  script.js  server.js  style.css
roger@roger:~/files$ mv index.html script.js style.css front-end/
roger@roger:~/files$ ls
back-end  front-end  server.js
roger@roger:~/files$ mv server.js back-end/
roger@roger:~/files$ ls
back-end  front-end
roger@roger:~/files$ ls front-end/
index.html  script.js  style.css
roger@roger:~/files$ ls back-end/
server.js
roger@roger:~/files$
```

## Renomeando

```console
roger@roger:~/files$ ls
back-end  front-end
roger@roger:~/files$ mv front-end/ public
roger@roger:~/files$ ls
back-end  public
roger@roger:~/files$ mv back-end/ src
roger@roger:~/files$ ls
public  src
roger@roger:~/files$
```