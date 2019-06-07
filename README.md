This repository has the data and code developed for a project assessing github usage in pubmed papers. This work was (mostly) completed during OHBM 2019 hackathon.

The data directory contains a series of csv files that describe basic details of the pubmed papers. These papers can be obtained at the [BioC API](https://www.ncbi.nlm.nih.gov/research/bionlp/APIs/BioC-PubMed/). 

Because getting papers from the API takes a while, you can also download a subset of fulltext papers from [this googledrive link](https://drive.google.com/open?id=1QhsJ5lpmOZpZJImwyOlbHRWBYslP3BiD) (large-ish download. ~300mb). All of these papers are ones that contain the text string `github`. In the original corpus, there are about 20k papers that contain matches to this string. At present, the zipped directory contains ~14k. Each file in this zip directory contains 100 papers as a list of json objects and can be read as below:

```
with open('git_papes/papes_0.txt') as infile:
	dat = json.load(infile)
```