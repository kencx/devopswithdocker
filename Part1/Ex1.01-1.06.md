### 1.01
```
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS                          PORTS     NAMES
5492b7e840ef   ubuntu:18.04   "bash"                   About a minute ago   Exited (0) About a minute ago             stoic_hamilton
4509ecf3ba22   ubuntu         "bash"                   2 minutes ago        Exited (0) 2 minutes ago                  gallant_aryabhata
1ad21e7c3032   nginx          "/docker-entrypoint.…"   3 minutes ago        Up 3 minutes                    80/tcp    sleepy_yalow
31bdbc8f6286   nginx          "/docker-entrypoint.…"   4 minutes ago        Exited (0) 3 minutes ago                  tender_mayer
```

### 1.02
```
docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

docker images
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
```

### 1.03
Secret message is: 'You can find the source code here: https://github.com/docker-hy'

### 1.04
```
docker run -d -it --name read-website ubuntu sh -c 'echo "Input website:"; read website; echo
"Searching..."; sleep 1; curl http://$website;'
```

To install curl, we first enter the container with an interactive terminal
```
docker exec -it read-website bash
```
Install curl with ubuntu's apt-get
```
apt-get update && apt-get install curl
```
Exit the container with Ctrl+p, Ctrl+q and re-attach to the container with
```
docker attach read-website

Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
```

### 1.05
```
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   8 months ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   8 months ago   15.7MB
```

Launch alpine container and attach with
```
docker run -it -d devopsdockeruh/simple-web-service:alpine --name alpine
docker exec -it alpine sh
```

Secret message is: 'You can find the source code here: https://github.com/docker-hy'

### 1.06
```
docker run -it devopsdockeruh/pull_exercise
Give me the password: basics
You found the correct password. Secret message is:
"This is the secret message"
```
