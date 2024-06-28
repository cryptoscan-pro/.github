# Cryptoscan - Swap API

## Why use this API?

We have no delays, as soon as a token is released you will be able to trade it using our API.

## Example

```
curl -l "https://api.cryptoscan.pro/v1/swap?walletAddress=DggKFxSoev2xJfMeb1CvgXZ8BsDUXb54bhFtaVMUT9nU&from=sol&to=HJAoYbnsf16Z8ftk3SsuShKLQQgzmxAPu41RTpjjpump&amount=0.05"
```

## Swap

```
https://api.cryptoscan.pro/v1/swap
```

Request

- `walletAddress` - Wallet address
- `from` - Coin address to pay (Defaults: `sol`)
- `to` - Coin address to buy
- `amount` - Amount of Coin `from` to buy

## Create transaction

```
https://api.cryptoscan.pro/v1/createTransaction
```

Request

- `payerAddress` - Wallet address to pay fee
- `instructions` - Instructions for swap
    - *Buy instruction*
      - `type` - buy
      - `service` - exchange name to buy (ex: pumpfun)
      - `coinAddress` - Coin address to buy
      - `walletAddress` - Wallet address
      - `sol` - Amount of Coin `from` to buy
      - `slippage` - Slippage
    - *Sell instruction*
      - `type` - sell
      - `service` - exchange name to sell (ex: pumpfun)
      - `coinAddress` - Coin address to sell
      - `walletAddress` - Wallet address
      - `sol` - (optional) Amount of Coin `from` to sell, if empty - all amount
    - *Transfer instruction*
      - `type` - transfer
      - `fromAddress` - Coin address to pay
      - `toAddress` - Coin address to buy
      - `sol` - (Optional) Amount of Coin `from` to buy, if empty - all amount
      - `coinAddress` - (Optional) address of coin to transfer
    - *Create account instruction*
      - `type` - createAccount
      - `coinAddress` - Coin address to create
      - `walletAddress` - Wallet address
      - `payerAddress` - Wallet address to pay fee
    - *Close account instruction*
      - `type` - closeAccount
      - `coinAddress` - Coin address to close
      - `walletAddress` - Wallet address

## We supports

**Launchpads**

- [x] Pump.fun

**Aggregators**

- [ ] Cowswap
- [ ] Kyberswap
- [ ] Matcha / 0X
- [ ] Odos
- [ ] 1inch
- [ ] Paraswap
- [ ] Sushiswap

**Dexes**

- [ ] Raydium
- [ ] Jupiter
- [ ] Uniswap (V2/V3)

## Toolkit

- [Typescript SDK](https://github.com/cryptoscan-pro/swap-sdk)
- [Solana Send Transaction SDK](https://github.com/cryptoscan-pro/solana-send-transaction)
- [Solana Wallet SDK](https://github.com/cryptoscan-pro/solana-wallet-sdk)
