---
layout: article
title: add_ease2n_hydro_regions_v090.json
categories: setup_processes
excerpt:   Add Arctic hydrological basin regions for ease2n
tags:: 
    - json/add_ease2n_hydro_regions
date: 2021-12-03
modified: 2021-12-03
comments: true
share: true
---

# json/add ease2n hydro regions (setup_processes)

###   Add Arctic hydrological basin regions for ease2n

The json command file <span class='file'>add_ease2n_hydro_regions_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
            "regioncat": "basin",
            "regionid": "nordichydro_ease2n",
            "regionname": "nordichydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": 234000,
            "miny": -4653000,
            "maxx": 2124000,
            "maxy": -1773000,
            "version": "1.0",
            "title": "nordichydro_ease2n hydro ease2n",
            "label": "nordichydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "nordichydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "greenlandhydro_ease2n",
            "regionname": "greenlandhydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": -3123000,
            "miny": -2808000,
            "maxx": -153000,
            "maxy": -288000,
            "version": "1.0",
            "title": "greenlandhydro_ease2n hydro ease2n",
            "label": "greenlandhydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "greenlandhydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "cahydro_ease2n",
            "regionname": "cahydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": -5373000,
            "miny": -2853000,
            "maxx": -2853000,
            "maxy": 297000,
            "version": "1.0",
            "title": "cahydro_ease2n hydro ease2n",
            "label": "cahydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "cahydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "alaskahydro_ease2n",
            "regionname": "alaskahydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": -4842000,
            "miny": -432000,
            "maxx": -702000,
            "maxy": 3168000,
            "version": "1.0",
            "title": "alaskahydro_ease2n hydro ease2n",
            "label": "alaskahydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "alaskahydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "kolymahydro_ease2n",
            "regionname": "kolymahydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": -855000,
            "miny": 1332000,
            "maxx": 2025000,
            "maxy": 4032000,
            "version": "1.0",
            "title": "kolymahydro_ease2n hydro ease2n",
            "label": "kolymahydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "kolymahydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "lenahydro_ease2n",
            "regionname": "lenahydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": 1422000,
            "miny": 540000,
            "maxx": 4032000,
            "maxy": 2880000,
            "version": "1.0",
            "title": "lenahydro_ease2n hydro ease2n",
            "label": "lenahydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "lenahydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "yieniseyhydro_ease2n",
            "regionname": "yieniseyhydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": 2043000,
            "miny": -441000,
            "maxx": 5013000,
            "maxy": 1809000,
            "version": "1.0",
            "title": "yieniseyhydro_ease2n hydro ease2n",
            "label": "yieniseyhydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "yieniseyhydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "obhydro_ease2n",
            "regionname": "obhydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": 1809000,
            "miny": -2097000,
            "maxx": 4959000,
            "maxy": 423000,
            "version": "1.0",
            "title": "obhydro_ease2n hydro ease2n",
            "label": "obhydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "obhydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "dvinahydro_ease2n",
            "regionname": "dvinahydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": 1746000,
            "miny": -2745000,
            "maxx": 2736000,
            "maxy": -1665000,
            "version": "1.0",
            "title": "dvinahydro_ease2n hydro ease2n",
            "label": "dvinahydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "dvinahydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      },
      {
         "processid": "DefaultRegionFromCoords",
         "overwrite": false,
         "parameters": {
            "regioncat": "basin",
            "regionid": "arcticoceanhydro_ease2n",
            "regionname": "arcticoceanhydro_ease2n hydro ease2n",
            "parentcat": "global",
            "parentid": "global",
            "stratum": "1",
            "minx": 234000,
            "miny": -1845000,
            "maxx": 2124000,
            "maxy": 1575000,
            "version": "1.0",
            "title": "arcticoceanhydro_ease2n hydro ease2n",
            "label": "arcticoceanhydro_ease2n hydrological region for ease2n."
         },
         "dstpath": {
            "volume": "DEMDATA"
         },
         "dstcomp": [
            {
               "arcticoceanhydro_ease2n": {
                  "masked": "N",
                  "measure": "N",
                  "source": "karttur",
                  "product": "pubroi",
                  "content": "roi",
                  "layerid": "hydroreg",
                  "prefix": "hydroreg",
                  "suffix": "v01-ease2n",
                  "dataunit": "boundary",
                  "celltype": "vector",
                  "cellnull": "0"
               }
            }
         ]
      }
   ]
}
```
