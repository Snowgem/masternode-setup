### This script is for root user on VPS only
#### Again make sure you run everything as `root`
### Install dependencies


On Ubuntu/Debian-based systems:
```
apt-get update
apt-get install wget unzip gpw curl libgomp1 -y
```

### NOTE
```
You don't need to download blockchain manually, latest script will do it for you
```

### Download setup file
```
git clone https://github.com/TENTOfficial/masternode-setup
cd masternode-setup
chmod +x part1.sh part2.sh part2_arm64.sh
```

### Create swap

Run the following commands:

```
./part1.sh
```

### Setup masternode

For example:
- Your masternode name is ```masternode1```
- Your vps ip is ```207.145.65.77```
- Your masternode privatekey is ```5JJaWWprqeNLwEYd5JucbUne68m51yumu5Peen5j5hrg4nrjej4```

**For amd64 processors run part2.sh**
```
./part2.sh masternode1 207.145.65.77 5JJaWWprqeNLwEYd5JucbUne68m51yumu5Peen5j5hrg4nrjej4
```
**For arm64 processors run part2_arm64.sh**
```
./part2_arm64.sh masternode1 207.145.65.77 5JJaWWprqeNLwEYd5JucbUne68m51yumu5Peen5j5hrg4nrjej4
```

Go `home` and check current syncing process:
```
cd
./snowgem-cli getinfo
```

You should receive this data:
```
{
  "balance": 0.00000000,
  "blocks": 1724480,
  "buildinfo": "v3.1.2",
  "connections": 19,
  "difficulty": 216.9279947763039,
  "errors": "",
  "keypoololdest": 1519585211,
  "keypoolsize": 101,
  "networksolps": 26983,
  "paytxfee": 0,
  "protocolversion": 170010,
  "proxy": "",
  "relayfee": 0.000001,
  "testnet": false,
  "timeoffset": 0,
  "version": 3010250,
  "walletversion": 60000
}
```

In this case, your current syncing is at block: 1724480
You need to wait for syncing finish. Check the latest block at: https://explorer.tent.app/

If your current block is latest block, go to TENT Core and start this masternode.
