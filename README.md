# How to run Docker 17.11 CE on Raspberry Pi 3

- Logging in into Raspbian OS with user "pi" and password "raspbian" by default

```
pi@192.168.1.3's password:
Linux raspberrypi 4.9.41-v7+ #1023 SMP Tue Aug 8 16:00:15 BST 2017 armv7l

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Thu Dec  7 04:12:11 2017

SSH is enabled and the default password for the 'pi' user has not been changed.
This is a security risk - please login as the 'pi' user and type 'passwd' to set a new password.

```

```
root@raspberrypi:/home/pi# docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                NAMES
ee0bc4d29e44        nginx               "nginx -g 'daemon of…"   30 seconds ago      Up 28 seconds       0.0.0.0:80->80/tcp   mystifying_bhaskara
root@raspberrypi:/home/pi# docker logs -f ee0
^C
root@raspberrypi:/home/pi# curl localhost:80
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
    body {
        width: 35em;
        margin: 0 auto;
        font-family: Tahoma, Verdana, Arial, sans-serif;
    }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
root@raspberrypi:/home/pi# cat /etc/issue
Raspbian GNU/Linux 9 \n \l
root@raspberrypi:/home/pi# ^C
root@raspberrypi:/home/pi#
```
