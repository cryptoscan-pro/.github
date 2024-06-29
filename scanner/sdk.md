# @cryptoscan/scanner-sdk

The easiest way to get dynamic swap/exchange rates by CEX and DEX tokens;

[[GitHub]](https://github.com/cryptoscan-pro/scanner-sdk)
[[Our website]](https://cryptoscan.pro/)
[[Docs]](https://docs.cryptoscan.pro/)
[[Discord]](https://discord.gg/ktewAs67fE)

To install package:

```
npm install @cryptoscan/scanner-sdk
```

Usage example:

```javascript
import { getPrice, getRates, getRate } from '@cryptoscan/scanner-sdk';

const from = 'USDC';
const to = 'SOL';

async function load() {
  const price = await getPrice(to, from); // 145.3
  const amount = await getPrice(to, from, 10); // 1453
  const rates = await getRate(to, from) // Array of rates
  const rate = await getRate(to, from) // The first rate
}

load()
```

## Docs

- `getPrice(to: string, from: string, amount: number): Promise<number>`
- `getRates(to: string, from: string): Promise<Rate[]>`
- `getRate(to: string, from: string): Promise<Rate>`
- `listenTransactions(network: string, fromAddress: string, onTransaction: (t: Transaction) => void, toAddress?: string): Promise<Rate>`
    - `Transaction`
        - `tx` - transaction hash
        - `baseAmount` - amount of base coin
        - `quoteAmount` - amount of quote coin
        - `amount` - amount of base coin
    

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

## Contribute

```bash
bun install
```

To run:

```bash
bun run lib/index.ts
```

This project was created using `bun init` in bun v1.1.0. [Bun](https://bun.sh) is a fast all-in-one JavaScript runtime.
