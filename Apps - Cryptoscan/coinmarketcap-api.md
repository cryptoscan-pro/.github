# CoinMarketCap API - Cryptoscan

A real-time cryptocurrency price and information tracker that monitors both centralized (CEX) and decentralized (DEX) exchanges.

**Contacts**: [https://t.me/dan_cryptoscan](https://t.me/dan_cryptoscan)

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

## Features

- Real-time price monitoring for both CEX and DEX tokens
- Automatic data refresh based on liquidity groups
- WebSocket broadcasting of price updates
- Rate limiting and queue management for API requests
- Proxy support for reliable data fetching
- REST API endpoint for grouped coin data

## Architecture

### Core Components

1. **Price Fetching**
   - CEX prices via cryptoscan.pro API
   - DEX prices via CoinMarketCap's dexscan
   - Proxy rotation system for reliable scraping

2. **Data Management**
   - File-based storage using FileMap
   - Grouped by symbol and exchange
   - Price change detection and broadcasting

3. **Rate Limiting**
   - Concurrent request management (100 concurrent requests)
   - Dynamic update intervals based on liquidity groups:
     - Ultra Low Liquidity: 60 minutes
     - Very Low Liquidity: 10 minutes
     - Low Liquidity: 60 seconds
     - Medium Liquidity: 30 seconds
     - High Liquidity: 10 minutes

## API Reference

### GET /
Returns all coins grouped by symbol and exchange name.

Response format:
```json
{
  "[symbol]": {
    "[exchangeName]": [
      {
        // coin data
      }
    ]
  }
}
```

## WebSocket Updates

The system broadcasts real-time price updates when changes are detected. Connect to the WebSocket endpoint to receive live updates.

## Environment Variables

- `CRYPTOSCAN_API_KEY`: API key for proxy service
- `API_KEY`: CoinMarketCap API key

## Installation

```bash
npm install
```

## Running the Project

Development:
```bash
npm run start:debug
```

Production:
```bash
npm run start
```

Tests:
```bash
npm test
```

## Dependencies

- `@javeoff/proxy-fetch`: Proxy rotation for requests
- `@javeoff/file-map`: File-based data storage
- `hono`: Web framework
- `jsdom`: DOM parsing for scraping
- `p-queue`: Queue management
- `bottleneck`: Rate limiting
- `groupby-esm`: Data grouping utility

## License

ISC
