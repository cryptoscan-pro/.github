# CEX Rates Api

A microservice that provides real-time order book depth and exchange rate information from multiple cryptocurrency exchanges.

**Current Price**: $1800

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

## Features

- 100+ Exchanges integration
- Real-time order book depth data
- Exchange rate calculations
- Support for multiple exchanges (configurable)
- Built-in request caching
- Proxy support for reliable API access

## Prerequisites

- Node.js (LTS version)
- npm
- Environment variables configuration

## Installation

1. Clone the repository:
```bash
git clone cryptoscan-pro/cex-rates-api
cd cex-depths-loader
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file with the following variables:
```env
EXCHANGES=binance,kucoin,huobi  # comma-separated list of supported exchanges
```

## Usage

Start the server:
```bash
npm start
```

The server will run on port 3000 by default.

## API Endpoints

### Get Order Book Depth

```
GET /?exchange={exchange}&from={fromCurrency}&to={toCurrency}
```

Parameters:
- `exchange`: Exchange name (e.g., binance, kucoin)
- `from`: Base currency (e.g., BTC)
- `to`: Quote currency (e.g., USDT)

Response example:
```json
{
  "asks": [[price, amount], ...],
  "bids": [[price, amount], ...]
}
```

### Get Exchange Rate

```
GET /rate?exchange={exchange}&from={fromCurrency}&to={toCurrency}&amount={amount}&depth={0|1}
```

Parameters:
- `exchange`: Exchange name
- `from`: Source currency
- `to`: Target currency
- `amount`: Amount to convert
- `depth`: Include order book depth (0 or 1)

Response example:
```json
{
  "rate": 45000,
  "amount": 1,
  "total": 45000
}
```

## Development

The project uses semantic-release for versioning and automated releases. Commit messages should follow the [Conventional Commits](https://www.conventionalcommits.org/) specification.

## License

ISC
