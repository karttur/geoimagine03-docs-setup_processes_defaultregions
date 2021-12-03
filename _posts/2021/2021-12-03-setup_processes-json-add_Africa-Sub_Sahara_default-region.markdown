---
layout: article
title: add_Africa-Sub_Sahara_default-region_v090.json
categories: setup_processes
excerpt:  Adds African Sub-sahara region to the db
tags:: 
    - json/add_Africa-Sub_Sahara_default-region
date: 2021-12-03
modified: 2021-12-03
comments: true
share: true
---

# json/add Africa Sub Sahara default region (setup_processes)

###  Adds African Sub-sahara region to the db

The json command file <span class='file'>add_Africa-Sub_Sahara_default-region_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
  "process": [
    {
      "processid": "DefaultRegionFromCoords",
      "overwrite": false,
      "parameters": {
        "regioncat": "subcontinent",
        "regionid": "africasubsahara",
        "regionname": "Africa South of Sahara",
        "parentid": "africa",
        "parentcat": "continent",
        "stratum": "4",
        "minx": -16,
        "miny": -35.2,
        "maxx": 52,
        "maxy": 9.9999,
        "version": "1.0",
        "title": "Sub-saharan Africa",
        "label": "Africa South of the Sahara."
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    }
  ]
}
```
