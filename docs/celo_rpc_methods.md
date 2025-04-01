# Celo Blockchain RPC Methods

Based on research, Celo supports Ethereum-compatible JSON-RPC methods along with some Celo-specific methods. Here's a compilation of the available RPC namespaces and methods:

## Standard Ethereum Namespaces Supported by Celo

Celo is built on a fork of Ethereum's go-ethereum (geth), so it supports most standard Ethereum JSON-RPC methods in these namespaces:

### eth
Standard Ethereum methods for interacting with the blockchain:
- `eth_blockNumber`
- `eth_call`
- `eth_chainId`
- `eth_estimateGas`
- `eth_gasPrice`
- `eth_getBalance`
- `eth_getBlockByHash`
- `eth_getBlockByNumber`
- `eth_getCode`
- `eth_getFilterChanges`
- `eth_getFilterLogs`
- `eth_getLogs`
- `eth_getStorageAt`
- `eth_getTransactionByHash`
- `eth_getTransactionByBlockHashAndIndex`
- `eth_getTransactionByBlockNumberAndIndex`
- `eth_getTransactionCount`
- `eth_getTransactionReceipt`
- `eth_newBlockFilter`
- `eth_newFilter`
- `eth_newPendingTransactionFilter`
- `eth_sendRawTransaction`
- `eth_sendTransaction`
- `eth_subscribe`
- `eth_syncing`
- `eth_uninstallFilter`
- `eth_unsubscribe`

### net
Network-related methods:
- `net_listening`
- `net_peerCount`
- `net_version`

### web3
Utility methods:
- `web3_clientVersion`
- `web3_sha3`

### txpool
Transaction pool methods:
- `txpool_content`
- `txpool_inspect`
- `txpool_status`

### debug
Debugging methods (more extensive than standard Ethereum):
- Various debug methods for node operators and developers

## Celo-Specific Namespaces

Celo extends Ethereum's functionality with additional namespaces specific to its features:

### istanbul
Constantinople/Istanbul consensus related methods:
- `istanbul_getValidators`
- `istanbul_getValidatorsAtHash`
- `istanbul_propose`
- `istanbul_discard`

### parity
Some Parity-compatible APIs:
- Limited set of Parity namespace methods

### les
Light Ethereum Subprotocol methods:
- Various LES-related methods

### clique
Proof of Authority related methods:
- Various clique-related methods

### personal
Account management methods:
- `personal_importRawKey`
- `personal_listAccounts`
- `personal_lockAccount`
- `personal_newAccount`
- `personal_unlockAccount`
- `personal_sendTransaction`
- `personal_sign`
- `personal_ecRecover`

### admin
Node administration:
- `admin_addPeer`
- `admin_datadir`
- `admin_nodeInfo`
- `admin_peers`
- `admin_startRPC`
- `admin_startWS`
- `admin_stopRPC`
- `admin_stopWS`

### miner
Mining related methods:
- `miner_setEtherbase`
- `miner_setGasPrice`
- `miner_start`
- `miner_stop`

## Celo-Specific Extensions

### account
Celo account-related methods, including:
- Methods for interacting with Celo's account model, which has additional features compared to Ethereum

### election
Validator election methods:
- Methods for interacting with validator elections

### attestation
Identity attestation methods:
- Methods for phone number verification and attestations

### exchange
StableToken exchange methods:
- Methods for interacting with Celo's built-in exchange

### lockedgold
Methods for locking CELO:
- Methods for interacting with Celo's locked gold system

### validator
Validator management methods:
- Methods for validator operations

## Available RPC Endpoints

Celo has multiple public and paid RPC endpoints available:

### Mainnet
- `https://forno.celo.org` (operated by cLabs)
- `https://rpc.ankr.com/celo` (operated by Ankr)
- `https://celo.quicknode.pro` (operated by QuickNode, requires API key)
- `https://celo-mainnet.drpc.org` (operated by dRPC)

### Alfajores Testnet
- `https://alfajores-forno.celo-testnet.org` (operated by cLabs)

### Baklava Testnet
- `https://baklava-forno.celo-testnet.org` (operated by cLabs)

## Usage Notes

- Celo uses the same JSON-RPC format as Ethereum, with requests formatted as:
  ```json
  {
    "jsonrpc": "2.0",
    "method": "eth_blockNumber",
    "params": [],
    "id": 1
  }
  ```

- Most Ethereum tooling (web3.js, ethers.js, web3.py, etc.) works with Celo with minimal configuration changes.

- Celo has a different fee currency mechanism than Ethereum, allowing transaction fees to be paid in stable tokens (cUSD, cEUR, etc.) in addition to CELO.

- For wallet integration, developers typically use ContractKit, Celo's JavaScript library that extends the core Ethereum libraries with Celo-specific functionality.

## Resources

- [Celo Developer Documentation](https://docs.celo.org/)
- [Celo GitHub Repository](https://github.com/celo-org/celo-blockchain)
- [ContractKit Documentation](https://docs.celo.org/learn/developer-tools/contractkit)