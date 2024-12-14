# CEX Networks API - Cryptoscan

API to get realtime networks statuses, listen networks updates

**Current Price**: $600
**Contacts**: https://t.me/dan_cryptoscan

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

Features:

- 100+ Exchanges support.
- Show hided from exchange networks
- WebSocket Listen disables/enables networks
- WebSocket Listen deposit/withdraw fee changes
- WebSocket Listen network name changes
- Detect extra % / smart contract fees
- Get all networks HTTP Route
- Get minified all networks HTTP route


## HTTP Api

### Get all networks groupped by exchange

```
curl http://localhost:3000/
```

#### Get Minified Network List
```bash
curl http://localhost:3000/min
```

### WebSocket API

#### Listen for Updates
```bash
wscat -c ws://localhost:3000/listen
```

See [API Documentation](docs/API.md) for detailed API specifications.

## Configuration

- `MAX_HISTORY_AGE`: 24 hours (configurable in milliseconds)
- WebSocket connection timeout: 4 hours
- Network update interval: 1 second
- Memory usage logging: Every 60 seconds
- Data cleanup interval: Every hour

## License

[Add your license information here]
