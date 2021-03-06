---
layout: article
title: add_region_categories_v090.json
categories: setup_processes
excerpt:  Add region categories to the db
tags:: 
    - json/add_region_categories
date: 2021-12-03
modified: 2021-12-03
comments: true
share: true
---

# json/add region categories (setup_processes)

###  Add region categories to the db

The json command file <span class='file'>add_region_categories_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
  "process": [
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "global",
        "stratum": 1,
        "parentcat": "globe",
        "title": "Global regions, apart from the earth itself",
        "label": "Global regions include regions that cover more than one continent, usually girdling the Earth."
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "pancontinent",
        "stratum": 2,
        "parentcat": "global",
        "title": "Continental landmasses",
        "label": "Pancontinental include Americas, Eurasia, Africa, Australia, Oceania and Antarctica."
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "panoceanic",
        "stratum": 2,
        "parentcat": "global",
        "title": "Panoceanic regions, covering more than one ocean",
        "label": "Panoceanic regions include the Arctic, North Atlantic, Indian, Pacific and Antarctic oceans."
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "continent",
        "stratum": 3,
        "parentcat": "pancontinent",
        "title": "The classical 7 continents",
        "label": "Continental include North America, South America, Europe, Asia, Africa, Oceania and Antarctica"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "marinecontinent",
        "stratum": 3,
        "parentcat": "global",
        "title": "The classical 7 continents, including marine regions",
        "label": "Marine Continental include North America, South America, Europe, Asia, Africa, Oceania and Antarctica"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "oceanic",
        "stratum": 3,
        "parentcat": "panoceanic",
        "title": "Oceanic regions, covering more than one ocean",
        "label": "Oceanic regions include the Arctic, North Atlantic, South Atlantic, Indian, North Pacific, South Pacific and Antarctic oceans ."
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "subcontinent",
        "stratum": 4,
        "parentcat": "continent",
        "title": "Regions with subcontinental coverage, covering more than one country",
        "label": "Subcontinental regions cover arbitrary regions, defined by e.g. political, climatic or topographic conditions"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "marinesubcontinent",
        "stratum": 4,
        "parentcat": "marinecontinent",
        "title": "Regions with subcontinental coverage, covering more than one country",
        "label": "Subcontinental regions cover arbitrary regions, defined by e.g. political, climatic or topographic conditions"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "suboceanic",
        "stratum": 4,
        "parentcat": "oceanic",
        "title": "Regions with suboceanic coverage, including enclosed seas",
        "label": "Suboceanic regions cover both defined enclosed seas as well as other oceanic regions falling within a single of the seven classical oceans"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "basin",
        "stratum": 5,
        "parentcat": "pancontinent",
        "title": "Regions with hydrological basin coverage",
        "label": "The basin region category contains the worlds hydrological basins (watersheds)"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "subbasin",
        "stratum": 6,
        "parentcat": "basin",
        "title": "Regions with hydrological subasin coverage",
        "label": "The subbasin region category contains subbasins of basins (watersheds)"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "sovereign",
        "stratum": 5,
        "parentcat": "global",
        "title": "Sovereign (composite) nation states",
        "label": "Sovereign (composite) nation states"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "country",
        "stratum": 6,
        "parentcat": "sovereign",
        "title": "Country",
        "label": "Country (usually with recognized iso-code)"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "marinecountry",
        "stratum": 6,
        "parentcat": "global",
        "title": "Country incl maritime area",
        "label": "Country incl maritime area (usually with recognized iso-code)"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "continentcountry",
        "stratum": 6,
        "parentcat": "subcontinent",
        "title": "Country, or part of country, falling within one of the classical 7 continents",
        "label": "Transcontinental countries are split into parts"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "marinecontinentcountry",
        "stratum": 6,
        "parentcat": "marinesubcontinent",
        "title": "Country, or part of country, falling within one of the classical 7 continents",
        "label": "Transcontinental countries are split into parts"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "state",
        "stratum": 7,
        "parentcat": "country",
        "title": "State",
        "label": "State as part of a country (countries with no states are set to country = state)"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "province",
        "stratum": 8,
        "parentcat": "state",
        "title": "Province within a country",
        "label": "Provinces as part of a state"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "district",
        "stratum": 9,
        "parentcat": "province",
        "title": "District within Province",
        "label": "District is an arbitrary political division used for designating regions within a province"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "community",
        "stratum": 10,
        "parentcat": "district",
        "title": "Community within dstrict",
        "label": "Community is an arbitrary political division used for designating regions within a district"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "quarter",
        "stratum": 11,
        "parentcat": "community",
        "title": "Quarter within community",
        "label": "Quarter is an arbitrary division used for designating regions within a community"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "domain",
        "stratum": 12,
        "parentcat": "*",
        "title": "Arbitrary spatial extent having any region of categories 0 to 11 as parentid",
        "label": "User defined but public region definition"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "tract",
        "stratum": 12,
        "parentcat": "*",
        "title": "Tract is a user defined region category (private or public) and can have any region of categories 0 to 11 as parentid",
        "label": "Tract is arbitrary defined by users, and can be kept private or made available for public use"
      },
      "system": {
        "srcsystem": "NA",
        "dstsystem": "system",
        "srcdivision": "NA",
        "dstdivision": "region",
        "srcepsg": 0,
        "dstepsg": 0
      }
    },
    {
      "processid": "RegionCategories",
      "overwrite": false,
      "parameters": {
        "regioncat": "site",
        "stratum": 13,
        "parentcat": "tract",
        "title": "Site is a user defined region category having tract as parentid",
        "label": "Site is arbitrary defined by users"
      }
    }
  ]
}
```
