# Arbitrage

## Funding Arbitrage

This section covers arbitrage opportunities in centralized exchange (CEX) futures markets, allowing users to exploit price differences between futures contracts.

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

This section describes arbitrage opportunities from decentralized exchanges (DEX) to centralized exchanges (CEX), enabling users to benefit from price discrepancies between these platforms.

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

This section focuses on arbitrage between centralized exchanges, where users can take advantage of price differences across various CEX platforms.

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

This section highlights arbitrage opportunities between decentralized exchanges, allowing users to capitalize on price variations within DEX platforms.

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

This section covers arbitrage opportunities involving cross-chain bridges, where users can exploit price differences between assets on different blockchains.

- [GET]

```
https://api.cryptoscan.pro?type=arbitrage&variant=dex-bridge
```

- [WS] Listen Updates

```
{ "type": "arbitrage", "variant": "dex-dex" }
```
