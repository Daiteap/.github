## Daiteap Cloud Solutions

Daiteap is an open-source platform which enables developers and IT professionals to use multiple cloud providers' resources like Kubernetes clusters, Compute VMs and Storage in an easy and integrated fasion. The platform offers the following advantages:

- Web UI to manage multi-cloud resources and environments across a range of public and private cloud providers
- Ability to create multi-cloud Kubernetes and Compute clusters where one cluster spans multiple cloud providers
- API to manage different cloud providers without needing to integrate each provider separately
- CLI tool to automate and integrate `daiteap` into existing systems and automation scripts

For further information visit our website [daiteap.com](https://www.daiteap.com/)


## Getting Started ##

### Fast Track ###

Follow the steps below to run Daiteap locally. 

Requirements:
- docker 
- GIT


[daiteap-ui](https://github.com/Daiteap/diteap-ui) clone into the same folder where this repository is cloned

```shell
# clone daiteap-ui (make sure it is in the same directory as this repository)
git clone https://github.com/Daiteap/daiteap-ui

# clone and cd into this repository
git clone https://github.com/Daiteap/daiteap-platform
cd daiteap-platform

# build images
docker-compose build

# generate ssh keys
mkdir -p docker-compose/.ssh
ssh-keygen -o -a 100 -t rsa -f docker-compose/.ssh/id_rsa -C "user@server.com" -N "" -m PEM

# start daiteap locally
docker-compose -f docker-compose.yml --log-level DEBUG up

# Init environment (first start only)
sh docker-compose/init.sh

# Navigate to http://localhost:18090


