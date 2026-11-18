# Coderise Coaching site

Static site for coderisecoaching.com, deployed as the Cloudflare Worker `red-hat-50c0` from the `main` branch.

- `public/index.html`: home page, packages and prices, free guide form, FAQ
- `public/terms.html`, `public/privacy.html`: legal pages
- `public/welcome.html`: page Stripe sends buyers to after payment

No build step. `wrangler.jsonc` points Cloudflare at the `public` folder.

Prices appear only in `public/index.html`. Each Buy button links to a Stripe payment link, so a price change needs a matching payment link in Stripe.
