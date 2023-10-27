
# gap detector

gap detector merupakan refrensi saham yang mempunyai gap pada **_orderbook_** **_BUY_** dan **_SELL_** bedasarkan fraksi harga.

untuk memahami fraksi harga silahkan menuju tautan berikut :
[https://snips.stockbit.com/investasi/pengertian-fraksi-harga-saham](https://snips.stockbit.com/investasi/pengertian-fraksi-harga-saham)

**CONTOH ORDERBOOK**
| | | |||
| --- | --- |--- |--- | --- |
| Buy price | Buy lot | |Sell price| Sell lot
| 1540| 2769 ||1550|3000
| 15435| 1000||1555|3100
|15425| 1020||1565|100
|15415| 3000||1570|652
||||1575|10000
|| ||1580|8987

Dari contoh Orderbook dapat dilihat terdapat kekosongan selisih harga antara **_BUY_** dan **_SELL_** dimana untuk rentang harga antara 500 - 2000 jumlah penambahan dan pengurangannya diangka 5 , yang saya sebut gap harga orderbook.

anda bisa melihat summary dari data saham yang terdapat gap .

untuk keterangan meta data yang terdapat pada file  **gap_data.json** sebagai berikut :

       [
          {
            code: 'IDX:CODE',
            TBuyAvg: 39645,
            TSellAvg: 5782,
            BuyLength: 3,
            SellLength: 10,
            fraksi: 5,
            BuyInvalid: true,
            SellInvalid: false,
            BothInvalid: false
          }
          ..........
    ]

code : merupakan IDX:CODE yang diperdagangkan di BEI.

TBuyAvg : merupakan nilai rata-rata lot yang terdapat pada BUY slide.

TSellAvg : merupakan nilai rata-rata lot yang terdapat pada SELL slide.

BuyLength : merupakan banyaknya variasi harga penawaran pada BUY slide.

SellLength: merupakan banyaknya variasi harga penawaran pada SELL slide.

fraksi: merupakan nilai fraksi harga.


BuyInvalid : bernilai TRUE jika terdapat gap pada BUY slide.

SellInvalid: bernilai TRUE jika terdapat gap pada SELL slide.

BothInvalid : bernilai TRUE jika terdapat gap pada paris pertama di BUY dan SELL slide.
