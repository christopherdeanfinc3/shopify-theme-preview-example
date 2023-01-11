# shopify-theme-preview-example

This Project is an example for the usage of the [Shopify Theme Preview Action](https://github.com/Brand-Boosting-GmbH/shopify-theme-preview).

To see this action in action, simply click on the open Pull Request and see for yourself!

### preview.yml

```yaml
run-name: Create Theme Preview by @${{ github.actor }}
on:
  issue_comment:      
    types: [created]    
jobs:                   
  deploy:
    name: Preview
    runs-on: ubuntu-latest
    if: contains(github.event.comment.body, '!preview')
    steps:
      - uses: Brand-Boosting-GmbH/shopify-theme-preview@v1
        with:
          shopify_flag_store: 'your-store.myshopify.com'
          shopify_cli_theme_token: 'shopify_cli_theme_token'
          build_step: 'npm i && npm run build'              // optional
          dir: 'dist'                                       // optional

```

For more detailed information follow these links:

[GitHub Action]( https://github.com/Brand-Boosting-GmbH/shopify-theme-preview)

[GitHub Marketplace](https://github.com/marketplace/actions/create-shopify-theme-preview)

[brand-boosting.de]( https://brand-boosting.de/)

---
<div style="display: inline">
  <img width="280" alt="wort-bild-primary@2x" src="https://user-images.githubusercontent.com/77160493/206194969-10dc2ed8-476d-4639-865e-75c9028109a4.png">
  <div>
    <b>Brand Boosting GmbH</b> |
    <b>David Süßlin</b>
  </div>
</div>
