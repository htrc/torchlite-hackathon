# Publication Place Map
## Use case
Undergrad students in a digital humanities are studying a bibliographic dataset derived from known items in the personal library of Victorian poetry Algernon Charles Swinburne. They are asked to analyze various attributes of the books, such as language, publication dates, genre, etc. For this task it will be useful to display places of publication on a date and the number of volumes from published in each place.

| Title                   | Publication Place Map |
| ----------------------------------       | ---  |
| **visualization type**                       |  map |
| **description**                          |  This widget will visualize the place of publication for all volumes in a workset on a map of the world, zoomed in to the area(s) of coverage.      |
| **Relevant extracted features field(s)** | `pubPlace`, `publisher`|

## Description
This proposed tool is basically a version of the existing “Mapping Contributor Data” widget, but uses place of publication data rather than creators’ birthplace data. Like the “Mapping Contributor Data,” parameters may allow a user to filter the displayed results by publication date (or other parameters). The size of the location indicators should increase to correspond with the number of volumes published in a particular location, e.g., London.


![image](images/mapping_contributor_data.png)

<figcaption style="">Mapping Contributor Data</figcaption>

Possible enhancement could include combining the Publication Place Map with a version of the existing “Publication Date Timeline“ or adding useful contextual data to the downloadable CSV data. For example, for each row of data, one might include columns containing arrays of `htid` and `title` values for the volumes published in a particular place.  

![image](images/publication_date_timeline.png)

<figcaption style="">Publication Date Timeline</figcaption>

## Extracted Features data points necessary
```
metadata
  htid
  title
  pubPlace
  pubDat
  publisher
```

## Tasks
- Write API call to grab metadata
- Write API call to get token data
- Code or edit code for a map on which locations may be plotted
- Code or edit code to limit plotted locations by range of publication dates
- Optionally: Integrate a publication date timeline and/or publisher data for a more comprensive “pubication data” analysis tool.

