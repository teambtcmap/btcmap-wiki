# Embedding

If you would like to embed the web map on your own website, simply add the following code to your HTML:

```html
<iframe
  id="btcmap"
  title="BTC Map"
  width="600"
  height="300"
  allowfullscreen="true"
  allow="geolocation"
  src="https://btcmap.org/map"
>
</iframe>
```

You can adjust the `width` and `height` attributes to fit your page.

**NOTE:** If you want the geolocation feature to work you must also allow this in the `Permissions Policy HTTP Header` on the server of your website.

```
Permissions-Policy: geolocation=(self "https://btcmap.org")
```

For more information see this [article](https://developer.chrome.com/docs/privacy-sandbox/permissions-policy/).

### If you would like the map the initialize on a specific location there are a couple more steps to complete

#### General area

1. Visit [btcmap.org/map](https://btcmap.org/map) and zoom the map to your desired location
2. Copy the URL from your browser tab which contains geolocation data
3. Add this URL to your `iframe` `src` attribute embed code

#### Communities map

1. Use `https://btcmap.org/communities/map` for your `iframe` URL

##### Community area

1. Use `https://btcmap.org/communities/map?community=einundzwanzig-deutschland` for your `iframe` URL (replace `einundzwanzig-deutschland` with the ID of your community - this can be found in the URL when visiting your community page)

##### Organization filter

1. Use `https://btcmap.org/communities/map?organization=einundzwanzig`

##### Language filter

1. Use `https://btcmap.org/communities/map?language=es`

### If you would like to filter by payment method

Add the preferred payment method(s) as `URLSearchParams` to the `src` attribute of your `iframe`. These can be added in addition to the location params above.

The available options are:

- onchain
- lightning
- nfc

Example: `/map?onchain&lightning`

### Selecting a default basemap

To choose which basemap displays on page load, you can add the `basemap` param to your URL. The values correspond to the order they appear in the list on the map. For example, if you wanted to use the Terrain basemap you would add `basemap=7`. Like so: `/map?basemap=7`.

That's it!

Embedding is also possible on native mobile applications by utilizing the **WebView**.
