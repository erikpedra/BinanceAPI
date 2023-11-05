# BinanceAPI

# Sosial Media
Telegram : https://t.me/minsanztuy        
Website    : https://autotradevip.com/en/  
Olmyptrade : https://youtu.be/zTZT7zDlmtU  
Binomo     : https://youtu.be/ww9rVMX5TK4  
IQ Option  : https://youtu.be/4i3YUEDRGWY  
Quotex     : https://www.youtube.com/channel/UCCqnm8XHUoc0Ude78RJwmoA  
Expert Option     : https://www.youtube.com/channel/UCCqnm8XHUoc0Ude78RJwmoA

### Debug Mode ON
```python
import logging
logging.basicConfig(level=logging.DEBUG,format='%(asctime)s %(message)s')
```

### Import
```python
from binanceapi  import Binance
```

### Login by apikey and secretkey
if connect sucess return True,None  
if connect fail return False,reason  
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
print(check,message)
```

### Get Account
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_Account()
    print(result)
```

### Get Symbol
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_symbol()
    print(result)
```

### Get Market Depth
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_Depth('ETHBTC', limit=10)
    print(result)
```

### get_AggTrades
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_Trades('ETHBTC', limit=1)) #symbol: str, fromId, startTime, endTime, limit
    print(result)
```

### get_Ticker24HR
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_Ticker24HR('BTCUSDT') #symbol: str
    print(result)
```

### get_TickerPrice
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_TickerPrice('BTCUSDT') #symbol: str
    print(result)
```

### get_BookTicker
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_BookTicker('BTCUSDT') #symbol: str
    print(result)
```

### get_newOrder
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    #orderTypes  ['LIMIT', 'LIMIT_MAKER', 'MARKET', 'STOP_LOSS_LIMIT', 'TAKE_PROFIT_LIMIT']
    data, result = account.get_newOrder('BTCUSDT') ##symbol: str, BUY/SELL, LIMIT/MARKET. PRICE, Quantity,  GTC/IOC
    print(result)
```
### get_Order
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.cancelOrder('BTCUSDT', '1231231') 
    print(result)
```
### cancelOrder
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.cancelOrder('BTCUSDT', '123456789') 
    print(result)
```

### get_OpenOrders
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_OpenOrders('BTCUSDT') 
    print(result)
```

### Get_AllOrders
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.Get_AllOrders('BTCUSDT') #symbol: str , orderId: int, limit: int
    print(result)
```

### get_MyTrades
```python
from binanceapi import Binance
account=Binance(host="binance.com",apikey="x",secretKey="x")
check,message=account.connect()
if check:
    data, result = account.get_MyTrades('BTCUSDT') #symbol: str , orderId: int, limit: int
    print(result)
```
