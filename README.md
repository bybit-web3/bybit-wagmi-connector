# Bybit Wagmi Connector
This small package allows you to add a dedicated, functional, connector to integrate Bybit Wallet into your wagmi ^v1 project

to install
```sh
yarn add bybit-wagmi-connector
# or
npm install bybit-wagmi-connector
# or
pnpm add bybit-wagmi-connector
```

## Import
```javascript
import { BybitConnector } from 'bybit-wagmi-connector'
```

## Usage
```javascript
import { BybitConnector } from 'bybit-wagmi-connector'

const connector = new BybitConnector()
```

## Configuration

### chains (optional)
```javascript
import { mainnet, polygon } from 'wagmi/chains'
import { BybitConnector } from 'bybit-wagmi-connector'

const connector = new BybitConnector({
  chains: [mainnet, polygon],
})
```
### options (optional)
Options for configuring the connector.

```javascript
import { BybitConnector } from 'bybit-wagmi-connector'
 
const connector = new BybitConnector({
  options: {
    shimDisconnect: true,
  },
})
```

### shimDisconnect

Bybit does not support programmatic disconnect on EVM chains. This flag simulates the disconnect behavior by keeping track of connection status in storage. Defaults to true.
```javascript

import { BybitConnector } from 'bybit-wagmi-connector'
 
const connector = new BybitConnector({
  options: {
    shimDisconnect: false,
  },
})
```