# playShadowsocks

### install shadowsockX on OSX
  
  ```
  $ brew cask install shadowsocksx
  ```
  
### install the client on windows
  
  [shadowsocks-windows](https://github.com/shadowsocks/shadowsocks-windows)

### Get shadowsocks container
  - [oddrationale](https://hub.docker.com/r/oddrationale/docker-shadowsocks/)
  - [mrjin](https://hub.docker.com/r/mrjin/shadowsocks/)
  - [tommylau](https://hub.docker.com/r/tommylau/shadowsocks/)
### Used on Google Cloud with BBR
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
“server”:”0.0.0.0”,
“server_port”:8888,
“local_address”:”127.0.0.1”,
“local_port”:1080,
“password”:”XXXXX”,
“timeout”:600,
“method”:”aes-256-cfb”
}
```
```
sudo ssserver -c /etc/ss-conf.json -d start

