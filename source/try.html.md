---
title: Member API v2
language_tabs:
  - http: HTTP
  - shell: Curl
  - javascript: JavaScript
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="member-api-v2">Member API v2 v1.8.48</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Member API is API which can be used by client application like SPA.

Base URLs:

* <a href="//api-dev.etorox.io/api">//api-dev.etorox.io/api</a>

License: <a href="https://github.com/rubykube/peatio/blob/master/LICENSE.md">undefined</a>

<h1 id="member-api-v2-markets">markets</h1>

Operations about markets

## getV2Markets

<a id="opIdgetV2Markets"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/markets HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/markets

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/markets',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/markets`

*Get all available markets.*

Get all available markets.

<h3 id="getv2markets-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all available markets.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-tickers">tickers</h1>

Operations about tickers

## getV2TickersMarket

<a id="opIdgetV2TickersMarket"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/tickers/{market} HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/tickers/{market}

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/tickers/{market}',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/tickers/{market}`

*Get ticker of specific market.*

Get ticker of specific market.

<h3 id="getv2tickersmarket-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|path|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|

<h3 id="getv2tickersmarket-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get ticker of specific market.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2Tickers

<a id="opIdgetV2Tickers"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/tickers HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/tickers

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/tickers',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/tickers`

*Get ticker of all markets.*

Get ticker of all markets.

<h3 id="getv2tickers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get ticker of all markets.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-members">members</h1>

Operations about members

## getV2MembersMe

<a id="opIdgetV2MembersMe"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/members/me HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/members/me

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/members/me',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/members/me`

*Get your profile and accounts info.*

Get your profile and accounts info.

<h3 id="getv2membersme-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get your profile and accounts info.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-deposits">deposits</h1>

Operations about deposits

## getV2Deposits

<a id="opIdgetV2Deposits"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/deposits HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/deposits

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/deposits',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/deposits`

*Get your deposits history.*

Get your deposits history.

<h3 id="getv2deposits-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|Currency value contains aud,bch,btc,dash,erc,eth,eur,gold,ltc,terc,usd,xrp,AUD,BCH,BTC,DASH,ERC,ETH,EUR,GOLD,LTC,TERC,USD,XRP|
|limit|query|integer(int32)|false|Set result limit.|
|state|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|currency|aud|
|currency|bch|
|currency|btc|
|currency|dash|
|currency|erc|
|currency|eth|
|currency|eur|
|currency|gold|
|currency|ltc|
|currency|terc|
|currency|usd|
|currency|xrp|
|currency|AUD|
|currency|BCH|
|currency|BTC|
|currency|DASH|
|currency|ERC|
|currency|ETH|
|currency|EUR|
|currency|GOLD|
|currency|LTC|
|currency|TERC|
|currency|USD|
|currency|XRP|
|state|submitted|
|state|canceled|
|state|rejected|
|state|accepted|

<h3 id="getv2deposits-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get your deposits history.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-deposit">deposit</h1>

Operations about deposits

## getV2Deposit

<a id="opIdgetV2Deposit"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/deposit?txid=string HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/deposit?txid=string

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/deposit',
  method: 'get',
  data: '?txid=string',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/deposit`

*Get details of specific deposit.*

Get details of specific deposit.

<h3 id="getv2deposit-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|txid|query|string|true|none|

<h3 id="getv2deposit-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get details of specific deposit.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-deposit_address">deposit_address</h1>

Operations about deposit_addresses

## getV2DepositAddress

<a id="opIdgetV2DepositAddress"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/deposit_address?currency=bch HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/deposit_address?currency=bch

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/deposit_address',
  method: 'get',
  data: '?currency=bch',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/deposit_address`

*Where to deposit. The address field could be empty when a new address
          is generating (e.g. for bitcoin), you should try again later in that case.*

Where to deposit. The address field could be empty when a new address
          is generating (e.g. for bitcoin), you should try again later in that case.

<h3 id="getv2depositaddress-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|true|The account to which you want to deposit. Available values: bch, btc, dash, erc, eth, ltc, terc, xrp, BCH, BTC, DASH, ERC, ETH, LTC, TERC, XRP|

#### Enumerated Values

|Parameter|Value|
|---|---|
|currency|bch|
|currency|btc|
|currency|dash|
|currency|erc|
|currency|eth|
|currency|ltc|
|currency|terc|
|currency|xrp|
|currency|BCH|
|currency|BTC|
|currency|DASH|
|currency|ERC|
|currency|ETH|
|currency|LTC|
|currency|TERC|
|currency|XRP|

<h3 id="getv2depositaddress-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Where to deposit. The address field could be empty when a new address
          is generating (e.g. for bitcoin), you should try again later in that case.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-orders">orders</h1>

Operations about orders

## postV2OrdersClear

<a id="opIdpostV2OrdersClear"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/orders/clear HTTP/1.1

Content-Type: application/x-www-form-urlencoded

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/orders/clear \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```javascript
var headers = {
  'Content-Type':'application/x-www-form-urlencoded'

};

$.ajax({
  url: '/api-dev.etorox.io/api/v2/orders/clear',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/orders/clear`

*Cancel all my orders.*

Cancel all my orders.

> Body parameter

```yaml
side: sell

```

<h3 id="postv2ordersclear-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» side|body|string|false|If present, only sell orders (asks) or buy orders (bids) will be canncelled.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» side|sell|
|» side|buy|

<h3 id="postv2ordersclear-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Cancel all my orders.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2Orders

<a id="opIdpostV2Orders"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/orders HTTP/1.1

Content-Type: application/x-www-form-urlencoded

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/orders \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```javascript
var headers = {
  'Content-Type':'application/x-www-form-urlencoded'

};

$.ajax({
  url: '/api-dev.etorox.io/api/v2/orders',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/orders`

*Create a Sell/Buy order.*

Create a Sell/Buy order.

> Body parameter

```yaml
market: bchbtc
side: sell
volume: string
price: string
ord_type: limit

```

<h3 id="postv2orders-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» market|body|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|» side|body|string|true|Either 'sell' or 'buy'.|
|» volume|body|string|true|The amount user want to sell/buy. An order could be partially executed, e.g. an order sell 5 btc can be matched with a buy 3 btc order, left 2 btc to be sold; in this case the order's volume would be '5.0', its remaining_volume would be '2.0', its executed volume is '3.0'.|
|» price|body|string|false|Price for each unit. e.g. If you want to sell/buy 1 btc at 3000 usd, the price is '3000.0'|
|» ord_type|body|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» market|bchbtc|
|» market|bchusd|
|» market|bchxrp|
|» market|btcaud|
|» market|btcusd|
|» market|btcxrp|
|» market|dashterc|
|» market|ethgold|
|» market|ethterc|
|» market|ltcbch|
|» market|ltcbtc|
|» market|ltcusd|
|» market|ltcxrp|
|» market|xrpusd|
|» side|sell|
|» side|buy|
|» ord_type|market|
|» ord_type|limit|

<h3 id="postv2orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a Sell/Buy order.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2Orders

<a id="opIdgetV2Orders"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/orders?market=bchbtc HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/orders?market=bchbtc

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/orders',
  method: 'get',
  data: '?market=bchbtc',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/orders`

*Get your orders, results is paginated.*

Get your orders, results is paginated.

<h3 id="getv2orders-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|state|query|string|false|Filter order by state, default to 'wait' (active orders).|
|limit|query|integer(int32)|false|Limit the number of returned orders, default to 20.|
|page|query|integer(int32)|false|Specify the page of paginated results.|
|order_by|query|string|false|If set, returned orders will be sorted in specific order, default to 'asc'.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|
|state|wait|
|state|done|
|state|cancel|
|order_by|asc|
|order_by|desc|

<h3 id="getv2orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get your orders, results is paginated.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2OrdersMulti

<a id="opIdpostV2OrdersMulti"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/orders/multi HTTP/1.1

Content-Type: application/x-www-form-urlencoded

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/orders/multi \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```javascript
var headers = {
  'Content-Type':'application/x-www-form-urlencoded'

};

$.ajax({
  url: '/api-dev.etorox.io/api/v2/orders/multi',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/orders/multi`

*Create multiple sell/buy orders.*

Create multiple sell/buy orders.

> Body parameter

```yaml
market: bchbtc
'orders[side]':
  - sell
'orders[volume]':
  - string
'orders[price]':
  - string
'orders[ord_type]':
  - limit

```

<h3 id="postv2ordersmulti-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» market|body|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|» orders[side]|body|[string]|true|Either 'sell' or 'buy'.|
|» orders[volume]|body|[string]|true|The amount user want to sell/buy. An order could be partially executed, e.g. an order sell 5 btc can be matched with a buy 3 btc order, left 2 btc to be sold; in this case the order's volume would be '5.0', its remaining_volume would be '2.0', its executed volume is '3.0'.|
|» orders[price]|body|[string]|false|Price for each unit. e.g. If you want to sell/buy 1 btc at 3000 usd, the price is '3000.0'|
|» orders[ord_type]|body|[string]|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» market|bchbtc|
|» market|bchusd|
|» market|bchxrp|
|» market|btcaud|
|» market|btcusd|
|» market|btcxrp|
|» market|dashterc|
|» market|ethgold|
|» market|ethterc|
|» market|ltcbch|
|» market|ltcbtc|
|» market|ltcusd|
|» market|ltcxrp|
|» market|xrpusd|
|» orders[side]|sell|
|» orders[side]|buy|
|» orders[ord_type]|market|
|» orders[ord_type]|limit|

<h3 id="postv2ordersmulti-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create multiple sell/buy orders.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-order">order</h1>

Operations about orders

## postV2OrderDelete

<a id="opIdpostV2OrderDelete"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/order/delete HTTP/1.1

Content-Type: application/x-www-form-urlencoded

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/order/delete \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```javascript
var headers = {
  'Content-Type':'application/x-www-form-urlencoded'

};

$.ajax({
  url: '/api-dev.etorox.io/api/v2/order/delete',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/order/delete`

*Cancel an order.*

Cancel an order.

> Body parameter

```yaml
id: string

```

<h3 id="postv2orderdelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» id|body|string|true|Unique order id.|

<h3 id="postv2orderdelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Cancel an order.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2Order

<a id="opIdgetV2Order"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/order?id=string HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/order?id=string

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/order',
  method: 'get',
  data: '?id=string',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/order`

*Get information of specified order.*

Get information of specified order.

<h3 id="getv2order-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|string|true|Unique order id.|

<h3 id="getv2order-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get information of specified order.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-order_book">order_book</h1>

Operations about order_books

## getV2OrderBook

<a id="opIdgetV2OrderBook"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/order_book?market=bchbtc HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/order_book?market=bchbtc

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/order_book',
  method: 'get',
  data: '?market=bchbtc',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/order_book`

*Get the order book of specified market.*

Get the order book of specified market.

<h3 id="getv2orderbook-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|asks_limit|query|integer(int32)|false|Limit the number of returned sell orders. Default to 20.|
|bids_limit|query|integer(int32)|false|Limit the number of returned buy orders. Default to 20.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|

<h3 id="getv2orderbook-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the order book of specified market.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-depth">depth</h1>

Operations about depths

## getV2Depth

<a id="opIdgetV2Depth"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/depth?market=bchbtc HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/depth?market=bchbtc

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/depth',
  method: 'get',
  data: '?market=bchbtc',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/depth`

*Get depth or specified market. Both asks and bids are sorted from highest price to lowest.*

Get depth or specified market. Both asks and bids are sorted from highest price to lowest.

<h3 id="getv2depth-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|limit|query|integer(int32)|false|Limit the number of returned price levels. Default to 300.|
|use_cache|query|boolean|false|Use cached version of depth|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|

<h3 id="getv2depth-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get depth or specified market. Both asks and bids are sorted from highest price to lowest.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-trades">trades</h1>

Operations about trades

## getV2TradesMy

<a id="opIdgetV2TradesMy"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/trades/my?market=bchbtc HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/trades/my?market=bchbtc

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/trades/my',
  method: 'get',
  data: '?market=bchbtc',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/trades/my`

*Get your executed trades. Trades are sorted in reverse creation order.*

Get your executed trades. Trades are sorted in reverse creation order.

<h3 id="getv2tradesmy-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|limit|query|integer(int32)|false|Limit the number of returned trades. Default to 50.|
|timestamp|query|integer(int32)|false|An integer represents the seconds elapsed since Unix epoch. If set, only trades executed before the time will be returned.|
|from|query|integer(int32)|false|Trade id. If set, only trades created after the trade will be returned.|
|to|query|integer(int32)|false|Trade id. If set, only trades created before the trade will be returned.|
|order_by|query|string|false|If set, returned trades will be sorted in specific order, default to 'desc'.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|
|order_by|asc|
|order_by|desc|

<h3 id="getv2tradesmy-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get your executed trades. Trades are sorted in reverse creation order.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2Trades

<a id="opIdgetV2Trades"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/trades?market=bchbtc HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/trades?market=bchbtc

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/trades',
  method: 'get',
  data: '?market=bchbtc',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/trades`

*Get recent trades on market, each trade is included only once. Trades are sorted in reverse creation order.*

Get recent trades on market, each trade is included only once. Trades are sorted in reverse creation order.

<h3 id="getv2trades-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|limit|query|integer(int32)|false|Limit the number of returned trades. Default to 50.|
|timestamp|query|integer(int32)|false|An integer represents the seconds elapsed since Unix epoch. If set, only trades executed before the time will be returned.|
|from|query|integer(int32)|false|Trade id. If set, only trades created after the trade will be returned.|
|to|query|integer(int32)|false|Trade id. If set, only trades created before the trade will be returned.|
|order_by|query|string|false|If set, returned trades will be sorted in specific order, default to 'desc'.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|
|order_by|asc|
|order_by|desc|

<h3 id="getv2trades-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get recent trades on market, each trade is included only once. Trades are sorted in reverse creation order.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-k">k</h1>

Operations about ks

## getV2K

<a id="opIdgetV2K"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/k?market=bchbtc HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/k?market=bchbtc

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/k',
  method: 'get',
  data: '?market=bchbtc',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/k`

*Get OHLC(k line) of specific market.*

Get OHLC(k line) of specific market.

<h3 id="getv2k-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|limit|query|integer(int32)|false|Limit the number of returned data points, default to 30.|
|period|query|integer(int32)|false|Time period of K line, default to 1. You can choose between 1, 5, 15, 30, 60, 120, 240, 360, 720, 1440, 4320, 10080|
|timestamp|query|integer(int32)|false|An integer represents the seconds elapsed since Unix epoch. If set, only k-line data after that time will be returned.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|
|period|1|
|period|5|
|period|15|
|period|30|
|period|60|
|period|120|
|period|240|
|period|360|
|period|720|
|period|1440|
|period|4320|
|period|10080|

<h3 id="getv2k-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get OHLC(k line) of specific market.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-k_with_pending_trades">k_with_pending_trades</h1>

Operations about k_with_pending_trades

## getV2KWithPendingTrades

<a id="opIdgetV2KWithPendingTrades"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/k_with_pending_trades?market=bchbtc&trade_id=0 HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/k_with_pending_trades?market=bchbtc&trade_id=0

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/k_with_pending_trades',
  method: 'get',
  data: '?market=bchbtc&trade_id=0',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/k_with_pending_trades`

*Get K data with pending trades, which are the trades not included in K data yet, because there's delay between trade generated and processed by K data generator.*

Get K data with pending trades, which are the trades not included in K data yet, because there's delay between trade generated and processed by K data generator.

<h3 id="getv2kwithpendingtrades-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|trade_id|query|integer(int32)|true|The trade id of the first trade you received.|
|limit|query|integer(int32)|false|Limit the number of returned data points, default to 30.|
|period|query|integer(int32)|false|Time period of K line, default to 1. You can choose between 1, 5, 15, 30, 60, 120, 240, 360, 720, 1440, 4320, 10080|
|timestamp|query|integer(int32)|false|An integer represents the seconds elapsed since Unix epoch. If set, only k-line data after that time will be returned.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|
|period|1|
|period|5|
|period|15|
|period|30|
|period|60|
|period|120|
|period|240|
|period|360|
|period|720|
|period|1440|
|period|4320|
|period|10080|

<h3 id="getv2kwithpendingtrades-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get K data with pending trades, which are the trades not included in K data yet, because there's delay between trade generated and processed by K data generator.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-timestamp">timestamp</h1>

Operations about timestamps

## getV2Timestamp

<a id="opIdgetV2Timestamp"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/timestamp HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/timestamp

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/timestamp',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/timestamp`

*Get server current time, in seconds since Unix epoch.*

Get server current time, in seconds since Unix epoch.

<h3 id="getv2timestamp-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get server current time, in seconds since Unix epoch.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-bootstrap">bootstrap</h1>

Operations about bootstraps

## getV2Bootstrap

<a id="opIdgetV2Bootstrap"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/bootstrap HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/bootstrap

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/bootstrap',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/bootstrap`

*Get bootstrap settings*

Get bootstrap settings

<h3 id="getv2bootstrap-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get bootstrap settings|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-withdraws">withdraws</h1>

Operations about withdraws

## postV2Withdraws

<a id="opIdpostV2Withdraws"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/withdraws HTTP/1.1

Content-Type: application/x-www-form-urlencoded

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/withdraws \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```javascript
var headers = {
  'Content-Type':'application/x-www-form-urlencoded'

};

$.ajax({
  url: '/api-dev.etorox.io/api/v2/withdraws',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/withdraws`

*Create a new withdraw request.*

Create a new withdraw request.

> Body parameter

```yaml
rid: string
currency: string
sum: string

```

<h3 id="postv2withdraws-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» rid|body|string|true|none|
|» currency|body|string|true|Any supported currencies: aud,bch,btc,dash,erc,eth,eur,gold,ltc,terc,usd,xrp,AUD,BCH,BTC,DASH,ERC,ETH,EUR,GOLD,LTC,TERC,USD,XRP.|
|» sum|body|string|true|none|

<h3 id="postv2withdraws-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a new withdraw request.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2Withdraws

<a id="opIdgetV2Withdraws"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/withdraws HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/withdraws

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/withdraws',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/withdraws`

*List your withdraws as paginated collection.*

List your withdraws as paginated collection.

<h3 id="getv2withdraws-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|Any supported currencies: aud,bch,btc,dash,erc,eth,eur,gold,ltc,terc,usd,xrp,AUD,BCH,BTC,DASH,ERC,ETH,EUR,GOLD,LTC,TERC,USD,XRP.|
|page|query|integer(int32)|false|Page number (defaults to 1).|
|limit|query|integer(int32)|false|Number of withdraws per page (defaults to 100, maximum is 1000).|

#### Enumerated Values

|Parameter|Value|
|---|---|
|currency|aud|
|currency|bch|
|currency|btc|
|currency|dash|
|currency|erc|
|currency|eth|
|currency|eur|
|currency|gold|
|currency|ltc|
|currency|terc|
|currency|usd|
|currency|xrp|
|currency|AUD|
|currency|BCH|
|currency|BTC|
|currency|DASH|
|currency|ERC|
|currency|ETH|
|currency|EUR|
|currency|GOLD|
|currency|LTC|
|currency|TERC|
|currency|USD|
|currency|XRP|

<h3 id="getv2withdraws-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List your withdraws as paginated collection.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-withdraw">withdraw</h1>

Operations about withdraws

## postV2WithdrawDelete

<a id="opIdpostV2WithdrawDelete"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/withdraw/delete HTTP/1.1

Content-Type: application/x-www-form-urlencoded

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/withdraw/delete \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```javascript
var headers = {
  'Content-Type':'application/x-www-form-urlencoded'

};

$.ajax({
  url: '/api-dev.etorox.io/api/v2/withdraw/delete',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/withdraw/delete`

*Cancel a withdraw request.*

Cancel a withdraw request.

> Body parameter

```yaml
id: 0

```

<h3 id="postv2withdrawdelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» id|body|integer(int32)|true|none|

<h3 id="postv2withdrawdelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Cancel a withdraw request.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-sessions">sessions</h1>

Operations about sessions

## deleteV2Sessions

<a id="opIddeleteV2Sessions"></a>

> Code samples

```http
DELETE /api-dev.etorox.io/api/v2/sessions HTTP/1.1

```

```shell
# You can also use wget
curl -X DELETE /api-dev.etorox.io/api/v2/sessions

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/sessions',
  method: 'delete',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`DELETE /v2/sessions`

*Delete all user sessions.*

Delete all user sessions.

<h3 id="deletev2sessions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Delete all user sessions.|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2Sessions

<a id="opIdpostV2Sessions"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/sessions HTTP/1.1

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/sessions

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/sessions',
  method: 'post',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/sessions`

*Create new user session.*

Create new user session.

<h3 id="postv2sessions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create new user session.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-solvency">solvency</h1>

Operations about solvencies

## getV2SolvencyLiabilityProofsPartialTreeMine

<a id="opIdgetV2SolvencyLiabilityProofsPartialTreeMine"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/solvency/liability_proofs/partial_tree/mine?currency=bch HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/solvency/liability_proofs/partial_tree/mine?currency=bch

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/solvency/liability_proofs/partial_tree/mine',
  method: 'get',
  data: '?currency=bch',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/solvency/liability_proofs/partial_tree/mine`

*Returns newest partial tree record for member account of specified currency.*

Returns newest partial tree record for member account of specified currency.

<h3 id="getv2solvencyliabilityproofspartialtreemine-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|true|The code of any currency with type 'coin'.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|currency|bch|
|currency|btc|
|currency|dash|
|currency|erc|
|currency|eth|
|currency|ltc|
|currency|terc|
|currency|xrp|
|currency|BCH|
|currency|BTC|
|currency|DASH|
|currency|ERC|
|currency|ETH|
|currency|LTC|
|currency|TERC|
|currency|XRP|

<h3 id="getv2solvencyliabilityproofspartialtreemine-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns newest partial tree record for member account of specified currency.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2SolvencyLiabilityProofsLatest

<a id="opIdgetV2SolvencyLiabilityProofsLatest"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/solvency/liability_proofs/latest?currency=bch HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/solvency/liability_proofs/latest?currency=bch

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/solvency/liability_proofs/latest',
  method: 'get',
  data: '?currency=bch',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/solvency/liability_proofs/latest`

*Returns newest liability proof record for given currency.*

Returns newest liability proof record for given currency.

<h3 id="getv2solvencyliabilityproofslatest-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|true|The code of any currency with type 'coin'.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|currency|bch|
|currency|btc|
|currency|dash|
|currency|erc|
|currency|eth|
|currency|ltc|
|currency|terc|
|currency|xrp|
|currency|BCH|
|currency|BTC|
|currency|DASH|
|currency|ERC|
|currency|ETH|
|currency|LTC|
|currency|TERC|
|currency|XRP|

<h3 id="getv2solvencyliabilityproofslatest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns newest liability proof record for given currency.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-fees">fees</h1>

Operations about fees

## getV2FeesTrading

<a id="opIdgetV2FeesTrading"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/fees/trading HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/fees/trading

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/fees/trading',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/fees/trading`

*Returns trading fees for markets.*

Returns trading fees for markets.

<h3 id="getv2feestrading-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns trading fees for markets.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2FeesDeposit

<a id="opIdgetV2FeesDeposit"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/fees/deposit HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/fees/deposit

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/fees/deposit',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/fees/deposit`

*Returns deposit fees for currencies.*

Returns deposit fees for currencies.

<h3 id="getv2feesdeposit-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns deposit fees for currencies.|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2FeesWithdraw

<a id="opIdgetV2FeesWithdraw"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/fees/withdraw HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/fees/withdraw

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/fees/withdraw',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/fees/withdraw`

*Returns withdraw fees for currencies.*

Returns withdraw fees for currencies.

<h3 id="getv2feeswithdraw-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns withdraw fees for currencies.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-pusher">pusher</h1>

Operations about pushers

## postV2PusherAuth

<a id="opIdpostV2PusherAuth"></a>

> Code samples

```http
POST /api-dev.etorox.io/api/v2/pusher/auth HTTP/1.1

Content-Type: application/x-www-form-urlencoded

```

```shell
# You can also use wget
curl -X POST /api-dev.etorox.io/api/v2/pusher/auth \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```javascript
var headers = {
  'Content-Type':'application/x-www-form-urlencoded'

};

$.ajax({
  url: '/api-dev.etorox.io/api/v2/pusher/auth',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`POST /v2/pusher/auth`

*Returns the credentials used to subscribe to private Pusher channel. IMPORTANT: Pusher events are not part of Peatio public interface. The events may be changed or removed in further releases. Use this on your own risk.*

Returns the credentials used to subscribe to private Pusher channel. IMPORTANT: Pusher events are not part of Peatio public interface. The events may be changed or removed in further releases. Use this on your own risk.

> Body parameter

```yaml
channel_name: string
socket_id: string

```

<h3 id="postv2pusherauth-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» channel_name|body|string|true|The name of the channel being subscribed to. Example: private-SN362ECB6F7D.|
|» socket_id|body|string|true|An unique identifier for the connected client.|

<h3 id="postv2pusherauth-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Returns the credentials used to subscribe to private Pusher channel. IMPORTANT: Pusher events are not part of Peatio public interface. The events may be changed or removed in further releases. Use this on your own risk.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-member_levels">member_levels</h1>

Operations about member_levels

## getV2MemberLevels

<a id="opIdgetV2MemberLevels"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/member_levels HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/member_levels

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/member_levels',
  method: 'get',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/member_levels`

*Returns list of member levels and the privileges they provide.*

Returns list of member levels and the privileges they provide.

<h3 id="getv2memberlevels-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns list of member levels and the privileges they provide.|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-currency">currency</h1>

Operations about currencies

## getV2CurrencyTrades

<a id="opIdgetV2CurrencyTrades"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/currency/trades?currency=aud HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/currency/trades?currency=aud

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/currency/trades',
  method: 'get',
  data: '?currency=aud',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/currency/trades`

*Get currency trades at last 24h*

Get currency trades at last 24h

<h3 id="getv2currencytrades-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|true|Available values: bch, btc, dash, erc, eth, ltc, terc, xrp, BCH, BTC, DASH, ERC, ETH, LTC, TERC, XRP|

#### Enumerated Values

|Parameter|Value|
|---|---|
|currency|aud|
|currency|bch|
|currency|btc|
|currency|dash|
|currency|erc|
|currency|eth|
|currency|eur|
|currency|gold|
|currency|ltc|
|currency|terc|
|currency|usd|
|currency|xrp|
|currency|AUD|
|currency|BCH|
|currency|BTC|
|currency|DASH|
|currency|ERC|
|currency|ETH|
|currency|EUR|
|currency|GOLD|
|currency|LTC|
|currency|TERC|
|currency|USD|
|currency|XRP|

<h3 id="getv2currencytrades-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get currency trades at last 24h|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="member-api-v2-history">history</h1>

Operations about histories

## getV2HistoryOrders

<a id="opIdgetV2HistoryOrders"></a>

> Code samples

```http
GET /api-dev.etorox.io/api/v2/history/orders?market=bchbtc HTTP/1.1

```

```shell
# You can also use wget
curl -X GET /api-dev.etorox.io/api/v2/history/orders?market=bchbtc

```

```javascript

$.ajax({
  url: '/api-dev.etorox.io/api/v2/history/orders',
  method: 'get',
  data: '?market=bchbtc',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /v2/history/orders`

*Get your orders history, results is paginated.*

Get your orders history, results is paginated.

<h3 id="getv2historyorders-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|market|query|string|true|Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btcusd'. All available markets can be found at /api/v2/markets.|
|state|query|string|false|Filter order by state, default to 'wait' (active orders).|
|limit|query|integer(int32)|false|Limit the number of returned orders, default to 100.|
|page|query|integer(int32)|false|Specify the page of paginated results.|
|order_by|query|string|false|If set, returned orders will be sorted in specific order, default to 'asc'.|
|start|query|string(date-time)|false|Created from date|
|end|query|string(date-time)|false|Created up to date|
|price_from|query|number(double)|false|From Price|
|price_to|query|number(double)|false|Up To Price|
|volume_from|query|number(double)|false|From volume|
|volume_to|query|number(double)|false|Up To volume|

#### Enumerated Values

|Parameter|Value|
|---|---|
|market|bchbtc|
|market|bchusd|
|market|bchxrp|
|market|btcaud|
|market|btcusd|
|market|btcxrp|
|market|dashterc|
|market|ethgold|
|market|ethterc|
|market|ltcbch|
|market|ltcbtc|
|market|ltcusd|
|market|ltcxrp|
|market|xrpusd|
|state|wait|
|state|done|
|state|cancel|
|order_by|asc|
|order_by|desc|

<h3 id="getv2historyorders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get your orders history, results is paginated.|None|

<aside class="success">
This operation does not require authentication
</aside>

<script type="application/ld+json">
{
  "@context": "http://schema.org/",
  "@type": "WebAPI",
  "description": "Member API is API which can be used by client application like SPA.",
  
  
  
  "name": "Member API v2"
}
</script>

