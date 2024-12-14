# Onchain Tracking

## Get latest onchain activity

This section provides the latest onchain activity, offering insights into recent blockchain transactions.

- [GET]

```
https://api.cryptoscan.pro?type=onchain&variant=latest
```

- [WS] Listen Updates

```json
{ "type": "onchain", "variant": "latest" }
```

## Get 24 hours all flows

This section tracks all onchain flows over the past 24 hours, helping users to understand daily transaction patterns.

- [GET]

```
https://api.cryptoscan.pro?type=onchain&variant=24h-flows
```

- [WS] Listen Updates

```json
{ "type": "onchain", "variant": "24h-flows" }
```

## Get 1 hour all flows

This section provides data on all onchain flows within the last hour, offering insights into short-term transaction trends.

- [GET]

```
https://api.cryptoscan.pro?type=onchain&variant=1h-flows
```

- [WS] Listen Updates

```json
{ "type": "onchain", "variant": "1h-flows" }
```

## Get active onchain

This section highlights active onchain addresses, helping users to identify key players in the blockchain network.

- [GET]

```
https://api.cryptoscan.pro?type=onchain&variant=active
```

- [WS] Listen Updates

```json
{ "type": "onchain", "variant": "active" }
```

## Get 24h ETH Flows

This section tracks Ethereum flows over the past 24 hours, providing insights into ETH-specific transaction patterns.

- [GET]

```
https://api.cryptoscan.pro?type=onchain&variant=24h-eth-flows
```

- [WS] Listen Updates

```json
{ "type": "onchain", "variant": "24h-eth-flows" }
```

## Get 1h ETH Flows

This section provides data on Ethereum flows within the last hour, offering insights into short-term ETH transaction trends.

- [GET]

```
https://api.cryptoscan.pro?type=onchain&variant=1h-eth-flows
```

- [WS] Listen Updates

```json
{ "type": "onchain", "variant": "1h-eth-flows" }
```
