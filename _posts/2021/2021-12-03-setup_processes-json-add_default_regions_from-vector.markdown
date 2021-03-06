---
layout: article
title: add_default_regions_from-vector_v090.json
categories: setup_processes
excerpt:  Add countries, subregions and continents to the db
tags:: 
    - json/add_default_regions_from-vector
date: 2021-12-03
modified: 2021-12-03
comments: true
share: true
---

# json/add default regions from vector (setup_processes)

###  Add countries, subregions and continents to the db

The json command file <span class='file'>add_default_regions_from-vector_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "NAME",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "NAME",
        "vector_db_label": "CATEGORY"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "land": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "land",
            "prefix": "land",
            "suffix": "tol@1km",
            "volume": "DEMDATA",
            "ext": "shp"
          }
        }
      ],
      "dstcopy": [
        {
          "land": {
            "layerid": "land"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "NAME",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "NAME",
        "vector_db_label": "CATEGORY"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "continents": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "continents",
            "prefix": "continents",
            "suffix": "tol@1km",
            "volume": "DEMDATA",
            "ext": "shp"
          }
        }
      ],
      "dstcopy": [
        {
          "continents": {
            "layerid": "continents"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "NAME",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "NAME",
        "vector_db_label": "CATEGORY"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "continent-subregions": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "continent-subregions",
            "prefix": "continent-subregions",
            "suffix": "tol@1km"
          }
        }
      ],
      "dstcopy": [
        {
          "continent-subregions": {
            "layerid": "continent-subregions"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "ISO_A2",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "FORMALNAME",
        "vector_db_label": "TYPE"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "country": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "country",
            "prefix": "country",
            "suffix": "tol@100m"
          }
        }
      ],
      "dstcopy": [
        {
          "country": {
            "layerid": "country"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "CODE",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "FORMALNAME",
        "vector_db_label": "TYPE"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "country-continent": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "country-continent",
            "prefix": "country-continent",
            "suffix": "tol@100m"
          }
        }
      ],
      "dstcopy": [
        {
          "country-continent": {
            "layerid": "country-continent"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "CODE",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "NAME",
        "vector_db_label": "CATEGORY"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "marine-continents": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-continents",
            "prefix": "marine-continents",
            "suffix": "0"
          }
        }
      ],
      "dstcopy": [
        {
          "marine-continents": {
            "layerid": "marine-continents"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "CODE",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "NAME",
        "vector_db_label": "CATEGORY"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "marine-continent-subregions": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-continent-subregions",
            "prefix": "marine-continent-subregions",
            "suffix": "0"
          }
        }
      ],
      "dstcopy": [
        {
          "marine-continent-subregions": {
            "layerid": "marine-continent-subregions"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "CODE",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "FORMALNAME",
        "vector_db_label": "TYPE"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "marine-countries": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-countries",
            "prefix": "marine-countries",
            "suffix": "0"
          }
        }
      ],
      "dstcopy": [
        {
          "marine-countries": {
            "layerid": "marine-countries"
          }
        }
      ]
    },
    {
      "processid": "DefaultRegionFromVector",
      "parameters": {
        "vector_db_id": "CODE",
        "vector_db_name": "NAME",
        "vector_db_category": "CATEGORY",
        "vector_db_parentid": "PARENTNAME",
        "vector_db_parentcat": "PARENTCAT",
        "vector_db_stratum": "STRATUM",
        "version": "kt1",
        "vector_db_title": "FORMALNAME",
        "vector_db_label": "TYPE"
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "marine-continent-countries": {
            "source": "karttur",
            "product": "karttur",
            "content": "defaultregions",
            "layerid": "marine-continent-countries",
            "prefix": "marine-continent-countries",
            "suffix": "0"
          }
        }
      ],
      "dstcopy": [
        {
          "marine-continent-countries": {
            "layerid": "marine-continent-countries"
          }
        }
      ]
    }
  ]
}
```
