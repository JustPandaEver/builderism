# optimism_builder
user-friendly tool to build your optimism mainnet

## configuration ( .env.example )
### common
- `CONFIG_DIR`: Directory that will store config data (default `../config`)
- `L1_CHAIN_ID`: L1 chain id (default `11155111`)
- `L1_RPC_URL`: L1 RPC endpoint
- `L1_RPC_KIND`: The type of RPC provider (default `standard`)
- `L2_CHAIN_ID`: Your L2 chain id

### init node
- `PRIORITY_GAS_PRICE`: Gas price during deploy contracts (default `10000`)
- `FAUCET_ADDRESS`: Charging address
- `FAUCET_PRIVATE_KEY`: Charging private key; Be careful about security
- `FAUCET_AMOUNT_ADMIN`: Faucet amount eth to admin (default `0.5`)
- `FAUCET_AMOUNT_BATCHER`: Faucet amount eth to batcher (default `0.2`)
- `FAUCET_AMOUNT_PROPOSER`: Faucet amount eth to proposer (default `0.1`)

### run node
- `L1_BEACON_URL`: L1 Beacon endpoint
- `GETH_DATA_DIR`: Directory that will store chain data (default `../geth_data`)
- `SEQUENCER_MODE`: If true, run sequencer mode (default `true`)
- `SEQUENCER_HTTP`: Sequencer node URL, only used for not sequencer mode
- `BOOTNODES`: Bootnode URL, only used for not sequencer mode

### sdk
- `L2_RPC_URL`: L2 RPC endpoint (default `http://localhost:8545`)

## init your node
```
make init
```

## run your node
```
make run
```

## run blockscout
```
make scan
```

## bridge eth / erc20 ( L1 <-> L2 )
```
make bridge
```