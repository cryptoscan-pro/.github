# CEX Tracking

## Get networks statuses

```
https://api.cryptoscan.pro?type=networks
```

```
{ "type": "networks" }
```

## Get pumps/dumps in 10 seconds


```
https://api.cryptoscan.pro?type=dex&includes[price]=change10s&sort[priceChange10s]=asc
```

```
{ "type": "dex", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get pumps/dumps in X minutes


```
https://api.cryptoscan.pro?type=dex&includes[price]=change1m&sort[priceChange1m]=asc
```

```
{ "type": "dex", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get buys/sells in 10 seconds

```
https://api.cryptoscan.pro?type=dex&includes[price]=change10s&sort[priceChange10s]=asc
```

```
{ "type": "dex", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get buys/sells in X minutes

```
https://api.cryptoscan.pro?type=dex&includes[price]=change1m&sort[priceChange1m]=asc
```

```
{ "type": "dex", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get funding rates [WIP]

```
https://api.cryptoscan.pro?type=funding
```

```
{ "type": "funding" }
```

## Get top interests [WIP]

```
https://api.cryptoscan.pro?type=news&variant=top-interest
```

```
{ "type": "news", "variant": "top-interest" }
```

## Get liquidations [WIP]

```
https://api.cryptoscan.pro?type=liquidations
```

```
{ "type": "liquidations" }
```
