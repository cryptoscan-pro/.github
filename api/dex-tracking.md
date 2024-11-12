# DEX Tracking

## Get pumps/dumps in 10 seconds

This section identifies rapid price changes (pumps or dumps) within a 10-second interval, helping users to quickly react to market movements.

- [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change10s&sort[priceChange10s]=asc
```

- [WS] Listen Updates

```json
{ "type": "dex", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get pumps/dumps in 1 minute

This section tracks price changes over a 1-minute interval, allowing users to analyze short-term market trends.

- [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change1m&sort[priceChange1m]=asc
```

- [WS] Listen Updates

```json
{ "type": "dex", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get pumps/dumps in 1 hour

This section provides data on price changes over a 1-hour period, helping users to understand longer-term market movements.

- [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change1h&sort[priceChange1h]=asc
```

- [WS] Listen Updates

```json
{ "type": "dex", "includes[price]": "change1h", "sort[priceChange1h]": "asc" }
```

## Get buys/sells in 10 seconds

This section provides data on buy and sell activities within a 10-second window, enabling users to observe short-term trading behaviors.

- [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change10s&sort[priceChange10s]=asc
```

- [WS] Listen Updates

```json
{ "type": "dex", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get buys/sells in 1 minute

This section offers insights into buy and sell activities over a 1-minute interval, helping users to understand short-term trading patterns.

- [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change1m&sort[priceChange1m]=asc
```

- [WS] Listen Updates

```json
{ "type": "dex", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get buys/sells in 1 hour

This section tracks buy and sell activities over a 1-hour period, providing users with data on longer-term trading behaviors.

- [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change1h&sort[priceChange1h]=asc
```

- [WS] Listen Updates

```json
{ "type": "dex", "includes[price]": "change1h", "sort[priceChange1h]": "asc" }
```

## Get Smart traders transactions [WIP]

This section provides data on transactions made by smart traders, offering insights into strategic trading activities.

- [GET]

```
https://api.cryptoscan.pro?type=news&variant=smart-traders
```

- [WS] Listen Updates

```json
{ "type": "news", "variant": "smart-traders" }
```

## Get trending coins [WIP]

This section highlights coins that are currently trending, helping users to identify popular investment opportunities.

- [GET]

```
https://api.cryptoscan.pro?type=news&variant=trending
```

- [WS] Listen Updates

```json
{ "type": "news", "variant": "trending" }
```

## Get DEX Track [WIP]

This section tracks decentralized exchange activities, providing users with comprehensive data on DEX transactions.

- [GET]

```
https://api.cryptoscan.pro?type=news&variant=dex-track
```

- [WS] Listen Updates

```json
{ "type": "news", "variant": "dex-track" }
```

## Get BSC DEX Track [WIP]

This section focuses on tracking activities on Binance Smart Chain (BSC) decentralized exchanges, offering insights into BSC-specific transactions.

- [GET]

```
https://api.cryptoscan.pro?type=news&variant=bsc-track
```

- [WS] Listen Updates

```json
{ "type": "news", "variant": "bsc-track" }
```

## Get New pairs ETH Track [WIP]

This section provides information on newly created trading pairs on Ethereum, helping users to discover new investment opportunities.

- [GET]

```
https://api.cryptoscan.pro?type=news&variant=eth-mints
```

- [WS] Listen Updates

```json
{ "type": "news", "variant": "eth-mints" }
```
