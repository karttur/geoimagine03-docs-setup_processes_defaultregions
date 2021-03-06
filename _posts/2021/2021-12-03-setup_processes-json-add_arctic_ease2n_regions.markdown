---
layout: article
title: add_arctic_ease2n_regions_v090.json
categories: setup_processes
excerpt:  Add global arctic regions in EASE-grid 6931 to the db
tags:: 
    - json/add_arctic_ease2n_regions
date: 2021-12-03
modified: 2021-12-03
comments: true
share: true
---

# json/add arctic ease2n regions (setup_processes)

###  Add global arctic regions in EASE-grid 6931 to the db

The json command file <span class='file'>add_arctic_ease2n_regions_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "ease2n"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "DefaultRegionFromCoords",
      "overwrite": false,
      "parameters": {
        "regioncat": "global",
        "regionid": "ease2n",
        "regionname": "system default region",
        "parentid": "global",
        "parentcat": "global",
        "epsg": 6931,
        "stratum": "1",
        "minx": -9000000,
        "miny": -9000000,
        "maxx": 9000000,
        "maxy": 9000000,
        "version": "1.0",
        "title": "system default region EASE-grid 6931",
        "label": "system default region for Northern circumpolar EASE-grid 6931."
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "DefaultRegionFromCoords",
      "overwrite": false,
      "parameters": {
        "regioncat": "global",
        "regionid": "northlandease2n",
        "regionname": "Northern circumpolar landmass EASE-grid 6931",
        "parentid": "global",
        "parentcat": "global",
        "epsg": 6931,
        "stratum": "1",
        "minx": -5400000,
        "miny": -5400000,
        "maxx": 5400000,
        "maxy": 4500000,
        "version": "1.0",
        "title": "Northern circumpolar landmass EASE-grid 6931",
        "label": "Tile fitted region for Northern circumpolar landmass EASE-grid 6931."
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "DefaultRegionFromCoords",
      "overwrite": false,
      "parameters": {
        "regioncat": "global",
        "regionid": "arcticdemease2n",
        "regionname": "Arctic circumpolar DEM EASE-grid 6931",
        "parentid": "globe",
        "parentcat": "globe",
        "epsg": 6931,
        "stratum": "1",
        "minx": -3500000,
        "miny": -3500000,
        "maxx": 3500000,
        "maxy": 4400000,
        "version": "1.0",
        "title": "Global arctic DEM in EASE-grid 6931",
        "label": "Region covering 60 to 90 degrees north, coinciding with the core region of the Arctic DEM."
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "DefaultRegionFromCoords",
      "overwrite": false,
      "parameters": {
        "regioncat": "global",
        "regionid": "nhemispherease2n",
        "regionname": "Northern hemisphere EASE-grid 6931",
        "parentid": "globe",
        "parentcat": "globe",
        "epsg": 6931,
        "stratum": "1",
        "minx": -9000000,
        "miny": -9000000,
        "maxx": 9000000,
        "maxy": 9000000,
        "version": "1.0",
        "title": "Northern hemisphere EASE-grid 6931",
        "label": "Northern hemisphere EASE-grid 6931."
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "DefaultRegionFromCoords",
      "overwrite": false,
      "parameters": {
        "regioncat": "global",
        "regionid": "panarcticease2n",
        "regionname": "Pan Arctic EASE-grid 6931",
        "parentid": "globe",
        "parentcat": "globe",
        "epsg": 6931,
        "stratum": "1",
        "minx": -4500000,
        "miny": -4500000,
        "maxx": 4500000,
        "maxy": 4500000,
        "version": "1.0",
        "title": "Pan Arctic EASE-grid 6931",
        "label": "Pan Arctic EASE-grid 6931."
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    }
  ]
}
```
