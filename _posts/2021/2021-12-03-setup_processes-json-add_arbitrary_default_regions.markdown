---
layout: article
title: add_arbitrary_default_regions_v090.json
categories: setup_processes
excerpt:  Add global default regions to the db
tags:: 
    - json/add_arbitrary_default_regions
date: 2021-12-03
modified: 2021-12-03
comments: true
share: true
---

# json/add arbitrary default regions (setup_processes)

###  Add global default regions to the db

The json command file <span class='file'>add_arbitrary_default_regions_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "postgresdb": {
    "db": "geoimagine"
  },
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
        "regionid": "global",
        "regionname": "Global",
        "regioncat": "global",
        "parentid": "globe",
        "parentcat": "globe",
        "epsg": "4326",
        "stratum": "1",
        "minx": -180,
        "miny": -90,
        "maxx": 180,
        "maxy": 90,
        "version": "1.0",
        "title": "Global region",
        "label": "Global region (entire global sphere)"
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
        "regionid": "globaltropics",
        "regionname": "Global tropics",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": -23.43705,
        "maxx": 180,
        "maxy": 23.43705,
        "version": "1",
        "title": "Global tropical region",
        "label": "Region between the tropics"
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
        "regionid": "northtropical",
        "regionname": "North Tropical zones",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": 0,
        "maxx": 180,
        "maxy": 23.43705,
        "epsg": "4326",
        "version": "1",
        "title": "Global norhtern tropical region",
        "label": "Region between the equator and north 23.5 degrees"
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
        "regionid": "southtropical",
        "regionname": "South Tropical zones",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": -23.43705,
        "maxx": 180,
        "maxy": 0,
        "epsg": "4326",
        "version": "1",
        "title": "Global southern tropical region",
        "label": "Region between the equator and south 23.5 degrees"
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
        "regionid": "northsubtropical",
        "regionname": "North Subtropical zone",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": 23.43705,
        "maxx": 180,
        "maxy": 40,
        "epsg": "4326",
        "version": "1",
        "title": "Global northern subtropical region",
        "label": "Region extending between the northern tropic (23.5 degrees) to 40 degrees north"
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
        "regionid": "southsubtropical",
        "regionname": "South Subtropical zone",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": -40,
        "maxx": 180,
        "maxy": -23.43705,
        "epsg": "4326",
        "version": "1",
        "title": "Global northern subtropical region",
        "label": "Region extending between the southern tropic (23.5 degrees) to 40 degrees south"
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
        "regionid": "pantropical",
        "regionname": "Global Pantropical zone",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": -40,
        "maxx": 180,
        "maxy": 40,
        "epsg": "4326",
        "version": "1",
        "title": "Global panropical region",
        "label": "Region including the tropics and subtropics (between 40 degrees north and south)"
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
        "regionid": "trmm",
        "regionname": "TRMM tropical zone",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": -50,
        "maxx": 180,
        "maxy": 50,
        "epsg": "4326",
        "version": "1",
        "title": "TRMM precipitation coverage region",
        "label": "Region for the TRMM data products"
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
        "regionid": "northtemperate",
        "regionname": "North Temperate zone",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": 40,
        "maxx": 180,
        "maxy": 66.565325,
        "epsg": 4326,
        "version": "1",
        "title": "Global northern temperate zone",
        "label": "Region extending between 40 degrees north and the arctic circles (66.5 degrees)"
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
        "regionid": "southtemperate",
        "regionname": "South Temperate zone",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": -66.565325,
        "maxx": 180,
        "maxy": -40,
        "epsg": "4326",
        "version": "1",
        "title": "Global southern temperate zone",
        "label": "Region extending between 40 degrees south and the antarctic circles (66.5 degrees)"
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
        "regionid": "arctic",
        "regionname": "Arctic",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": 66.565325,
        "maxx": 180,
        "maxy": 90,
        "epsg": "4326",
        "version": "1",
        "title": "Global arctic zone",
        "label": "Region extending from the arctic circles (66.5 degrees) to the North Pole"
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
        "regionid": "antarctic",
        "regionname": "Antarctic",
        "parentid": "globe",
        "parentcat": "globe",
        "stratum": "1",
        "minx": -180,
        "miny": -90,
        "maxx": 180,
        "maxy": -66.565325,
        "epsg": "4326",
        "version": "1",
        "title": "Global antarctic zone",
        "label": "Region extending from the antarctic circles (66.5 degrees) to the South Pole"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    }
  ]
}
```
