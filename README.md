# AI API Pricing — DeepAPI

Compare LLM API prices across models and providers, with input and
output costs shown separately.

[Open the API price comparison](https://deepapi.app/model-api-price)

A low input price does not always mean a low bill. Output length,
cache usage, and provider-specific charges can change which option
costs less.

This repository is a public reference for DeepAPI's API pricing
comparisons. It explains how to read token prices and estimate costs.
The interactive listings are on the website; this repository does
not contain the application source code or a complete pricing dataset.

## Start with the question you need to answer

| Question | Where to look |
| --- | --- |
| What do different models and providers charge? | [API price comparison](https://deepapi.app/model-api-price) |
| What information does DeepAPI list about a model? | [Model directory](https://deepapi.app/models) |
| How are prices and uncertain information handled? | [Comparison methodology](https://deepapi.app/methodology) |
| Am I comparing an API with a monthly app plan? | [Subscription prices](https://deepapi.app/subscriptions) |

For provider comparisons, match the exact model version first.
Similar names do not necessarily mean identical models, context
limits, or service conditions.

## How much does an LLM API cost per million tokens?

Text API prices are commonly quoted separately for input and output.
Keep those rates separate when estimating a bill.

For a basic text workload without caching or additional charges:

    estimated cost =
      (input tokens / 1,000,000 × input rate)
      + (output tokens / 1,000,000 × output rate)

Here is a worked example using fictional USD prices:

| Provider | Input / 1M tokens | Output / 1M tokens |
| --- | ---: | ---: |
| A | $1.00 | $4.00 |
| B | $0.50 | $6.00 |

For 10 million input tokens and 1 million output tokens:

- Provider A: (10 × $1.00) + (1 × $4.00) = **$14.00**
- Provider B: (10 × $0.50) + (1 × $6.00) = **$11.00**

For 1 million input tokens and 1 million output tokens:

- Provider A: $1.00 + $4.00 = **$5.00**
- Provider B: $0.50 + $6.00 = **$6.50**

The cheaper option changes with the workload. Adding the two unit
prices gives an equal-volume comparison, not an estimate for every
application.

These examples exclude caching, tools, taxes, and other charges.
They are not quotes from actual providers.

## Comparing providers for the same model

Before choosing the lowest listed price, check:

- **Model identity:** exact version, variant, and supported features.
- **Billing:** currency, units, minimum charges, and additional fees.
- **Usage conditions:** context tiers, batch processing, or promotions.
- **Service:** rate limits, latency, availability, and data policies.
- **Evidence:** the source of the quote and when it was checked.

For an OpenRouter vs direct API comparison, use the same model and
usage assumptions on both sides. Check any platform or payment fees
separately from the model's token rates.

A lower token price alone does not establish better value.

## Cached input, batch requests, and long context

A standard input rate does not describe every request.

**Cached input:** Check which tokens qualify for a cache-read rate
and whether cache writes or storage incur separate charges. Do not
apply a cache discount to the entire prompt by default.

**Batch requests:** Compare batch rates separately from interactive
rates, and check the provider's processing conditions.

**Long context:** Check whether the published rate changes above an
input-length threshold.

For image, audio, video, or request-based billing, keep the original
unit visible. A price per image or minute is not directly comparable
to a text price per million tokens.

## Reading the listings

DeepAPI includes listings for model companies and third-party API
providers. Coverage and available fields vary.

Read the source and verification information beside each quote.
Some observations may be unverified or lack a source link. Treat
those as leads to investigate, not confirmed purchase prices.

A checked date describes a past check; it does not guarantee that
a price is unchanged today. Confirm the provider's current terms
before committing a production workload.

See the [methodology](https://deepapi.app/methodology) for the site's
approach to sources, normalization, and uncertainty.

## Report a pricing error

Please open an issue with:

- The DeepAPI page URL.
- The exact model and API provider.
- The listed price and the proposed correction.
- An official pricing or documentation link, if available.
- The date checked and any relevant conditions.

Include the currency and billing unit. Please do not include API
keys, account details, or private billing documents.

## About DeepAPI

[DeepAPI](https://deepapi.app) is an independent comparison site for
AI products and prices. This repository focuses on API costs;
the website also covers subscriptions and buying guides.

DeepAPI is not affiliated with the providers listed. Prices and
availability can change, and a listing is not an endorsement.
