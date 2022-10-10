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


[vuejs-client](https://github.com/Daiteap/vuejs-client) clone into the same folder where this repository is cloned

```shell
# clone vuejs-client (make sure it is in the same directory as this repository)
git clone https://github.com/Daiteap/vuejs-client

# clone and cd into this repository
git clone https://github.com/Daiteap/platform-api
cd platform-api

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

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
