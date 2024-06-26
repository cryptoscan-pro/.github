# [Get] Network

```
https://api.cryptoscan.pro/v1/networks/{networkId}
```

## Request

- `coin` - Coin name, ticker or contract

```
{
  coin?: string;
}
```

## Response

- `id` - Network ID
- `name` - Network name
- `fullName` - Network full name
- `aliases` - Network aliases
- `exchanges` - Exchanges statuses, includes with `coin` param

```
{
  id: number;
  name: string;
  fullName: string;
  aliases: string[];
  exchanges?: {
    [exchangeName]: {
      coin: string;
      id: number;
      name: string;
      fullName: string;
      aliases: string[];
      deposit: {
        isEnabled: boolean;
        fee: number;
        percentageFee: number;
        enabledAt: Date;
        disabledAt: Date;
      };
      withdraw: {
        isEnabled: boolean;
        fee: number;
        percentageFee: number;
        enabledAt: Date;
        disabledAt: Date;
      }
    }
  }
}
```

## Example

```
curl -X GET "https://api.cryptoscan.pro/v1/networks"
```
