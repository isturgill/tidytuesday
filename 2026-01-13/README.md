Original from https://github.com/rfordatascience/tidytuesday/blob/main/data/2026/2026-01-13/

# The Languages of Africa

This week we're exploring data about popular languages spoken on the African 
continent. The dataset this week comes from the [Languages of Africa](https://en.wikipedia.org/wiki/Languages_of_Africa) page on Wikipedia.

> The number of languages natively spoken in Africa is variously estimated (depending on the delineation of language vs. dialect) at between 1,250 and 2,100 and by some counts at over 3,000.

The dataset is rich with information on the number of languages spoken across 
the continent. Some of the questions that could be thought of include:

- Which country in Africa has the largest number of spoken languages?
- Which family of languages has the highest density of speakers?
- Are there any languages that cut across multiple countries?

Can't wait to see the kind of visualisations that can be created!

Thank you to Robert Muwanga, Data Enthusiast for curating this week's dataset.

## Data Dictionary

### `africa.csv`

|variable        |class     |description                           |
|:---------------|:---------|:-------------------------------------|
|language        |character |Name of popular African language. |
|family          |character |Group of languages with similar ancestry, having similar vocabulary, phonetics and grammar. |
|native_speakers |integer   |Number of known native speakers of the language. |
|country         |character |Country where this language is spoken. |

Cleaning script scrapes `https://www.worldometers.info/geography/how-many-countries-in-africa/` and `https://en.wikipedia.org/wiki/Languages_of_Africa` and recommends processing with R package `rvest`.
