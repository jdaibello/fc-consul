# Commands

## Run consul server

1. `ifconfig` -> eth0 inet address
2. `mkdir /etc/consul.d`
3. `mkdir /var/lib/consul`
4. `consul agent -server -bootstrap-expect=3 -node=<CONTAINER_NAME> -bind=<IP_ADDRESS> -data-dir=/var/lib/consul -config-dir=/etc/consul.d`
5. `consul members`
6. `consul join <OTHER_SERVER_IP>`

## Run consul client

1. `ifconfig` -> eth0 inet address
2. `consul agent -bind=<IP_ADDRESS> -data-dir=/var/lib/consul -config-dir=/etc/consul.d`
3. `consul members`
4. `consul join <SERVER_IP>`
5. `consul reload` after creating a service schema
6. `apk -U add bind-tools`
7. `dig @localhost -p 8600 nginx.service.consul`
