# ESX_Serial

```
Serial Port 1: Use network

Status: Connect at power on

Connection: Direction: Server
            Port URI: telnet://vSPC.py:13370
            [x] Use Virtual Serial Port Concentrator
            vSPC URI: telnet://192.168.199.30:13370
```

```
./vSPCClient smartproxyrh1-imp
...here is the text from remote…
<Ctrl+]>
vspc> close
quit:         exit the client
continue:     exit this menu
print-escape: send the escape sequence to the VM
vspc> quit
```

The WUI is not able to parse vSPC.py rather it requires URL (telnet://vSPC.py:13370), has to be fixed in the library lib/telnet.py

```
BASENAMEX = 'telnet://vSPC.py:13370' - string matching
```

[https://github.com/shaozi/vSPC.py](https://github.com/shaozi/vSPC.py)
