# Arbitrage Loader - Cryptoscan

A real-time cryptocurrency arbitrage detection system that monitors price differences between various exchanges (CEX and DEX) and identifies profitable trading opportunities

**Current Price**: $360
**Contacts**: https://t.me/dan_cryptoscan

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

## Features

- Real-time monitoring of cryptocurrency prices across multiple exchanges
- Detection of arbitrage opportunities between:
  - CEX to CEX (Centralized Exchanges)
  - DEX to CEX (Decentralized to Centralized Exchanges)
- Configurable spread thresholds for notifications
- WebSocket API for real-time updates
- Spread change triggers to minimize noise

## Installation

```bash
# Clone the repository
git clone [repository-url]

# Install dependencies
bun install
```

## Usage

### Starting the Server

```bash
bun start
```

The server will start on port 3000 by default.

### WebSocket API

Connect to the WebSocket server to receive real-time arbitrage opportunities:

#### Basic Connection
```bash
wscat -c ws://localhost:3000/
```

#### Filtered Connection with Thresholds
Connect and set spread thresholds to receive only specific opportunities:

```bash
# Connect and send threshold configuration
wscat -c ws://localhost:3000/
```

### Setting Spread Thresholds

Send a JSON message after connection to configure spread thresholds:

```json
{
  "thresholds": {
    "spread": {
      "min": 0.1,
      "max": 10
    }
  }
}
```

This will only show arbitrage opportunities with spreads between 0.1% and 10%.

#### Listen Endpoint
For a simplified connection with default thresholds (-999% to 999%):
```bash
wscat -c ws://localhost:3000/listen
```

## Architecture

### Core Components

1. **Price Listeners**
   - `listenCexPrices`: Monitors centralized exchange prices
   - `listenDexPrices`: Monitors decentralized exchange prices

2. **Arbitrage Detectors**
   - `listenCexArbitrage`: Detects arbitrage between centralized exchanges
   - `listenDexCexArbitrage`: Detects arbitrage between DEX and CEX

3. **WebSocket Server**
   - Handles real-time client connections
   - Manages spread thresholds
   - Broadcasts arbitrage opportunities

### Configuration

Key constants in `constants.ts`:
```typescript
SPREAD_CHANGE_TRIGGER = 0.05  // Minimum spread change to trigger notification (5%)
```

API Endpoints:
- CEX Prices: `ALL_API_URL`
- DEX Prices: `DEX_PRICES_URL`
- WebSocket Prices: `LISTEN_CEX_PRICES_API`, `LISTEN_DEX_PRICES_API`

## Message Format

Arbitrage opportunities are broadcast in the following format:

```typescript
{
  exchangeFrom: string;    // Source exchange
  exchangeTo: string;      // Destination exchange
  symbol: string;         // Trading pair symbol
  priceFrom: string;      // Buy price
  priceTo: string;        // Sell price
  spread: number;         // Percentage profit potential
}
```

## Dependencies

- `bignumber.js`: Precise numerical calculations
- `hono`: Web framework
- `ws`: WebSocket client
- `@javeoff/ws-reconnect`: WebSocket reconnection handling
- `cryptoscan-provider`: Price data provider

## Development

The project is built with:
- TypeScript
- Bun runtime
- WebSocket for real-time communications
- BigNumber.js for precise calculations

## License

ISC
