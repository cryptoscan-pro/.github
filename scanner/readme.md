# Cryptoscan - Scanner API

## Why use this API?

- No delay price updates
- Integration with many DEXes/CEXes
- Easy to use

## Example

```
curl -l "https://api.cryptoscan.pro/v1/rate?to=29Q7c3kh1X9bdxYiNM3UpVsDMsH4sMyoYnnxgwmWGugD&from=sol&amount=1"
```

## Get price

```
curl -l "https://api.cryptoscan.pro/v1/rate?to=sol"
```

Request

- `to` - coin address to get price
- `from` - base coin address (Default: usdt)
- `amount` - amount of base coin (Deafult: 1)

## Toolkit

- [Typescript SDK](https://github.com/cryptoscan-pro/scanner-sdk)
