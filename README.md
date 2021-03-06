# facebookmarketing-python

facebookmarketing is an API wrapper for Facebook written in Python

## Installing
```
pip install git+git://github.com/GearPlug/facebookmarketing-python.git
```

## Usage
```
from facebookmarketing.client import Client

client = Client('APP_ID', 'APP_SECRET', 'v2.10')
```

Get authorization url
```
url = client.authorization_url('REDIRECT_URL', ['manage_pages'])
```

Exchange the code for an access token
```
token = client.exchange_code('REDIRECT_URL', 'CODE')
```

Extend a short-lived access token for a long-lived access token
```
token = client.extend_token('SHORT-LIVED TOKEN')
```

Get app token
```
token = client.get_app_token()
```

Inspect a token
```
info = client.inspect_token('INPUT TOKEN', 'APP TOKEN')
```

Set the access token
```
client.set_access_token('TOKEN')
```

Get account information
```
account = client.get_account()
```

Get account pages
```
pages = client.get_pages()
```

Get forms given the page
```
forms = client.get_ad_account_leadgen_forms('PAGE_ID')
```

Get leads given the form
```
leads = client.get_ad_leads('FORM_ID')
```

## Requirements
- requests

## Tests
```
python tests/test_client.py
```

## TODO Endpoints
- Ad Creative
- Image Ad
- Previews
- Ad Preview Plugin
- Ad Set
- Ad User
- Ad Video
- Campaign
- Connection Objects
- Currencies
- Image Crop
- Product Catalog
