# EnergyDrinkPriceData

Prices of energy drinks scraped from major NZ supermarket websites.

The code that scrapes this data is [here](https://github.com/DanGamingTV/SupermarketScraping).

All files in the directories follow this schema:
```json
[
{
        "productData": {
            "name": "(string) Name of the specific product",
            "productId": "(string) Product ID or SKU",
            "productShopPage": "(string) The link of this product on the supermarket's website",
            "productImageURL": "(string) Link to an image of this product",
            "productDescription": "(string) Any description that the supermarket provides for this item",
            "volume": "(string) The volume of this energy drink",
            "multipack": {
                "quantity": "(int) The quantity of this product provided, if it's in a multipack"
            }
        },
        "priceData": {
            "bestPrice": "(int) The lowest possible price for this product if bought in a multibuy or other promotion",
            "price": "(int) The default price for this product, excluding multibuys",
            "pricePerLitre": "(int) The default price per litre of this product",
            "bestPricePerLitre": "(int) The lowest possible price per litre for this product if bought in a multibuy or other promotion"
        },
        "store": {
            "id": "(string) If item pricing varies per store, this is the internal ID of the store this product price applies to",
            "name": "(string) If item pricing varies per store, this is the name of the store this product price applies to"
        }
    }, // repeated for each item scraped
]
```

Updated every now and then, if you want true reliability you'd probably want to get a copy of SupermarketScraper and run it yourself.