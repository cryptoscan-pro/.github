# CEX API - Cryptoscan

API to listen live centralized exchanges prices and volume in realtime. Spot + Futures.

**Current Price**: $1350
**Contacts**: https://t.me/dan_cryptoscan

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

Features:

- WebSocket Listen price updates
- WebSocket Listen coin listings
- WebSocket Listen volume/price changes by % by the time
- Get all price + volume tokens HTTP Route
- Get minified all tokens data HTTP route

## HTTP Api

### Get all tokens groupped by exchange

```shell
curl http://localhost:3000/
```

### Get all tokens minified

```shell
curl http://localhost:3000/min
```

## Websocket

### Listen all price updates

```shell
wscat -c ws://localhost:3000/
```

### Listen price changes

Request:

- thresholds Object
- threshold[key] -- Type of time (5s, 10m, 1h, 18h)
- threshold[value] -- Percentage of price change

```shell
wscat -c ws://localhost:3000/listen
{"thresholds":{"5s":{"price":0.1},"10s":{"price":2}}}
```

### Listen volume changes

Request:
- thresholds Object
- threshold[key] - Type of time (5s, 10m, 1h, 18h)
- threshold[value] - Percentage of volume change

```shell
wscat -c ws://localhost:3000/listen
{"thresholds":{"5s":{"volume":0.1},"10s":{"volume":2}}}
```

### Listen coin changes

```shell
wscat -c ws://localhost:3000/listen
{"symbols": ["BTCUSDT"], "thresholds":{"10s":{"volume":0.1}}}
{"symbols": ["BTCUSDT"], "exchanges": ["bybit"], "thresholds":{"5s":{"volume":0.1}}}
```

## WebSocket API Overview

### WebSocket Connection

- **Endpoint**: `/`
- **Description**: Establishes a WebSocket connection for listening to price updates.

### Listen Endpoint

- **Endpoint**: `/listen`
- **Description**: Allows clients to listen for price and volume changes based on specified thresholds.
- **Request Format**:
  - `thresholds`: Object containing time-based thresholds for price and volume changes.
  - `symbols`: Array of symbols to filter the updates.
  - `exchanges`: Array of exchanges to filter the updates.

### Recent Listings

- **Endpoint**: `/recent-listings`
- **Description**: Returns the most recent listings and delistings from various exchanges.

### Listings WebSocket

- **Endpoint**: `/listings`
- **Description**: Establishes a WebSocket connection for listening to new listings and delistings.

### Minified Tokens

- **Endpoint**: `/min`
- **Description**: Returns a minified version of all tokens data.

### Tickers

- **Endpoint**: `/tickers`
- **Description**: Returns the current tickers for all exchanges being monitored.

### Monitoring

The application monitors various exchanges for new listings and delistings, sending updates to connected clients in real-time. The following exchanges are monitored:
- Bitget
- Kucoin
- Gateio
- Mexc
- OKX
- Bybit
- HTX

The application uses WebSocket for real-time communication and supports filtering based on user-defined thresholds for price and volume changes.
