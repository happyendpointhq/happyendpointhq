# Happy Endpoint

Real-time data APIs for property portals, retailers, and marketplaces.

We turn sites that have no public API into clean, structured JSON endpoints, so
you do not have to build and maintain scrapers, rotate proxies, or repair
selectors every time the HTML changes. Every API is available on RapidAPI with a
free tier.

[happyendpoint.com](https://happyendpoint.com) |
[API catalogue](https://happyendpoint.com/library) |
[Datasets](https://happyendpoint.com/datasets) |
[Documentation](https://docs.happyendpoint.com)

---

## What we cover

| Market | Platforms |
|---|---|
| UAE real estate | Bayut, PropertyFinder, UAE Real Estate |
| UK real estate | Rightmove, Gumtree |
| Spain real estate | Idealista, Fotocasa |
| Turkey real estate | Emlakjet, Hepsiemlak |
| US real estate | Auction.com, Realtor.com |
| APAC real estate | 99co (Singapore), Suumo (Japan) |
| Other real estate | Aqar (Saudi Arabia), Yad2 (Israel), Njuskalo (Croatia) |
| Retail and grocery | Tesco, IKEA, Kohl's, H&M |
| Beauty | Sephora |
| Travel | Priceline, VRBO |
| Finance | Morningstar, Klarna |

Two product shapes per platform. **APIs** for request-time data, priced per
request through RapidAPI. **Datasets** for bulk snapshots, priced per file. Most
datasets ship a free sample with an identical schema, so you can build against
the sample and switch to the paid file once your integration works.

---

## Repositories

### API documentation

| Repo | Covers | Hosted docs |
|---|---|---|
| [bayut-api](https://github.com/happyendpointhq/bayut-api) | Dubai and UAE listings, agents, agencies, off-plan, transactions | [docs](https://happyendpointhq.github.io/bayut-api/) |
| [propertyfinder-api](https://github.com/happyendpointhq/propertyfinder-api) | UAE listings and broker data | [docs](https://happyendpointhq.github.io/propertyfinder-api/) |
| [sephora-api](https://github.com/happyendpointhq/sephora-api) | Beauty products, pricing, reviews, availability | [docs](https://happyendpointhq.github.io/sephora-api/) |
| [ikea-api](https://github.com/happyendpointhq/ikea-api) | IKEA products, categories, store data | [docs](https://happyendpointhq.github.io/ikea-api/) |
| [priceline-api](https://github.com/happyendpointhq/priceline-api) | Hotel, flight, and car rental pricing | [docs](https://happyendpointhq.github.io/priceline-api/) |

### Code and examples

| Repo | Language |
|---|---|
| [bayut-api-python-examples](https://github.com/happyendpointhq/bayut-api-python-examples) | Python client and nine runnable examples |
| [bayut-api-javascript-nextjs](https://github.com/happyendpointhq/bayut-api-javascript-nextjs) | JavaScript and Next.js |
| [bayut-api-postman-collection](https://github.com/happyendpointhq/bayut-api-postman-collection) | Postman collection covering every endpoint |

### Tools

| Repo | What it does |
|---|---|
| [dubai-rental-yield-calculator](https://github.com/happyendpointhq/dubai-rental-yield-calculator) | Compares gross and net rental yields across Dubai areas |
| [dubai-property-price-tracker](https://github.com/happyendpointhq/dubai-property-price-tracker) | Monitors listings and alerts on price drops |

### Clients and tooling

| Repo | What it is |
|---|---|
| [happyendpoint-mcp](https://github.com/happyendpointhq/happyendpoint-mcp) | MCP server, so Claude and Cursor can query our data directly |
| [happyendpoint-python](https://github.com/happyendpointhq/happyendpoint-python) | Python client covering every API |
| [happyendpoint-js](https://github.com/happyendpointhq/happyendpoint-js) | TypeScript client |
| [happyendpoint-cli](https://github.com/happyendpointhq/happyendpoint-cli) | Query property data from the terminal |

### Curated lists

Research we maintain on the wider data landscape. These include competitors,
government open data, and free alternatives, several of which are better choices
than ours for particular use cases.

| Repo | Covers |
|---|---|
| [awesome-real-estate-apis](https://github.com/happyendpointhq/awesome-real-estate-apis) | Property data sources by country: official, government, commercial, scraping |
| [awesome-ecommerce-data-apis](https://github.com/happyendpointhq/awesome-ecommerce-data-apis) | Product, pricing, and retail catalogue data |
| [awesome-alternative-data](https://github.com/happyendpointhq/awesome-alternative-data) | Alternative data for investment research |

### Guides

| Repo | Covers |
|---|---|
| [uae-real-estate-data-guide](https://github.com/happyendpointhq/uae-real-estate-data-guide) | Every route to UAE property data, including alternatives to us |

---

## Datasets

Bulk snapshots, sold as files rather than per request.

- [IKEA US Complete Product Dataset](https://payhip.com/b/Ppkis) - 10,564 products, 933 categories, CSV
- [Sephora US Products](https://payhip.com/b/faOZH) - 8,000+ products
- [PropertyFinder UAE Historical Transactions](https://payhip.com/b/A4nRp)

More at [happyendpoint.com/datasets](https://happyendpoint.com/datasets). Need a
platform or field set we do not list? Email us.

---

## Using our APIs from an AI assistant

RapidAPI hosts an MCP server, so any of our APIs can be queried from Claude,
Cursor, or another MCP client without writing code. Swap `x-api-host` for
whichever API you want:

```json
{
  "mcpServers": {
    "Bayut UAE Real Estate": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://mcp.rapidapi.com",
        "--header",
        "x-api-host: uae-real-estate3.p.rapidapi.com",
        "--header",
        "x-api-key: YOUR_RAPIDAPI_KEY"
      ]
    }
  }
}
```

---

## Getting started

1. Pick an API from the [catalogue](https://happyendpoint.com/library)
2. Subscribe on RapidAPI, free tier available
3. Send your key as the `x-rapidapi-key` header
4. Copy a working example from the repos above

---

## Elsewhere

- [uaepropertyapi.com](https://uaepropertyapi.com/)
- [bayutapi.dev](https://bayutapi.dev/)
- [RapidAPI profile](https://rapidapi.com/user/happyendpoint)
- [@happyendpointhq](https://x.com/happyendpointhq)
- happyendpointhq@gmail.com

---

## Disclaimer

Happy Endpoint is an independent provider. This project is **not affiliated
with, endorsed by, sponsored by, or connected to** any of the websites,
platforms, retailers, or marketplaces referenced here or reachable through the
underlying APIs.

All product names, brands, trademarks, and registered trademarks are the
property of their respective owners. Any reference to them is descriptive only,
to identify the subject matter of the data, and does not imply any association
or endorsement.

Users are responsible for ensuring their use of any data complies with
applicable laws and the terms of service of the relevant source.
