This client library is designed to support the Blocket REST API.

Blocket does not supply a public API any more, so this wrapper are for those who can find other ways to gain acces to the api ;)

Install:
	python setup.py install

Basic usage:
```python
import blocket

b = blocket.API(app_id, api_key)
	
# Search for volvo cars
results = b.search("volvo")
for ad in results['ads']:
	print ad['subject']
	
# View an indiviual ad
ad = b.view("46637278")

# Get any related ads to a specific ad
related = b.related("46637278")

# Get all categories
categories = b.categories()

# Get all areas
areas = b.areas()
```
