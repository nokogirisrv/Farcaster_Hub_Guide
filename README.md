# How to run your own Farcaster Hub

## Sign up on Alchemy

Start by creating a free account on Alchemy. This account is essential to connect your farcaster hub to Ethereum mainnet and Optimism Layer 2, allowing it to sync and communicate effectively with other hubs. 

The free plan offered by Alchemy *should* be adequate for running your hub.

[Alchemy Register](https://alchemy.com/?r=baa923610b5f9fe0)

## Spin up an Ethereum and Optimism node on Alchemy

Once you have an Alchemy account, set up new applications within it. You'll need to create two apps/nodes: one for Ethereum Mainnet (name it something like "Ethereum Farcaster") and another for Optimism.

After setting up these apps, Alchemy will provide you with RPC endpoint addresses for both Ethereum and Optimism. Make sure to note these addresses down as you'll need them later.

### Create new apps:

Create an Ethereum mainnet app

Create an Optimism app


### Get the Ethereum and Optimism endpoints

We now need to get the Ethereum and Optimism RPC endpoint address that you will use later when setting up the farcaster hub.

*In the main app screen, click on “API Key”*

*Copy-paste the HTTPS address in the API Key window for Ethereum*

![image](https://github.com/nokogirisrv/farcaster_hub_guide/assets/125523696/70a2b0ed-ce55-42e3-81a3-12a179f37beb)


*Copy-paste the HTTPS address in the API Key window for Optimism*

![image](https://github.com/nokogirisrv/farcaster_hub_guide/assets/125523696/da4c0ad4-bfe2-4af0-bba2-4d40f1dd5459)


## Install the farcaster hub (using Hubble)

*Official instructions here: [https://www.thehubble.xyz/intro/install.html](https://www.thehubble.xyz/intro/install.html)*

We’re going to install the farcaster hub using the Hubble package with a simple command in the console

```bash
curl -sSL https://download.thehubble.xyz/bootstrap.sh | bash
```

When prompted, enter the following:

- **Ethereum RPC Address:** Paste the address that you have on your ETH app
- **Optimism RPC Address:** Enter the address that you have on yout Optimism app
- **Farcaster username or fid:** Enter your farcaster FID

Started log for console should look like this:

![image](https://github.com/nokogirisrv/farcaster_hub_guide/assets/125523696/4048c3d0-9272-4b1c-99af-97b4abae680d)


### Access the grafana monitor

In a new browser window/tab enter the following address:

- http:// YOUR_IP : 3000

## Updating the hub

When you want/need to update to the latest version of the farcaster protocol or app you have to do two things:

1. Kill the current instance of the hub
2. Upgrade Hubble

### Kill current instance

```bash
docker stop $(docker ps -a -q)
```

### Upgrade
In a console execute the following code

```bash
cd ~/hubble && ./hubble.sh upgrade
```
