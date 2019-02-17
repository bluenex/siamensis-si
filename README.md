# Siamensis SI Data

## Introduction

In Thailand, there is a community website for naturalist called [Siamensis (siamensis.org)](http://www.siamensis.org) founded by, Nonn Panitvong, a naturalist businessman. This website is one of the best place for knowledge exchange and biodiversity discussion.. in the past. Nowadays it is pretty hard to keep running on a webboard and people tend to come over to social network service instead. However, there is an invaluable source of information which is only available on the website, it is Species Index (SI).

There is a world species index database called [The Catalogue of Life](http://www.catalogueoflife.org/col/), but they are different in many ways. The most distinctive point is that, Siamensis SI is authored by Thai, hence species listed on it are reportedly found in Thailand (whether or not they are re-found). This makes Siamensis SI unique and should be reserved for the next generation.

However, it seems that Siamensis SI have not been yet used at its best value. We can explain this in many reasons, one of them is that _there is no API available_. Knowledge available for public in the present has choices to access, e.g., open data or API. This scraper and open data project is started to make the SI more accessible.

## Objectives

- To make Siamensis SI data more accessible than just a web.

## Usage

I have scraped all the data and saved in `.json` format so that it is easy to import with `pandas` and Python. To import into Python you can run:

```py
import pandas as pd

si_data = pd.read_json('si-data.json)
```

## Example

You can see example in [si-stats.ipynb](ipynb/si-stats.ipynb).

## Licenses

Even though the data is meant to publicize but not for images in it. All images in the data are not supposed to use for commercial and also not to use anywhere with out contacting to the image owner. License used for the images is `CC BY-NC-ND`.

## FAQ

**Why data is not saved as `.csv`?**

- Because some of the cells contain list which is not automatically parsed as type `list` in Python when use `pd.read_csv()`.