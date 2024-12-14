# Jupiter API - Cryptoscan

A TypeScript wrapper for Jupiter DEX API on Solana blockchain with proxy support and rate fetching capabilities.

**Current Price**: $120

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

## Features

- Get exchange rates for Solana tokens
- Create swap transactions
- Automatic retry mechanism for failed requests
- Proxy support for requests
- Price impact and fee calculations
- Multi-route swaps support

## Installation

```bash
npm install jupiter-api
# or
bun install jupiter-api
```

## Usage

### Basic Setup

```typescript
import { jupiterApi } from 'jupiter-api';

// The API is pre-configured with default settings
// Including proxy support via @javeoff/proxy-fetch
```

### Getting Exchange Rates

```typescript
// Get rate for token swap
const rate = await jupiterApi.getRate({
  from: "USDC_ADDRESS", // Optional, defaults to USDC
  to: "TARGET_TOKEN_ADDRESS",
  amount: 1, // Optional, defaults to 1
  slippage: 1 // Optional, defaults to 1%
});
```

### Creating a Transaction

```typescript
const transaction = await jupiterApi.createTransaction({
  from: "SOURCE_TOKEN_ADDRESS",
  to: "TARGET_TOKEN_ADDRESS",
  amount: 1,
  walletAddress: "YOUR_WALLET_ADDRESS"
});
```

### Rate Response Structure

The getRate method returns a Rate object with the following structure:

```typescript
{
  network: "solana",
  service: "jupiter",
  price: number,
  priceUSD: number,
  amount: number,
  amountUSD: number,
  liquidityUSD: number,
  fromAddress: string,
  toAddress: string,
  fee: number,
  feeUSD: number,
  impact: number,
  routes: [
    {
      service: string,
      percentage: number,
      price: number,
      fee: number,
      feeUSD: number,
      priceUSD: number
    }
  ]
}
```

## API Endpoints

The service exposes two HTTP endpoints:

### GET /
Gets the exchange rate for specified tokens

Query Parameters:
- `from` (optional): Source token address (defaults to USDC)
- `to`: Target token address
- `amount` (optional): Amount to swap (defaults to 1)
- `slippage` (optional): Slippage tolerance in percentage (defaults to 1)

### GET /createTransaction
Creates a swap transaction

Query Parameters:
- `from`: Source token address
- `to`: Target token address
- `amount`: Amount to swap
- `walletAddress`: Solana wallet address

## Development

```bash
# Install dependencies
bun install

# Start the development server
bun start
```

## Dependencies

- @cryptoscan/solana-sdk: Solana blockchain interaction
- @javeoff/proxy-fetch: Proxy support for API requests
- bs58: Base58 encoding/decoding
- hono: HTTP server framework
- p-retry: Retry mechanism for failed requests

## License

ISC
