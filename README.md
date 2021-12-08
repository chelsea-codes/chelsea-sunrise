# [chelsea-sunrise](https://www.chelsea-sunrise.com)

My primary goal for this site is to show you a glimpse of who I am beyond the customary one-page resume. I also want it to be simple to maintain, update with new content, and deploy.

**Stack:**

*   [Node.js](https://nodejs.org/en/about/)

*   [Hexo](https://hexo.io/) with the [Cactus](https://github.com/probberechts/hexo-theme-cactus) theme

*   Static hosting using [Cloudflare Workers](https://www.workers.cloudflare.com)

## Configuration
Update entries in root `_config.yml` and `_config.cactus.yml` files.

Sensitive or environment dependent entries should be added to `_config.local.yml` and `_config.prod.yml`. (See [_config.env.yml.sample](./_config.env.yml.sample)) These files are ignored in commits.

## Local Development

Install project and theme dependencies:
```
npm install && npm run install-theme
```

Clean hexo project and generate static files:
```
npm run build-dev
```

Run hexo server:
```
npm run server-dev
```

View the **development** app at http://localhost:4000.

# Deploy to Production
Clean hexo project and generate static files:
```
npm run build-prod
```

Login to Wrangler (Cloudflare workers):
```
$(npm bin)/wrangler login
```

Deploy to Cloudflare worker:
```
npm run deploy-prod
```

View the **production** app at https://www.chelsea-sunrise.com or https://chelsea-sunrise-prod.chelseasunrise.workers.dev.
