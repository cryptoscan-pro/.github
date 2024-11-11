# CEX Tracking

## Get networks statuses

### [GET]

```
https://api.cryptoscan.pro?type=networks
```

### [WS] Listen Updates

```
{ "type": "networks" }
```

## Get pumps/dumps in 10 seconds

### [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change10s&sort[priceChange10s]=asc
```

### [WS] Listen Updates

```
{ "type": "dex", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get pumps/dumps in X minutes

### [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change1m&sort[priceChange1m]=asc
```

### [WS] Listen Updates

```
{ "type": "dex", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get buys/sells in 10 seconds

### [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change10s&sort[priceChange10s]=asc
```

### [WS] Listen Updates

```
{ "type": "dex", "includes[price]": "change10s", "sort[priceChange10s]": "asc" }
```

## Get buys/sells in X minutes

### [GET]

```
https://api.cryptoscan.pro?type=dex&includes[price]=change1m&sort[priceChange1m]=asc
```

### [WS] Listen Updates

```
{ "type": "dex", "includes[price]": "change1m", "sort[priceChange1m]": "asc" }
```

## Get funding rates [WIP]

### [GET]

```
https://api.cryptoscan.pro?type=funding
```

### [WS] Listen Updates

```
{ "type": "funding" }
```

## Get top interests [WIP]

### [GET]

```
https://api.cryptoscan.pro?type=news&variant=top-interest
```

### [WS] Listen Updates

```
{ "type": "news", "variant": "top-interest" }
```

## Get liquidations [WIP]

### [GET]

```
https://api.cryptoscan.pro?type=liquidations
```

### [WS] Listen Updates

```
{ "type": "liquidations" }
```
