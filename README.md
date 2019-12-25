# ss
shadowsocks

### installShadowsocks.sh
```
#!/bin/bash

yum install -y python-setuptools &&
easy_install pip &&
yum install -y git &&
pip install git+https://github.com/shadowsocks/shadowsocks.git@master &&

ssserver -c /etc/shadowsocks.json -d start
```

### /etc/shadowsocks.json
```
{
    "server":"0.0.0.0",
    "server_port":8383,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"2xGk47T3",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}
```
