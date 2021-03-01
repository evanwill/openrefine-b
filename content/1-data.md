---
title: Power tool for Messy Data
nav: Data
---

One of Refine's strengths is the flexibility to handle all sorts of data from all sorts of sources:

{% capture formats %}
<span class="term">Import formats:</span> CSV, TSV, custom separator, Excel, ODF spreadsheet, XML, JSON, RDF, Google Sheets, MARC, line-based text...

<span class="term">Import sources:</span> local file(s), archive (zip), URL, clipboard, database, or Google Sheets.

<span class="term">Output formats:</span> TSV, CSV, HTML, Excel, ODF spreadsheet, SQL, Wikidata, RDF schema, or custom template...
{% endcapture %}
{% include card.html text=formats %}

Refine imports the data *without* changing the original source, saving a copy using an optimized format in the "workspace directory" on your computer.
Importantly, Refine is *not* a cloud based service, no data is sent off your computer during this process (see [where data is stored](https://docs.openrefine.org/manual/installing#set-where-data-is-stored) and [data privacy FAQ](https://openrefine.org/privacy.html)).

Once imported, Refine's interface represents the data in a tabular grid, using this basic terminology: 

{% include figure.html img="refine-terms.png" alt="Refine row, column, cell labelled" %}

Refine is efficient enough to provide comfortable performance up to 100,000's of rows.
For very large data sets, you may want to [increase memory allocation](https://docs.openrefine.org/manual/installing#increasing-memory-allocation){:target='_blank' rel='noopener'}.

## Messy Data 

Inconsistent formats, unnecessary white space, extra characters, typos, etc... 
Messy data is the bane of analysis! 

For example, each column contains exactly the same info:

| 2015-10-14 | $1,000 | ID |
| 10/14/2015 | 1000 | I.D. |
| 10/14/15 | 1,000 | US-ID |
| Oct 14, 2015 | 1000 dollars | idaho |
| Wed, Oct 14th | US$1000 | Idaho, |
| 42291 | $1k | Ihaho |
{:.table .table-bordered}

Multi-valued cells limit ability to manipulate, clean, and use the data:

| “Using OpenRefine by Ruben Verborgh and Max De Wilde, September 2013” | | |
| "University of Idaho, 875 Perimeter Drive, Moscow, ID, 83844, p. 208-885-6111, info@uidaho.edu" | | |
{:.table .table-bordered}

Luckily, Refine provides powerful visualizations and tools to discover, isolate, and fix these types of data issues.
