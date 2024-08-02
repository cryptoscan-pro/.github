# @cryptoscan/scanner-sdk

The easiest way to get dynamic swap/exchange rates by CEX and DEX tokens

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

const network = 'solana';
const from = 'USDC';
const to = 'SOL';

async function load() {
  const price = await getPrice(network, to, from); // 145.3
  const amount = await getPrice(network, to, from, 10); // 1453
  const rates = await getRate(network, to, from) // Array of @Rate
  const rate = await getRate(network, to, from) // The first @Rate
}

load()
```

## Docs

- `getPrice(network: string, to: string, from: string, amount: number): Promise<number>`
- `getRates(network: string, to: string, from: string): Promise<Rate[]>`
- `getRate(network: string, to: string, from: string): Promise<Rate>`
- `listenTransactions(network: string, fromAddress: string, onTransaction: (t: Transaction) => void, toAddress?: string): () => void`
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
