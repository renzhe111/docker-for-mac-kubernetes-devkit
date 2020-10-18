docker-compose.yml中地22行
command: TCP-LISTEN:1194,fork TCP:172.32.0.1:31194
改为：
command: TCP-LISTEN:1194,fork TCP:172.19.0.1:31194
因为我们目标docker容器集群的网段是172.19.0
生成的docker-for-mac.ovpn文件最后加入
route 172.19.0.0 255.255.255.0
