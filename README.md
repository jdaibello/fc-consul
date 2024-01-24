# Run consul server

`ifconfig` -> eth0 inet address
`mkdir /etc/consul.d`
`mkdir /var/lib/consul`
`consul agent -server -bootstrap-expect=3 -node=<CONTAINER_NAME> -bind=<IP_ADDRESS> -data-dir=/var/lib/consul -config-dir=/etc/consul.d`
