# usage

```
docker run --rm\
    -e OS_USERNAME=admin \
    -e OS_PASSWORD=ADMIN_PASS \
    -e OS_AUTH_URL=http://keystone:5000/v2.0 \
    -e OS_TENANT_NAME=admin \
    ardin/openstackclient openstack --help
```

or

```
docker run\ 
    -ti --rm=true \ 
    -v `pwd`/admin-openrc.sh:/root/admin-openrc.sh:Z \
    ardin/openstackclient bash

## in container
source /root/admin-openrc.sh
openstack --help
```
