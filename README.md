# Producthunt Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Producthunt Scraper](https://oxylabs.io/products/scraper-api/web/producthunt?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Producthunt website effortlessly. This brief guide showcases how Producthunt Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Producthunt results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Producthunt page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.producthunt.com/topics/design-tools'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/producthunt-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\"/><title> The Best Design Tools Apps and P ... </html>",
      "created_at": "2024-02-20 12:34:36",
      "updated_at": "2024-02-20 12:34:40",
      "page": 1,
      "url": "https://www.producthunt.com/topics/design-tools",
      "job_id": "7165685171746786305",
      "status_code": 200
    }
  ]
}
```
With our Producthunt Scraper, you can seamlessly pull public data from any Producthunt web page. Gather all necessary tech product insights, including launch dates, maker details, or upvotes, to keep up with industry trends and gain an edge over your competitors. In case of any inquiries, feel free to reach out to our customer support team through live chat or email us at hello@oxylabs.io.