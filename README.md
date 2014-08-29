meanio-single
===============

A HEAT template to provision a single instance of the mean.io stack. Initial provisioning just fulfills the pre-requisites.

Getting Started
===============
Requirements
 - Python 2.7.x
 - pip

Setup the following environment variables:
```
export OS_AUTH_URL=https://identity.api.rackspacecloud.com/v2.0/
export OS_USERNAME=<username>
export OS_TENANT_ID=<tenant_id>
export HEAT_URL=https://ord.orchestration.api.rackspacecloud.com/v1/${OS_TENANT_ID}  
export OS_PASSWORD=<password>
```
Install the heat command line tool:
```
python-pip install python-heatclient
```

To spin up this stack do the following:
```
heat stack-create -f meanio-single.yaml -P "ssh_keyname=<ssh keyname>;flavor=<flavor name>;image=<image name>" <stack name>
```
