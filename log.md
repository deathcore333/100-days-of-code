# 100 Days Of Code - Log

## Day 0: October 12, 2022

Create the simplest web server using python.

**Today's Progress**:

use python to build the most simple version of a web server.
Running in a docker python alpine container exposing network to host, run the server and acces it from the host using curl.

```bash
$ docker run -d --rm -it --name py-dj-0 -v ~/code:/code --network=host py-dj

$ docker exec -it py-dj-0 sh

/ # cd code/Django/simple_server_browser/
/code/Django/simple_server_browser # ./02-simplest_server.py
Access http://localhost:80
GET http://127.0.0.1 HTTP/1.0
GET / HTTP/1.1
GET / HTTP/1.1
```

- from other shell in the host

```bash
$ curl -v localhost
*   Trying 127.0.0.1:80...
* Connected to localhost (127.0.0.1) port 80 (#0)
> GET / HTTP/1.1
> Host: localhost
> User-Agent: curl/7.85.0
> Accept: */*
>
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Content-Type: text/html; charset=utf-8
* no chunk, no close, no size. Assume close to signal end
<
<html><body>Hello World!!</body></html>

* Closing connection 0
```

**Thoughts:**


**Link to work:**
-[simplest server](https://github.com/ralexrivero/python/blob/e54bf84cc66a8d7a0bffe791fb673d728e66c445/1x01-simple_server_browser/02-simplest_server.py)
