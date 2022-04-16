# Reddit API



```
import requests
import jsonpath

'''reddit official api method
client_id='55vVoa0UQ4hFaB2xp6Qliw'
secret_key='o_NM8lXya7AIvvS6BMYc_R9EshNYaQ'

auth = requests.auth.HTTPBasicAuth(client_id,secret_key) #创建的key
data ={
    'grant_type':'password',
    'username':'xbw199942',
    'password':'Xbw891054582'
} #reddit的账户名称和密码

headers ={'User-Agent':'MyAPI/0.0.1'}

res = requests.post('https://www.reddit.com/api/v1/access_token',
                  auth=auth,data=data,headers=headers) #登录

TOKEN = res.json()['access_token']

headers={**headers, **{'Authorization':f'bearer{TOKEN}'}}

headers

res = requests.get('https://oauth.reddit.com/r/python/hot', headers=headers)
'''


url1='https://api.pushshift.io/reddit/comment/search/?q=gtav&size=450&before=270d'
res1=requests.get(url1)
res1

need = jsonpath.jsonpath(res1.json(),'$..body')
```
