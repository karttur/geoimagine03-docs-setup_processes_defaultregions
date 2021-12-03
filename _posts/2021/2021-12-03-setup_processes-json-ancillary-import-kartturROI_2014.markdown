---
layout: article
title: ancillary-import-kartturROI_2014_v090.json
categories: setup_processes
excerpt:  Import global countries and continents as ancillary data
tags:: 
    - json/ancillary-import-kartturROI_2014
date: 2021-12-03
modified: 2021-12-03
comments: true
share: true
---

# json/ancillary import kartturROI 2014 (setup_processes)

###  Import global countries and continents as ancillary data

The json command file <span class='file'>ancillary-import-kartturROI_2014_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
    "system": "ancillary"
  },
  "period": {
    "startyear": 2014,
    "endyear": 2014,
    "timestep": "singleyear"
  },
  "process": [
    {
      "processid": "OrganizeAncillary",
      "overwrite": false,
      "parameters": {
        "importcode": "shp",
        "epsg": "4326",
        "orgid": "karttur",
        "dsname": "globalROI",
        "dsversion": "1.0",
        "accessdate": "20170320",
        "regionid": "globe",
        "regioncat": "globe",
        "dataurl": "",
        "metaurl": "",
        "title": "Global default regions",
        "label": "Global default regions based on countries and continents"
      },
      "srcpath": {
        "volume": ".",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srcraw": [
        {
          "country": {
            "datadir": "data/political",
            "datafile": "country_karttur_global_2014_tol@100m",
            "datalayer": "country",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "country-continent": {
            "datadir": "data/political",
            "datafile": "country-continent_karttur_global_2014_tol@100m",
            "datalayer": "country-continent",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "continent-subregions": {
            "datadir": "data/political",
            "datafile": "continent-subregions_karttur_global_2014_tol@1km",
            "datalayer": "continent-subregions",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "continents": {
            "datadir": "data/political",
            "datafile": "continents_karttur_global_2014_tol@1km",
            "datalayer": "continents",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "land": {
            "datadir": "data/political",
            "datafile": "land_karttur_global_2014_tol@1km",
            "datalayer": "land",
            "title": "Global landsmass",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "marine-countries": {
            "datadir": "data/political",
            "datafile": "marine-countries_karttur_2014_0",
            "datalayer": "marine-countries",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "marine-continent-countries": {
            "datadir": "data/political",
            "datafile": "marine-continent-countries_karttur_2014_0",
            "datalayer": "marine-continent-countries",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "marine-continent-subregions": {
            "datadir": "data/political",
            "datafile": "marine-continent-subregions_karttur_2014_0",
            "datalayer": "marine-continent-subregions",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        },
        {
          "marine-continents": {
            "datadir": "data/political",
            "datafile": "marine-continents_karttur_2014_0",
            "datalayer": "marine-continents",
            "title": "Global countries (with iso-codes)",
            "label": "Cleaned vectors from ShareGeo representing global countries for 2014"
          }
        }
      ],
      "dstcomp": [
        {
          "country": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "country",
            "prefix": "country",
            "suffix": "0",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768",
            "masked": "Y",
            "measure": "N"
          }
        },
        {
          "country-continent": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "country-continent",
            "prefix": "country-continent",
            "suffix": "tol@100m",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        },
        {
          "continent-subregions": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "continent-subregions",
            "prefix": "continent-subregions",
            "suffix": "tol@1km",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        },
        {
          "continents": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "continents",
            "prefix": "continents",
            "suffix": "tol@1km",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        },{
          "land": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "land",
            "prefix": "land",
            "suffix": "tol@1km",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        },
        {
          "marine-countries": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-countries",
            "prefix": "marine-countries",
            "suffix": "0",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        },
        {
          "marine-continent-countries": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-continent-countries",
            "prefix": "marine-continent-countries",
            "suffix": "0",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        },
        {
          "marine-continent-subregions": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-continent-subregions",
            "prefix": "marine-continent-subregions",
            "suffix": "0",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        },
        {
          "marine-continents": {
            "masked": "Y",
            "measure": "N",
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-continents",
            "prefix": "marine-continents",
            "suffix": "0",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "-32768"
          }
        }
      ]
    }
  ]
}
```
