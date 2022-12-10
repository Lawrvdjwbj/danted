# Sockd
**Dante socks5 server (v1.3.2/v1.4.2) auto-install and management script** 

## Install by Script

```bash
wget --no-check-certificate https://raw.github.com/Lawrvdjwbj/danted/master/install.sh -O install.sh 
bash install.sh

# run with options: bash install.sh option1 option2
bash install.sh --ip="A.A.A.A:B.B.B.B" --port=2022 --user=sockd --passwd=sockd --whitelist="X.X.X.X/32"

```

* *if you want to uninstall, using this command*

```bash
bash install.sh --uninstall
```

* *if you want to add user*

```bash
/etc/init.d/sockd adduser USERNAME PASSWORD
```

## Options

| Long Option | Short Option | Value refer | description |
| :--- | :--- | --- | --- |
| --ip=                | | ip address list (a.a.a.a:b.b.b.b) *#change ';' to ':' * | Socks5 Server Ip address |
| --port=             | | Default: 2016| port for dante socks5 server |
| --version=          | | Default: 1.3.2 | dante server version, latest is 1.4.2 |
| --user=              | | Pam-Auth Username | Socks5 Auth user |
| --passwd=            | | Pam-Auth Password |Socks5 Auth passwd |
| --whitelist=         | | whitelist ip range (a.a.a.a/32:b.b.b.b/32) |Socks5 Auth IP list |
| --whitelist-url=     | | online white list file (url) | Socks Auth whitelist http online |
| --from-package       | -p    | --    | Install package from Bin package |
| --update-whitelist   | -u    | --    |  update white list |
| --force              | -f    | --    | force install sockd |
| --help               | -h    | --    | print help info |

## Management

| command | option | description |
| :--- | :--- | --- |
| service sockd start | /etc/init.d/sockd start | start socks5 server daemon |
| service sockd stop | /etc/init.d/sockd stop | stop socks5 server daemon |
| service sockd restart | /etc/init.d/sockd restart | restart socks5 server daemon |
| service sockd reload | /etc/init.d/sockd reload | reload socks5 server daemon |
| service sockd status | | systemd process status |
| service sockd state | /etc/init.d/sockd state | running state |
| service sockd tail | /etc/init.d/sockd tail | sock log tail |
| service sockd adduser | /etc/init.d/sockd adduser | add pam-auth user:  service sockd adduser NAME PASSWORD |
| service sockd deluser | /etc/init.d/sockd deluser | delete pam-auth user:  service sockd deluser NAME |


## Test Pass

| OS release | Platform | Provider | Result |
| :--- | :--- | --- |  --- | 
| Debian GNU/Linux 8 (jessie) | x86_64 | vultr | pass |
| Debian GNU/Linux 7 (wheezy) | x86_64 | vultr | pass |
| Debian GNU/Linux 7 (wheezy) | i686 | vultr | pass |
| Ubuntu 16.10 (Yakkety Yak)  | x86_64 | vultr | pass |
| Ubuntu 14.04.5 LTS | i686 | vultr | pass
| CentOS Linux 7 (Core) | x86_64 | vultr | pass |
| CentOS Linux 6 | x86_64 | vultr | pass |
| CentOS Linux 6 | i686 | vultr | pass |
