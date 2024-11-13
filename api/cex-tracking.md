# CEX Tracking

## Get networks statuses

This section provides the status of various networks, allowing users to monitor network availability and performance.

- [GET]

```
https://api.cryptoscan.pro?type=networks
```

- [WS] Listen Updates

```
{ "type": "networks" }
```

## Get pumps/dumps in 10 seconds

This section identifies rapid price changes (pumps or dumps) within a 10-second interval, helping users to quickly react to market movements.

- [GET]

```
https://api.cryptoscan.pro?type=prices&includes[price]=change10s&sort[priceChange10s]=asc
```

- [WS] Listen Updates

```
{ "type": "prices", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get pumps/dumps in X minutes in bybit

This section tracks price changes over a customizable time frame, allowing users to analyze market trends over longer periods.

- [GET]

```
https://api.cryptoscan.pro?type=prices&exchange=bybit&includes[price]=change1m&sort[priceChange1m]=asc
```

- [WS] Listen Updates

```
{ "type": "prices", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get buys/sells in 10 seconds

This section provides data on buy and sell activities within a 10-second window, enabling users to observe short-term trading behaviors.

- [GET]

```
https://api.cryptoscan.pro?type=prices&includes[price]=change10s&sort[priceChange10s]=asc
```

- [WS] Listen Updates

```
{ "type": "prices", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get buys/sells in X minutes

This section offers insights into buy and sell activities over a specified time frame, helping users to understand longer-term trading patterns.

- [GET]

```
https://api.cryptoscan.pro?type=prices&includes[price]=change1m&sort[priceChange1m]=asc
```

- [WS] Listen Updates

```
{ "type": "prices", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get Coinmarketcap coins

This section provides CoinMarketcap data on various cryptocurrencies, including their market capitalization, price, and other relevant information.

- [GET]

```
https://api.cryptoscan.pro?type=cex-rates,dex-rates
```

- [WS] Listen Updates

```
{ "type": "cex-rates,dex-rates" }
```

## Get CoinGecko coins

This section provides CoinGecko data on various cryptocurrencies, including their market capitalization, price, and other relevant information.

- [GET]

```
https://api.cryptoscan.pro?type=prices
```

- [WS] Listen Updates

```
{ "type": "prices" }
```


## Get funding rates [WIP]

This section provides information on funding rates, which are crucial for understanding the cost of holding positions in futures markets.

- [GET]

```
https://api.cryptoscan.pro?type=funding
```

- [WS] Listen Updates

```
{ "type": "funding" }
```

## Get top interests [WIP]

This section highlights the most popular or trending topics in the market, offering users insights into current market interests.

- [GET]

```
https://api.cryptoscan.pro?type=news&variant=top-interest
```

- [WS] Listen Updates

```
{ "type": "news", "variant": "top-interest" }
```

## Get liquidations [WIP]

This section tracks liquidation events, providing users with data on forced closures of positions due to insufficient margin.

- [GET]

```
https://api.cryptoscan.pro?type=liquidations
```

- [WS] Listen Updates

```
{ "type": "liquidations" }
```
