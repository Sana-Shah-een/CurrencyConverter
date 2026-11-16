# Currency Converter

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML) [![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS) [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

A clean, responsive currency converter built with HTML, CSS, and vanilla JavaScript. Select a source and target currency, enter an amount, and fetch the latest available exchange rate in seconds.

## Features

- Convert between a wide range of global currencies.
- USD and PKR are selected by default for a quick start.
- Automatically updates the country flag when a currency changes.
- Fetches live exchange rates from the Currency API.
- Displays a clear error message when the exchange-rate request is unavailable.
- Responsive, minimal interface with accessible form controls.

## Technology Stack

- **HTML5** - semantic page structure and form controls.
- **CSS3** - layout, spacing, responsive presentation, and visual styling.
- **Vanilla JavaScript (ES6+)** - dropdown population, API requests, flag updates, validation, and UI interaction.
- **Font Awesome 6.5.1** - currency-switch icon.
- **Currency API** - live exchange-rate data.
- **Flags API** - country flag images for selected currencies.

## Color Palette

The interface color palette was generated with [Coolors](https://coolors.co/) and applied to create a calm, readable financial dashboard aesthetic:

| Color | Hex | Usage |
| --- | --- | --- |
| Mint Green | `#B7E4C7` | Page background |
| Sea Green | `#40916C` | Primary action button |
| White | `#FFFFFF` | Converter card background |
| Light Gray | `lightgray` | Input and currency selector borders |

## Getting Started

### Prerequisites

You only need a modern web browser. No package installation or build step is required.

### Run locally

1. Clone or download this repository.
2. Open the project folder.
3. Open `index.html` in a browser.

For the best local-development experience, serve the folder with a local web server, such as the **Live Server** extension in VS Code:

```text
Right-click index.html → Open with Live Server
```

## How to Use

1. Enter the amount you want to convert.
2. Choose the currency to convert **from**.
3. Choose the currency to convert **to**.
4. Select **Get Exchange Rate**.
5. View the converted amount below the currency selectors.

Amounts below `1` or blank amounts are reset to `1` automatically.

## Project Structure

```text
CurrencyConverter/
├── index.html   # Application markup and external stylesheet/icon references
├── style.css    # Layout and visual styling
├── app.js       # Converter logic, API calls, and flag updates
├── codes.js     # Currency-to-country-code mapping
└── README.md    # Project documentation
```

## API Integrations

Exchange rates are requested from:

```text
https://latest.currency-api.pages.dev/v1/currencies/{currency}.json
```

Flag images are loaded from:

```text
https://flagsapi.com/{country-code}/flat/64.png
```

These services are external dependencies, so rate availability and response times may vary. An in-app message is shown when a rate cannot be retrieved.

## Future Improvements

- Add exchange-rate timestamps and source attribution.
- Add a swap-currencies control.
- Improve amount formatting based on the selected currency.
- Add loading feedback while a request is in progress.
- Add automated tests for conversion and validation behavior.

## License

No license has been specified for this project yet.
