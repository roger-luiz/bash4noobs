## Movendo

```console
abantes@AB4NT5S:~/files$ ls
back-end  front-end  index.html  script.js  server.js  style.css
abantes@AB4NT5S:~/files$ mv index.html script.js style.css front-end/
abantes@AB4NT5S:~/files$ ls
back-end  front-end  server.js
abantes@AB4NT5S:~/files$ mv server.js back-end/
abantes@AB4NT5S:~/files$ ls
back-end  front-end
abantes@AB4NT5S:~/files$ ls front-end/
index.html  script.js  style.css
abantes@AB4NT5S:~/files$ ls back-end/
server.js
abantes@AB4NT5S:~/files$
```

## Renomeando

```console
abantes@AB4NT5S:~/files$ ls
back-end  front-end
abantes@AB4NT5S:~/files$ mv front-end/ public
abantes@AB4NT5S:~/files$ ls
back-end  public
abantes@AB4NT5S:~/files$ mv back-end/ src
abantes@AB4NT5S:~/files$ ls
public  src
abantes@AB4NT5S:~/files$
```