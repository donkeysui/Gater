# Gater

Used for get Gate.IO high frequency data.

```{python}
<< import Gater
<< Gater.how()
>>  5 - 7 params:
    biz     ->       spot futures_btc futures_usdt
    market  ->       BTC_USDT ....
    type    ->       trades/deals mark_prices candlesticks_10s funding_applies
                    funding_updates orderbooks
    year    ->       2021
    month   ->       11
    day     ->       17 (only in orderbooks)
    hour    ->       15 (only in orderbooks)
<< Gater.get('futures_btc', "BTC_USD", "orderbooks", "2023", "02", "11", "0")
>>           timestamp action    price   size     orderid  merged_count
            0      1.676074e+09    set   3600.6      5  3970101842             0
            1      1.676074e+09    set   3800.6      5  3970101842             0
            2      1.676074e+09    set   5000.0     11  3970101842             0
            3      1.676074e+09    set   5369.4     10  3970101842             0
            4      1.676074e+09    set   5500.0      1  3970101842             0
            ...             ...    ...      ...    ...         ...           ...
            51176  1.676077e+09   make  21657.9  -2000  3970152308             1
            51177  1.676077e+09   take  21658.0 -12972  3970152309             1
            51178  1.676077e+09   make  21657.8 -12972  3970152310             1
            51179  1.676077e+09   make  21696.4   -751  3970152311             1
            51180  1.676077e+09   make  21673.6   -750  3970152312             1

            [51181 rows x 6 columns]
```



