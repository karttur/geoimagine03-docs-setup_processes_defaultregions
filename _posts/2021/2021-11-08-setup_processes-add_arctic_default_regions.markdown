---
layout: article
title: add_arctic_default_regions_v090.json
categories: setup_processes
excerpt:  Add global arctic regions to the db
tags:: 
    - add_arctic_default_regions
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# add arctic default regions (setup_processes)

###  Add global arctic regions to the db

The json command file <span class='file'>add_arctic_default_regions_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "system"
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
        "regionid": "arcticdem",
        "regionname": "Arctic circumpolar DEM",
        "parentid": "globe",
        "parentcat": "globe",
        "epsg": "4326",
        "stratum": "1",
        "minx": -180,
        "miny": 58,
        "maxx": 180,
        "maxy": 90,
        "version": "1.0",
        "title": "Global arctic DEM",
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
        "regionid": "arcticland",
        "regionname": "Arctic circumpolar land",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": 58,
        "maxx": 180,
        "maxy": 84,
        "version": "1",
        "title": "Global arctic land zone",
        "label": "Region covering arctic cricumpolar land masses extending from 58 to 84 degrees north."
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
        "regionid": "arcticdemext",
        "regionname": "Arctic circumpolar DEM",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": 50,
        "maxx": 180,
        "maxy": 90,
        "version": "1",
        "title": "Global arctic extended DEM",
        "label": "Region covering 50 to 90 degrees north, coinciding with the extended region of the Arctic DEM."
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    }
  ]
}
```
