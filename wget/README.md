# wget Archive

Captured using basic proceedure outlined in [go-archive-tools](https://github.com/gathering/go-archive-tools)

1. `wget -np -m -p -E -o wget.log https://www.gathering.org/tg22/`
2. `extract_urls.sh | keep_asset_urls.sh | grep gathering.org | download_urls.sh`
3. `extract_urls.sh | keep_asset_urls.sh | grep gathering.org | replace_with_local_urls.sh "/"`
4. Move `/static` files to `/tg22/static` (and calls in `web-client-....js` and `web-vendor-....css` files)
5. `remove_url_query_parameters.sh`
6. Rename `web-client-....js` to stop it from running (and triggering non-archived api requests)

# To view

1. Go to `www.gathering.org` folder
2. Start a simple web server `npx http-server`
3. Visit web server in browser
