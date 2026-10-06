# amni-price-data

Nightly price tiles for the [Amni-Price](https://github.com/Amnibro/Amni-Price) app's **Community prices** feature.

The files on the [`packs` release](https://github.com/Amnibro/amni-price-data/releases/tag/packs) are built from the public
[Open Prices](https://prices.openfoodfacts.org) database (Open Food Facts), split into 2° × 2° map tiles so the app only downloads
the area around you.

- `index.json`: generation time, license and the list of tiles with their sizes and SHA-256
- `tile_<lat>_<lon>.json.gz`: stores (OpenStreetMap id, name, city, position), products (barcode, name, brand, size) and prices
  (store, product, cents, date, sale flag, currency), up to the last 4 observations per store and product from the past two years

Built on a home machine by [`tools/openprices/publish.sh`](https://github.com/Amnibro/Amni-Price/tree/main/tools/openprices).

## License

The data is © Open Food Facts contributors and available under the
[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/). Any rights in the tile files themselves are
licensed under the same ODbL 1.0. Please contribute prices back at [prices.openfoodfacts.org](https://prices.openfoodfacts.org).
