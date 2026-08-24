Original from https://github.com/rfordatascience/tidytuesday/blob/main/data/2026/2026-01-20

# Astronomy Picture of the Day (APOD) Archive

This week we're exploring the Astronomy Picture of the Day (APOD) archive.
APOD is a popular NASA website featuring daily astronomy related images with a scientific explanation.  
Each day a different image or photograph of our universe is featured, along with a brief explanation. 
This APOD archive contains image information from the 2007 - 2025, pulled together into the {astropic} R package.

- What types of objects are most common in the archive?
- Are any images posted more than once?

Thank you to [Erin Grand](https://github.com/eringrand) for curating this week's dataset.

## Data Dictionary
`apod.csv`

|variable        |class     |description                           |
|:---------------|:---------|:-------------------------------------|
|copyright       |character |The name of the copyright holder. |
|date            |Date |Date of image. |
|explanation     |character |The supplied text explanation of the image. |
|media_type      |character |The type of media (data) returned. May either be ‘image’ or ‘video’ depending on content. |
|title           |character |The title of the image. |
|url             |character |The URL of the APOD image or video of the day. |
|hdurl           |character |The URL for any high-resolution image for that day. Will be omitted in the response IF it does not exist originally at APOD. |

## Cleaning Script
Included with the data description; data already exists in a ready form in an R package.

```r
remotes::install_github("eringrand/astropic")

# Dataset inside the {{astropic}} R package on GitHub.
library(astropic)
library(dplyr)
data("hist_apod")

# Remove one column with constant values
apod <- hist_apod |> 
  select(-service_version)
```

## Data processing and analysis
Available at [tidytuesday_astronomy_apod.qmd](tidytuesday_astronomy_apod.qmd).
