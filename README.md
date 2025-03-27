# gsi-dem-terrain-rgb-tiles

国土地理院の標高タイル（基盤地図情報数値標高モデル）の Terrain-RGB タイルです。

## 使い方

本タイルは [GitHub Pages](https://docs.github.com/ja/pages/getting-started-with-github-pages/about-github-pages) でホスティングしており、TileJSON 及びタイルは下記 URL となっています。

|          | URL                                                                   |
| -------- | --------------------------------------------------------------------- |
| TileJSON | https://geodig-jp.github.io/gsi-dem-terrain-rgb-tiles/tiles.json      |
| タイル    | https://geodig-jp.github.io/gsi-dem-terrain-rgb-tiles/{z}/{x}/{y}.png |

MapLibre GL JS の場合、下記のように指定することで利用可能です。

```js
map.addSource('raster-dem-source', {
  type: 'raster-dem',
  url: 'https://geodig-jp.github.io/gsi-dem-terrain-rgb-tiles/tiles.json',
  tileSize: 256
});
```

## 仕様

本タイルの仕様は以下の通りです。

|           | 仕様                           |
| --------- | ----------------------------- |
| データ     | 基盤地図情報数値標高モデル(DEM10B)　 |
| 最小ズーム  | 1                             |
| 最大ズーム  | 12                            |
| タイルサイズ | 256 * 256                     |
| 最終更新日  | 2025/03/27                    |

標高タイルの詳細な仕様は国土地理院の下記 URL からご覧いただけます。

- https://maps.gsi.go.jp/development/demtile.html
- https://maps.gsi.go.jp/development/hyokochi.html

## 利用

本タイルは、GitHub Pages および国土地理院の利用規約に準拠してご利用ください。

- https://docs.github.com/ja/pages/getting-started-with-github-pages/about-github-pages#github-pages%E3%81%AE%E5%88%A9%E7%94%A8%E4%B8%8A%E3%81%AE%E5%88%B6%E9%99%90
- https://www.gsi.go.jp/kikakuchousei/kikakuchousei40182.html

## 参考

- https://zenn.dev/shi_works/articles/6f50506d5bc3b0
- https://docs.mapbox.com/ja/data/tilesets/reference/mapbox-terrain-rgb-v1/
- https://github.com/mapbox/tilejson-spec
- https://maplibre.org/maplibre-gl-js/docs/API/classes/RasterDEMTileSource/