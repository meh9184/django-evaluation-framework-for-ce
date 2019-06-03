# django-evaluation-framework-for-ce
Web Content Extraction 연구의 성능 평가에 대한 resource를 제공해주는 REST API

This project is about benchmarking and evaluating existing content extraction tools on their abilities to extract the contents from web pages. It provides:

> (1) a benchmark generator   
> (2) a benchmark  
> (3) a evaluation with meaningful evaluation criteria  

## The Benchmark Generator
+ Construct benchmark pages randomly generated from sites refered to [*www.alexa.com*](https://www.alexa.com/) using the [Random Page Selector](benchmark-generator/RandomPageSelector).
+ Downlaod the pages in MHT format using [Page Downloader](benchmark-generator/PageDownloader)
+ Construct answers using the [Answer Set Manager](benchmark-generator/PageDownloader)

For more details and usage, see [`benchmark-generator/`](benchmark-generator).

## The Benchmark
+ Consists of 500 pages randomly selected from [*www.alexa.com*](https://www.alexa.com/) and each answer generated using the benchmark generated above.
+ Consist of Content Extracton tool or implementation of top papers.
+ Consist of Evaluation metrics.

For more details, see [`benchmark/`](benchmark).

## The Evaluation
+ assesses the following 3 content extraction tools (and top paper content extraction):
[PDFExtract](https://github.com/elacin/PDFExtract), [Grobid](https://github.com/kermitt2/grobid), [Icecite](https://github.com/ckorzen/icecite).
+ provides meaningful evaluation criteria in order to assess the semantic abilities of a tool on identifying (1) *DOM tree similarity*, (2) the *are intersection*, and (3) *word/tag token distance*.

For more details, see [`evaluation/`](evaluation).

## Visualization

+ Main Page
<kbd>
  <div width='80%'>
    <img src='./screenshots/screenshot1.jpg'>
  </div>
</kbd>
<br><br>

+ Performance Compare Page
<kbd>
  <div width='80%'>
    <img src='./screenshots/screenshot2.jpg'>
  </div>
</kbd>
