# API Serpent PHP SDK

Official PHP wrapper for [API Serpent](https://apiserpent.com/serp-api) – fast, reliable, and cost-effective search engine results API.

## Features

- **SERP API:** Fetch real-time search engine results from Google, Bing, Yahoo, DuckDuckGo, and Brave in clean JSON format.
- **Rank Tracking API:** Monitor search rankings for your keywords programmatically across locations and devices.
- **Pixel Position API:** Get exact pixel-level placement metrics to calculate true above-the-fold visibility.
- **AI Search Monitoring:** Track visibility across generative engines including ChatGPT, Claude, Gemini, and Perplexity.

---

## Quick Start

### Installation

```bash
composer require guzzlehttp/guzzle
```

### Basic Usage

```php
<?php
require 'vendor/autoload.php';

use GuzzleHttp\Client;

$client = new Client();
$apiKey = 'YOUR_API_SERPENT_KEY';
$endpoint = 'https://api.apiserpent.com/v1/search';

$response = $client->request('GET', $endpoint, [
    'query' => [
        'api_key'  => $apiKey,
        'q'        => 'php serp api',
        'engine'   => 'google',
        'location' => 'United States',
    ]
]);

$data = json_decode($response->getBody(), true);

print_r($data);
```

---

## Documentation & Links

- [SERP API Overview](https://apiserpent.com/serp-api)
- [Rank Tracking API](https://apiserpent.com/rank-tracking-api)
- [Pixel Position API](https://apiserpent.com/pixel-position-api)
- [API Serpent Homepage](https://apiserpent.com/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
