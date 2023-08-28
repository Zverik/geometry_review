# Geometry Review Tool

This stand-alone page is for reviewing geometries one by one.
You prepare a JSON file for it with features to review, and specify options to choose for each feature.
The result can be exported to a text file, with which you can resume your review if you stop part-way.
There is no server; all the data is stored on your machine locally.

[Open the tool](https://zverik.github.io/geometry_review/)

## Sample JSON

I know, it's hard to prepare an input file without an example.

```json
[
  {
    "id": "first",
    "title": "First object, <b>a point</b>",
    "geometries": [
      {
        "type": "Feature",
        "geometry": {"type": "Point", "coordinates": [10.56, 18.23]},
        "properties": {"icon": 1}
      }
    ]
  },
  {
    "id": "second",
    "title": "Let's compare <a href=\"https://osm.org/\">lines</a>",
    "geometries": [
      {"type": "LineString", "coordinates": [[5.23, 10.345], [5.65, 10.23]]},
      {"type": "LineString", "coordinates": [[5.24, 10.335], [5.62, 10.21]]}
    ]
  }
]
```

Note that geometries (including markers for points) are colored in blue, black, red etc.
Use `dash: true` in GeoJSON feature properties to display a line dashed, and
`icon: 'A'` to display a text ("A" in this case) on a marker.
Yes, you can have links in titles, but keep them short. Titles are optional actually.
Geometries can be GeoJSON features or geometries, or even FeatureCollections.

## Author and License

Written by Ilya Zverev, published under MIT license.

Includes Muhammad Arslan Sajid's [BeautifyMarker](https://github.com/masajid390/BeautifyMarker),
also published under MIT license.
