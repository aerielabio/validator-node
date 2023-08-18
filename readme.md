
# Aerie Validator Node

  
## Dependencies
1. CL & EL Node running properly, visit [here](https://github.com/aerielabio/public-node) for more details , DONT MAKE DEPOSIT UNTIL YOUR PUBLIC NODE RUNNING
2.  Deposits visit https://github.com/aerielabio/aerie-val-tools/ . We will release the GUI Version soon
3. Docker & Docker-compose installed

## Preparation

1. Make sure you already have the validator-keystores which you can obtain by making a deposit first. Visit our repository page that we have written in point number 2 above.
2. Ensure that your EL & CL Node is running and functioning properly.

Execution Steps:

1. Clone this Repo to your machine.
2. Go to the misc directory, create a new directory named **wallet-dir**, then paste the file you obtained from Dependencies #2 above.
3. Still in the misc folder, you will find prometheus.example.yml file. Copy that file as prometheus.yml, and edit it according to your server configuration.
4. Inside the misc folder, there is also validatorpass.txt, which contains the default wallet password obtained from aerie-val-tools. Make sure to change it if there are any changes.
5. Go back to the main directory, copy `.env.example` file as `.env`, and adjust its contents with your server configuration.
6. Run the following command: `docker-compose up -d`
7. Please understand that you have to wait 10 Blocks at least until the network observe your deposits. At that time, your validator node might showing Validator Status Invalid

## SETUP GRAFANA DASHBOARD

We have included a dashboard for you to monitor your validators, you can just visit http://yourserveripaddress:3000 , then login and setup a username and password ( default uname & password are admin ) . Once you logged in, you can import `grafana-dashboard.json` file content within misc folder into your grafana