# API

You can get data from

```
https://api.cryptoscan.pro
```

or listen data by WebSocket

```
ws://api.cryptoscan.pro/listen
```

## Sort data

- `asc` - Ascending (from low to high)
- `desc` - Descending (from high to low)

```
https://api.cryptoscan.pro?type=arbitrage&sort[spread]=asc
```

## Filter data

- `minParam` - Minimal number value to filter
- `maxParam` - Maximal number value to filter
- `param` - Filter string

```
https://api.cryptoscan.pro?type=cex&minVolume=100000
```

## Get Types column

You can show all unique columns by slicing. Put slice=type into the url
to get all types in the api.

```
https://api.cryptoscan.pro?slice=type
```

## Get column values

You can select all unique values of a column and check it in the
{"data": [], "slice": { DATA OBJECT }}

```
https://api.cryptoscan.pro?slice=exchange
```

## Group by values

If you found a many duplicates of column, you can group data by column.

```
https://api.cryptoscan.pro?groupBy=exchange
```
