# ETCswap V3 Subgraph

Subgraph for indexing ETCswap V3 protocol data on Ethereum Classic.

## Supported Networks

- `etc` - Ethereum Classic Mainnet (Chain ID: 61)
- `mordor` - Mordor Testnet (Chain ID: 63)

## Development

### Prerequisites

1. Install dependencies
```bash
yarn install
```

### Build and Deploy

2. Build a v3 subgraph
```bash
yarn build --network <network> --subgraph-type v3
```

3. Deploy a v3 subgraph
```bash
yarn build --network <network> --subgraph-type v3 --deploy
```

4. Build a v3-tokens subgraph
```bash
yarn build --network <network> --subgraph-type v3-tokens
```

5. Deploy a v3-tokens subgraph
```bash
yarn build --network <network> --subgraph-type v3-tokens --deploy
```

**Note:** Deployments will fail if there are uncommitted changes in the subgraph. Please commit your changes before deploying.

## Configuration

Before deploying, update the config files in `config/<network>/config.json` with:
- `factory` - The deployed ETCswapV3Factory contract address
- `startblock` - The block number when the factory was deployed

## Post-Deployment TODO

After deploying ETCswap V3 contracts to ETC/Mordor:

1. Update `config/etc/config.json` with actual factory address and start block
2. Update `config/mordor/config.json` with actual factory address and start block
3. Build and deploy the subgraph to your Graph Node instance

## Links

- ETCswap V3 App: https://v3.etcswap.org
- ETCswap V3 Analytics: https://v3-info.etcswap.org
- Documentation: https://docs.etcswap.org
