# Foursquare Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Foursquare Scraper](https://oxylabs.io/products/scraper-api/web/foursquare?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Foursquare website effortlessly. This brief guide explains how an Foursquare Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Foursquare results by providing your own URLs to our service. We can return the HTML for any Foursquare page you like.

#### Python code example

The example below illustrates how you can get HTML of Foursquare page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://location.foursquare.com/products/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/foursquare-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en-US\">\n<head>\n\t<meta charset=\"UTF-8\">\n\t<meta name=\"viewport\" content=\"w ... </html>",
      "created_at": "2023-12-18 11:13:47",
      "updated_at": "2023-12-18 11:13:48",
      "page": 1,
      "url": "https://location.foursquare.com/products/",
      "job_id": "7142472008956183553",
      "status_code": 200
    }
  ]
}
```
With our Foursquare Scraper, you can easily gather public data from any Foursquare web page. Harvest crucial venue information, such as ratings, reviews or check-ins, to analyze the food and beverage market and outperform your competitors. For any inquiries, feel free to reach out to our support team through live chat or email us at hello@oxylabs.io.