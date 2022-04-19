# Steam Websipder 2018

```python
import json
from bs4 import BeautifulSoup
import pandas as pd

res = r.get('https://store.steampowered.com/sale/2018_so_far_top_sellers/')

if res.status_code == 200:
    soup = BeautifulSoup(res.text, 'html.parser')
    config = soup.find_all('div',{'class' : 'item'}) 

    for app in config:
         print('\tappid: '+str(app['data-ds-appid']))

```
