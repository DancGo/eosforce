# EOS Force

## Supported Operating Systems

EOS Force currently supports the following operating systems:

1. Ubuntu 16.04 (Ubuntu 16.10 recommended)
2. macOS 10.12 and higher (macOS 10.13.x recommended)

## Getting Started

```bash
# clone this repository and build
$ git clone https://github.com/eosforce/eosforce.git eosforce
$ cd eosforce
$ git submodule update --init --recursive
$ ./eosio_build.sh

# once you've built successfully
$ cd build && make install

# also copy the generated abi and wasm contract file to ~/.local/share/eosio/nodeos/config
$ cp build/contracts/eosio.token/eosio.token.abi build/contracts/eosio.token/eosio.token.wasm ~/.local/share/eosio/nodeos/config
$ cp build/contracts/System/System.abi build/contracts/System/System.wasm ~/.local/share/eosio/nodeos/config

# place some p2p nodes in here, see the following seed list section
$ vim ~/.local/share/eosio/nodeos/config/config.ini

# download genesis.json to ~/.local/share/eosio/nodeos/config
$ curl https://raw.githubusercontent.com/eosforce/genesis/master/genesis.json -o ~/.local/share/eosio/nodeos/config/genesis.json

$ cd build/programs/nodeos && ./nodeos
```

:warning: Ensure your chain id is correct when your node is up: `bd61ae3a031e8ef2f97ee3b0e62776d6d30d4833c8f7c1645c657b149151004b`

### Seed list

These IPs could be used as `p2p-peer-address` in your `config.ini`:

IP            | P2P
:----:        | :----:
47.104.255.49 | 65511
47.254.71.89  | 8222
47.75.126.7   | 19876
47.96.232.211 | 8899
47.97.122.109 | 7894
101.132.77.22 | 9066

## Resources

1. [eosfore.io website](http://eosforce.io)
2. [Community Telegram Group](https://t.me/eosforce_en)
3. [Developer Telegram Group](https://t.me/EOSForce)