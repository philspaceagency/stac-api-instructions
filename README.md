# stac-api-instructions

### Retrieve using Bounding Box
To retrieve a dataset using a location, a bounding box `bbox` is required as a parameter. For example:
```
https://api.diwata-stac.philsa.gov.ph/search?bbox=120.007,12.157,121.649,13.501
```

### Retrieve using Point (Longitude and Latitude)
To retrieve a dataset using a point, a Point GeoJSON Object can be passed to `intersects` parameter.
```
{
    "type": "Point",
    "coordinates": [125.6, 10.1]
  }
}
```

#### Request URL
    https://api.diwata-stac.philsa.gov.ph/search?intersects=%7B%20%20%20%20%20%22type%22%3A%20%22Point%22%2C%20%20%20%20%20%22coordinates%22%3A%20%5B125.6%2C%2010.1%5D%20%20%20%7D&limit=10

Which should return a FeatureCollection like so:
```
{
  "type": "FeatureCollection",
  "context": {
    "limit": 10,
    "returned": 2
  },
  "features": [
    {
      "id": "D2_SMI_2020-02-15T045948_2020-02-15T235959_L1C",
      "bbox": [
        125.32203903061281,
        8.85592794762939,
        126.36210992582708,
        10.686407940821363
      ],
      "type": "Feature",
      "links": [
        {
          "rel": "collection",
          "type": "application/json",
          "href": "https://api.diwata-stac.philsa.gov.ph/collections/diwata-2"
        },
        {
          "rel": "parent",
          "type": "application/json",
          "href": "https://api.diwata-stac.philsa.gov.ph/collections/diwata-2"
        },
        {
          "rel": "root",
          "type": "application/json",
          "href": "https://api.diwata-stac.philsa.gov.ph/"
        },
        {
          "rel": "self",
          "type": "application/geo+json",
          "href": "https://api.diwata-stac.philsa.gov.ph/collections/diwata-2/items/D2_SMI_2020-02-15T045948_2020-02-15T235959_L1C"
        }
      ],
      "assets": {
        "thumbnail": {
          "href": "https://storage.googleapis.com/philsa-diwata-open-data/D2/thumbnail/D2_SMI_2020-02-15T045948_2020-02-15T235959_THUMB.png",
          "type": "image/png",
          "roles": [
            "thumbnail"
          ],
          "title": "Thumbnail"
        },
        "top-of-atmosphere-reflectance": {
          "href": "https://storage.googleapis.com/philsa-diwata-open-data/D2/smi/D2_SMI_2020-02-15T045948_2020-02-15T235959_L1C_COG.tif",
          "type": "image/tiff; application=geotiff; profile=cloud-optimized",
          "roles": [
            "cog",
            "data",
            "visual"
          ],
          "title": "Top of Atmosphere Reflectance (L1C)",
          "eo:bands": [
            {
              "name": "V490",
              "common_name": "blue",
              "description": "Operational Band V490"
            },
            {
              "name": "V550",
              "common_name": "green",
              "description": "Operational Band V550"
            },
            {
              "name": "V620",
              "common_name": "yellow",
              "description": "Operational Band V620"
            },
            {
              "name": "V670",
              "common_name": "red",
              "description": "Operational Band V670"
            },
            {
              "name": "V708",
              "common_name": "red-edge",
              "description": "Operational Band V708"
            }
          ],
          "raster:bands": [
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 993.099609375,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992.9098510742188,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992.37353515625,
                "minimum": 0
              },
              "spatial_resolution": 125
            }
          ]
        }
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
            [
              125.32203903061281,
              8.85592794762939
            ],
            [
              125.32203903061281,
              10.686407940821363
            ],
            [
              126.36210992582708,
              10.686407940821363
            ],
            [
              126.36210992582708,
              8.85592794762939
            ],
            [
              125.32203903061281,
              8.85592794762939
            ]
          ]
        ]
      },
      "collection": "diwata-2",
      "properties": {
        "datetime": "2020-02-15T04:59:48Z",
        "platform": "Diwata-2",
        "proj:epsg": 3857,
        "instruments": [
          "Spaceborne Multispectral Imager (SMI)"
        ]
      },
      "stac_version": "1.0.0",
      "stac_extensions": [
        "https://stac-extensions.github.io/projection/v1.1.0/schema.json",
        "https://stac-extensions.github.io/eo/v1.1.0/schema.json",
        "https://stac-extensions.github.io/raster/v1.1.0/schema.json"
      ]
    },
    {
      "id": "D2_SMI_2019-10-09T045641_2019-10-09T125741_L1C",
      "bbox": [
        125.08806295692507,
        9.364368559641449,
        126.01662343226049,
        10.496677916255502
      ],
      "type": "Feature",
      "links": [
        {
          "rel": "collection",
          "type": "application/json",
          "href": "https://api.diwata-stac.philsa.gov.ph/collections/diwata-2"
        },
        {
          "rel": "parent",
          "type": "application/json",
          "href": "https://api.diwata-stac.philsa.gov.ph/collections/diwata-2"
        },
        {
          "rel": "root",
          "type": "application/json",
          "href": "https://api.diwata-stac.philsa.gov.ph/"
        },
        {
          "rel": "self",
          "type": "application/geo+json",
          "href": "https://api.diwata-stac.philsa.gov.ph/collections/diwata-2/items/D2_SMI_2019-10-09T045641_2019-10-09T125741_L1C"
        }
      ],
      "assets": {
        "thumbnail": {
          "href": "https://storage.googleapis.com/philsa-diwata-open-data/D2/thumbnail/D2_SMI_2019-10-09T045641_2019-10-09T125741_THUMB.png",
          "type": "image/png",
          "roles": [
            "thumbnail"
          ],
          "title": "Thumbnail"
        },
        "top-of-atmosphere-reflectance": {
          "href": "https://storage.googleapis.com/philsa-diwata-open-data/D2/smi/D2_SMI_2019-10-09T045641_2019-10-09T125741_L1C_COG.tif",
          "type": "image/tiff; application=geotiff; profile=cloud-optimized",
          "roles": [
            "cog",
            "data",
            "visual"
          ],
          "title": "Top of Atmosphere Reflectance (L1C)",
          "eo:bands": [
            {
              "name": "V490",
              "common_name": "blue",
              "description": "Operational Band V490"
            },
            {
              "name": "V550",
              "common_name": "green",
              "description": "Operational Band V550"
            },
            {
              "name": "V620",
              "common_name": "yellow",
              "description": "Operational Band V620"
            },
            {
              "name": "V670",
              "common_name": "red",
              "description": "Operational Band V670"
            },
            {
              "name": "V708",
              "common_name": "red-edge",
              "description": "Operational Band V708"
            },
            {
              "name": "N740",
              "common_name": "red-edge",
              "description": "Operational Band V740"
            },
            {
              "name": "N753",
              "common_name": "red-edge",
              "description": "Operational Band V753"
            },
            {
              "name": "N778",
              "common_name": "nir",
              "description": "Operational Band V778"
            }
          ],
          "raster:bands": [
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 781.29052734375,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992.9329833984375,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992.8497924804688,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 992,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 742.4866943359375,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 632.91748046875,
                "minimum": 0
              },
              "spatial_resolution": 125
            },
            {
              "nodata": 0,
              "data_type": "float32",
              "statistics": {
                "maximum": 590.13671875,
                "minimum": 0
              },
              "spatial_resolution": 125
            }
          ]
        }
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
            [
              125.08806295692507,
              9.364368559641449
            ],
            [
              125.08806295692507,
              10.496677916255502
            ],
            [
              126.01662343226049,
              10.496677916255502
            ],
            [
              126.01662343226049,
              9.364368559641449
            ],
            [
              125.08806295692507,
              9.364368559641449
            ]
          ]
        ]
      },
      "collection": "diwata-2",
      "properties": {
        "datetime": "2019-10-09T04:56:41Z",
        "platform": "Diwata-2",
        "proj:epsg": 3857,
        "instruments": [
          "Spaceborne Multispectral Imager (SMI)"
        ]
      },
      "stac_version": "1.0.0",
      "stac_extensions": [
        "https://stac-extensions.github.io/projection/v1.1.0/schema.json",
        "https://stac-extensions.github.io/eo/v1.1.0/schema.json",
        "https://stac-extensions.github.io/raster/v1.1.0/schema.json"
      ]
    }
  ],
  "links": [
    {
      "rel": "root",
      "type": "application/json",
      "href": "https://api.diwata-stac.philsa.gov.ph/"
    },
    {
      "rel": "self",
      "type": "application/json",
      "href": "https://api.diwata-stac.philsa.gov.ph/search?intersects=%7B%20%20%20%20%20%22type%22%3A%20%22Point%22%2C%20%20%20%20%20%22coordinates%22%3A%20%5B125.6%2C%2010.1%5D%20%20%20%7D&limit=10"
    }
  ]
}

```

The image URLs can be found in the Asset Objects of the Features in the FeatureCollection. For this test API, please use the  **top-of-atmosphere-reflectance** assets.

### References
1. ItemSearch STAC API: https://stac-utils.github.io/stac-server/#tag/Item-Search/operation/getItemSearch
