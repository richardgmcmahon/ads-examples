# Examples of how to use the ADS API

## Search Facet Plots

A small tool to plot the search facet plots that are found on the ADS search results page:

![Search example page](https://raw.githubusercontent.com/jonnybazookatone/ads-examples/master/search_facet/ui_example.png)

The tool allows you to create metrics for a set of bibcodes in two ways:
  i. via ORCiD iD
  ii. via a generic ADS query

If you want to preseve the plots, you can either save them to disc as an image, or in CSV format.

Note: this tool is not limited by the number of bibcodes you send it, unlike the metrics service on the ADS user interface. To run on an unlimited set of bibcodes, you should play with the following two parameters:
  i. `--rows`: number of items returned in a single request (max: 2000)
  ii. `--max-pages`: number of times to iterate over the rows returned

For example, `--rows 2000` and `--max-pages 10` will allow the tool to work for upto `2000*10=20,000` bibcodes (if the query returns that many)

Example usage:
```
python plot_search.py --orcid 0000-0001-8043-4965 --plot -f png --save-to-file csv
```

Makes plots like this:

![Search example page](https://raw.githubusercontent.com/jonnybazookatone/ads-examples/master/search_facet/example.png)