# playShadowsocks

### install shadowsockX on OSX

  [ShadowsocksX-NG](https://github.com/shadowsocks/ShadowsocksX-NG/releases) or 
  ```
  $ brew cask install shadowsocksx
  ```
  
### install the client on windows
  
  [shadowsocks-windows](https://github.com/shadowsocks/shadowsocks-windows)

### Get shadowsocks container
  - [oddrationale](https://hub.docker.com/r/oddrationale/docker-shadowsocks/)
  - [mrjin](https://hub.docker.com/r/mrjin/shadowsocks/)
  - [tommylau](https://hub.docker.com/r/tommylau/shadowsocks/)
  - [go-shadowsocks2](https://hub.docker.com/r/justcy/go-shadowsocks2)
### Used on Google Cloud with BBR in Ubuntu 16.04.4 LTS (GNU/Linux 4.13.0-1019-gcp x86_64)
```
wget –no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh
chmod +x bbr.sh
sudo ./bbr.sh
sudo -i
reboot
sysctl net.ipv4.tcp_available_congestion_control
sudo apt-get install python-pip -y
sudo pip install shadowsocks
sudo vi /etc/ss-conf.json
```
```
{
"server":"0.0.0.0",
"server_port":8888,
"local_address":"127.0.0.1",
"local_port":1080,
"password":"phu021",
"timeout":600,
"method":"aes-256-cfb"
}
```
```
sudo ssserver -c /etc/ss-conf.json -d start

