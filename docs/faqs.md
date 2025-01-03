# FAQs

## 1. Why can't I create a link?

Please check the Cloudflare KV bindings, the KV environment variable name should be all uppercase letters.

<details>
  <summary><b>Screenshot</b></summary>
  <img alt="KV Bindings setting in Cloudflare" src="/docs/images/faqs-kv.png"/>
</details>

## 2. Why can't I log in?

Please check if `NUXT_SITE_TOKEN` is set to pure numbers, Sink does not support pure number Tokens, we consider this to be unsafe.

## 3. Why can't I see the analytics data?

Analytics data requires access to Cloudflare’s settings:

1. Verify `NUXT_CF_ACCOUNT_ID` and `NUXT_CF_API_TOKEN` are configured correctly (ensure the Account ID matches the deployment zone ID).
2. Check that the Worker analytics engine is enabled.

<details>
  <summary><b>Screenshot</b></summary>
  <img alt="Analytics engine Bindings setting in Cloudflare " src="/docs/images/faqs-Analytics_engine.png"/>
</details>

## 4. I don't want the current homepage? Can it be redirected to my blog?

Of course. Please set the environment variable `NUXT_HOME_URL` to your blog or official website address.

## 5. Why can't I see statistics after deploying with NuxtHub?

NuxtHub's ANALYTICS points to its dataset, you need to set the `NUXT_DATASET` environment variable to point to the same dataset.
