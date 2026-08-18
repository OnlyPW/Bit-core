# Getting Started with BIT Core

This guide helps you launch a node, connect your wallet, and verify the setup.

## 1) Install or Build

- See [../INSTALL.md](../INSTALL.md) for dependency and build steps.
- Expected binaries:
  - `bitd`
  - `bit-cli`
  - `bit-tx`
  - `bit-qt`

## 2) Start a Node

Mainnet:

```bash
bitd -daemon
```

Testnet:

```bash
bitd -testnet -daemon
```

Regtest (for local development):

```bash
bitd -regtest -daemon
```

## 3) Verify Node Status

```bash
bit-cli getblockchaininfo
bit-cli getnetworkinfo
```

For testnet/regtest, add the network flag:

```bash
bit-cli -testnet getblockchaininfo
bit-cli -regtest getblockchaininfo
```

## 4) Wallet Basics

Create a receiving address:

```bash
bit-cli getnewaddress
```

Check balance:

```bash
bit-cli getbalance
```

## 5) Regtest Quick Mining (for local tests)

Generate blocks to a local address:

```bash
ADDR=$(bit-cli -regtest getnewaddress)
bit-cli -regtest generatetoaddress 101 "$ADDR"
bit-cli -regtest getbalance
```

## 6) Next Steps

- Nickname usage examples: [how-to-use.md](how-to-use.md)
- RPC command list:

```bash
bit-cli help
bit-cli help sendtonickname
```
