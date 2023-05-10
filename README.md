__apt__
```
apt-get update && apt-get install git curl wget zsh bird2 vim
```
__omzsh only (not recommended)__
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
__omzsh with plugin and theme__
```
curl -sSL https://github.com/BOJIN-NETWORK/omz/raw/main/install.sh | sudo -E bash -s ${USER:=`whoami`}
```
__nexttrace__
```
bash <(curl -Ls https://raw.githubusercontent.com/sjlleo/nexttrace/main/nt_install.sh)
```
__ip addr config__
`/etc/network/interfaces` or `/etc/network/interfaces.d/*`
```
auto lo
iface lo inet loopback
    dns-nameservers x.x.x.x

# default ipv4
auto <interface name>
iface <interface name> inet dhcp
    mtu 1500

# addtional ipv4
auto <interface name>:0
iface <interface name>:0 inet static
    address x.x.x.x
    netmask 255.255.255.255

iface <interface name> inet6 static
    address x:x:x.x::x
    netmask 64
    gateway x:x:x:x::x
```