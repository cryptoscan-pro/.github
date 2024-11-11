# Arbitrage

## Funding Arbitrage

Arbitrage in CEX futures markets

- [GET]

```
https://api.cryptoscan.pro?type=arbitrage&variant=dex-cex,cex-dex
```

- [WS] Listen Updates

```
{ "type": "arbitrage", "variant": "cex-futures,futures-cex" }
```

## Dex-Cex Arbitrage

Arbitrage from Decentralized exchanges to Centralized

- [GET]

```
https://api.cryptoscan.pro?type=arbitrage&variant=dex-cex,cex-dex
```

- [WS] Listen Updates

```
{ "type": "arbitrage", "variant": "cex-cex" }
```

## Cex Arbitrage

Arbitrage between Centralized exchanges

- [GET]

```
https://api.cryptoscan.pro?type=arbitrage&variant=cex-cex
```

- [WS] Listen Updates
```
{ "type": "arbitrage", "variant": "cex-cex" }
```

## Dex Arbitrage

Arbitrage between Decentralized exchanges

- [GET]

```
https://api.cryptoscan.pro?type=arbitrage&variant=dex-dex
```

- [WS] Listen Updates

```
{ "type": "arbitrage", "variant": "dex-dex" }
```

## Bridge Arbitrage

- [GET]

```
https://api.cryptoscan.pro?type=arbitrage&variant=dex-bridge
```

- [WS] Listen Updates

```
{ "type": "arbitrage", "variant": "dex-dex" }
```
