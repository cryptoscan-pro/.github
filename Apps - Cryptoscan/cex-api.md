# CEX API - Cryptoscan

Real-time cryptocurrency price and volume monitoring API for centralized exchanges (Spot + Futures).

**Contact**: https://t.me/dan_cryptoscan

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [HTTP API](#http-api)
- [WebSocket API](#websocket-api)
- [Supported Exchanges](#supported-exchanges)
- [Development](#development)

## Features
- Real-time price updates via WebSocket
- New coin listing notifications
- Volume and price change monitoring with custom thresholds
- HTTP endpoints for current market data
- Minified data format support
- Multi-exchange support
- Custom filtering by symbols and exchanges

## Installation

```bash
# Clone the repository
git clone [repository-url]

# Install dependencies
npm install

# Start the service
npm start
```

## HTTP API

### Get All Tokens by Exchange
Returns all tokens grouped by exchange.

```bash
GET http://localhost:3000/
```

### Get Minified Token Data
Returns compressed token data format.

```bash
GET http://localhost:3000/min
```

### Get Current Tickers
Returns current ticker data for all monitored exchanges.

```bash
GET http://localhost:3000/tickers
```

## WebSocket API

### Price Updates Stream
Connect to the main WebSocket endpoint to receive all price updates.

```bash
ws://localhost:3000/
```

### Filtered Updates Stream
Connect with custom filters for specific symbols, exchanges, or threshold conditions.

**Endpoint**: `ws://localhost:3000/listen`

#### Example: Price Change Monitoring
```json
{
  "thresholds": {
    "5s": {"price": 0.1},
    "10s": {"price": 2}
  }
}
```

#### Example: Volume Change Monitoring
```json
{
  "thresholds": {
    "5s": {"volume": 0.1},
    "10s": {"volume": 2}
  }
}
```

#### Example: Symbol & Exchange Filtering
```json
{
  "symbols": ["BTCUSDT"],
  "exchanges": ["bybit"],
  "thresholds": {
    "5s": {"volume": 0.1}
  }
}
```

### Listings Stream
Monitor new listings and delistings across exchanges.

```bash
ws://localhost:3000/listings
```

## Supported Exchanges
- Binance
- Bitget
- Kucoin
- Gateio
- Mexc
- OKX
- Bybit
- HTX

## Development

### What's Included
- Free setup assistance for your hosting
- Access to full codebase and updates
- Issue tracking and feature requests
- Project time tracking
- Technical support

### Contributing
1. Fork the repository
2. Create your feature branch
3. Submit a pull request

## Support
For technical support or custom integration assistance, contact us on Telegram: https://t.me/dan_cryptoscan
