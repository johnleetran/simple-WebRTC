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
-open https://127.0.0.1:8080/index-caller.html
-press cal button
-copy the id that shows up
-open https://127.0.0.1:8080/index-answer.html
-paste in id that was copy from previous step
-click on the call button
-allow permissions
-go back to the index-caller.html tab
-allow permissions

```
