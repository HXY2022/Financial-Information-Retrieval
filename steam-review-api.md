# Steam review API

```python
import ast
import requests
import json
from bs4 import BeautifulSoup
import pandas as pd



def GetReviewOfGameId(id,filter='all',language='english',day_range=626.75,cursor='*',review_type='all',purchase_type='all',num_per_page=20):
    prefix = 'https://store.steampowered.com/appreviews/'
    res = requests.get(prefix+str(id),params={'json':1,'filter':filter,'language':language,'day_range':day_range,
    'cursor':cursor,'review_type':review_type,'purchase_type':purchase_type,'num_per_page':num_per_page}) #,
    if res.status_code == 200:
        return res.json()
    else:
        return None
```

```python
arr = []
cursor = '*'
for i in range(0,100):
    review = GetReviewOfGameId(271590,cursor=cursor,num_per_page=100)
    cursor = review['cursor']
    arr += review['reviews']
    if review['success'] != 1:
        print(review)
        break
    if review['query_summary']['num_reviews'] != 100:
        break
    print('Review Count: '+str(len(arr)))

abc = []
# print(len(arr))
for x in range (0,13000):
    if x >10000:
        abc.append ([arr[x]['review']])
    # print(x,'条评论\n',arr[x]['review'])
    #print(type(arr[x]['review']))


bcd = str(abc)

file = open('第三.txt','w', encoding="utf-8")
file.write(bcd)

file.close()

```
