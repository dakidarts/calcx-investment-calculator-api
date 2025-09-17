![CalcX - Investment Calculator API Logo](assets/calcx-investment.png)

# Calcx Investment Calculator API

**Welcome to the Calcx Investment Calculator API, the ultimate tool to power up your financial applications!**

In today's fast-paced financial world, making informed investment decisions is crucial. Calcx empowers developers with a comprehensive set of tools to calculate key investment metrics, such as:
- **Simple Interest**
- **Compound Interest**
- **Return on Investment (ROI)**
- **Capital Gains Tax**
- **Annual Percentage Yield (APY)**

By integrating the Calcx Investment API, you can bring precision and accuracy to your financial calculations and enhance investment strategies for your users.

## 🌍 Supported Currencies

Our API supports a wide range of currencies, providing real-time conversion rates sourced from the **European Central Bank (ECB)**. Here's a sample of the supported currencies:

USD, EUR, GBP, JPY, AUD, CAD, ZAR, INR, PHP, ... and many more! Check out the [full list of supported currencies](https://dakidarts.com/api/calcx-investment-calculator-api/) on our documentation page.

## 📜 Features

- **Currency Conversion**: Calculates results in various currencies, letting users choose in_currency and to_currency for investment metrics.
- **Flexible Compounding Options**: Options include yearly, semi-annual, quarterly, and monthly compounding frequencies.
- **Error Handling**: Provides helpful messages for invalid requests with appropriate status codes (`200`, `400`, `500`).

## 🚀 Endpoints

### 1. /calculate - GET or POST

Calculates investment metrics based on provided parameters.

**Example**:
```http
GET /calculate?principal=50000.00&rate=6.5&time=36&in_currency=USD&to_currency=USD&compounding=yearly&format=yes
```

### 2. /calculate/post - POST

Similar to `/calculate`, but supports a JSON body.

**Example JSON Body**:
```json
{
    "principal": 50000,
    "rate": 6.5,
    "time": 12,
    "compounding": "quarterly",
    "format": "yes",
    "in_currency": "USD",
    "to_currency": "USD"
}
```

### 3. /calculate/batch - POST

Submit multiple calculations at once for batch processing.

**Example JSON Body**:
```json
[
    {
        "principal": 1000,
        "rate": 5,
        "time": 12,
        "to_currency": "EUR",
        "in_currency": "USD",
        "compounding": "monthly",
        "format": "yes"
    },
    {
        "principal": 5000,
        "rate": 7,
        "time": 24,
        "format": "no"
    }
]
```

## 📊 Parameter Guide

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `principal` | decimal | Yes | The principal amount of the investment. |
| `rate` | decimal | Yes | The interest rate for the investment. |
| `time` | int | Yes | Time period of the investment in months. |
| `compounding` | string | Optional | Compounding frequency (`yearly`, `semi-annually`, `quarterly`, `monthly`). Defaults to `yearly`. |
| `format` | string | Optional | If the response should be formatted. Valid options are `yes` (default) and `no`. |
| `in_currency` | string | Optional | Currency of the principal amount. Defaults to `USD`. |
| `to_currency` | string | Optional | Currency to convert the results to. Defaults to `USD`. |

## 📡 Get Started on RapidAPI

To use the Calcx Investment Calculator API:

1. Visit the [API Documentation](https://dakidarts.com/api/calcx-investment-calculator-api/) to learn more.
2. Subscribe on RapidAPI to start making requests: [Calcx Investment Calculator API on RapidAPI](https://rapidapi.com/dakidarts-dakidarts-default/api/calcx-investment-api).

**Note**: You do not need to clone this repository. Access the API through RapidAPI directly.

## 📂 Status Codes

| Status Code | Description |
|-------------|-------------|
| `200` | Successful calculation and response. |
| `400` | Invalid request or missing parameters. |
| `500` | Internal server error. |

## 🔄 Error Handling

If an error occurs during request processing, the API returns an appropriate error message with the status code, ensuring that any issues are clear and easy to resolve.

Thank you for choosing the **Calcx Investment Calculator API** for your investment calculations! If you have any questions or need support, feel free to reach out via RapidAPI.
