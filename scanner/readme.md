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
https://api.cryptoscan.pro/v1/rate?to=sol&from=usdc
```

Request

- `to` - coin address to get price
- `from` - base coin address (Default: usdt)
- `amount` - amount of base coin (Deafult: 1)

Response 

List of `Rate`

- `Rate`
    - `contractFrom` - contract of the base coin address
    - `contractTo` - contract of the quote coin address
    - `base` - base coin symbol
    - `quote` - quote coin symbol
    - `price` - price of the pair
    - `priceUSD` - price of the coin in USD
    - `result` - amount of quote tokens to pay
    - `resultUSD` - amount of quote tokens to pay in USD
    - `fee` - fee
    - `feeUSD` - fee in USD
    - `service` - exchange or platform to buy
    - `impact` - price impact

## Listen transactions

```
ws://api.cryptoscan.pro/v1/transactions
```

Request

- `address` - address of the coin

Response

- `tx` - tx hash id of transaction
- `sol` - amount of solana in transaction
- `amount` - amount of tokens in transaction
- `owner` - owner address of transaction
- `mint` - coin address
- `createdDate` - creation date of transaction

## Toolkit

- [Typescript SDK](https://github.com/cryptoscan-pro/scanner-sdk)
