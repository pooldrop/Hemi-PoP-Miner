# Hemi PoP Miner Node

You will get tHEMI tokens for each block you mine with your Hemi Pop Node

## Install Miner on Linux

```bash
sudo apt-get update && sudo apt-get upgrade -y
```
```bash
wget https://github.com/hemilabs/heminetwork/releases/download/v0.4.5/heminetwork_v0.4.5_linux_amd64.tar.gz
```
```bash
tar -xvf heminetwork_v0.4.5_linux_amd64.tar.gz && rm heminetwork_v0.4.5_linux_amd64.tar.gz && cd heminetwork_v0.4.5_linux_amd64
```

Creat wallet

```bash
./keygen -secp256k1 -json -net="testnet" > ~/popm-address.json
```

Get BTC address

```bash
cat $HOME/popm-address.json
```

Get tBTC faucet in [Discord](https://discord.gg/hemixyz)

```bash
sudo apt install screen
```

```bash
screen -S hemi
```

> Replace your private key

```bash
export POPM_BTC_PRIVKEY=<private_key>
export POPM_STATIC_FEE=50
export POPM_BFG_URL=wss://testnet.rpc.hemi.network/v1/ws/public
```

```bash
./popmd
```

- To minizme screen: `CTRL+A+D`
- To return screen `screen -r hemi`

You can check points on : https://testnet.popstats.hemi.network/
