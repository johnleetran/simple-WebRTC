Need PeerJs server - https://github.com/peers/peerjs.  Very usefull to use https://www.gitpod.io/ to host the peerjs server temp.


Generate ssl certs
```
mkdir ssl
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout privateKey.key -out certificate.crt
```

Start http-server
```
npm intall -g http-server
http-server -S -C ssl/certificate.crt -K ssl/privateKey.key 
```

Usage
```
-open index-caller.html to point to peerjs server
-open index-answer.tml to point to peerjs server
-open browser to https://127.0.0.1:8080/index-caller.html
-press cal button
-copy the id that shows up
-open browser to https://127.0.0.1:8080/index-answer.html
-paste in id that was copy from previous step
-click on the call button
-allow permissions
-go back to the index-caller.html tab
-allow permissions

```

