# stac-api-instructions

### Retrieve using Bounding Box
To retrieve a dataset using a location, a bounding box `bbox` is required as a parameter. For example:
```
https://api.diwata-stac.philsa.gov.ph/search?bbox=120.007,12.157,121.649,13.501
```

### Retrieve using Point (Longitude and Latitude)
To retrieve a dataset using a point, a Point GeoJSON Object can be passed to `intersects` parameter.
```
const point =
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [125.6, 10.1]
  }
}

https://api.diwata-stac.philsa.gov.ph/search?intersects=

```

### References
1. ItemSearch STAC API: https://stac-utils.github.io/stac-server/#tag/Item-Search/operation/getItemSearch