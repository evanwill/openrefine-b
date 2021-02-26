---
title: Power tool for Messy Data
nav: Data
---

Refine can handle all sorts of data from all sorts of sources:

- **Import formats:** TSV, CSV, custom separator, Excel, ODF spreadsheet, XML, JSON, RDF, Google Sheets, MARC...
- **Import sources:** local file, archive (zip), URL, clipboard, database, or Google Sheets
- **Output formats:** TSV, CSV, HTML, Excel, ODF spreadsheet, SQL, Wikidata, RDF schema, or custom template

The data is imported *without* changing the original source--a new copy is saved in an optimized format in the Refine working directory.
Once imported, the data is represented as tabular, using this basic terminology: 

{% include figure.html img="table.png" alt="table parts" width="100%" %}

Refine is efficient enough to provide comfortable performance up to 100,000's of rows (although, you may want to [increase memory allocated to Java](https://github.com/OpenRefine/OpenRefine/wiki/FAQ:-Allocate-More-Memory){:target="_blank"}).

## Messy Data 

Inconsistent formats, unnecessary white space, extra characters, typos, etc... 
Messy data is the bane of analysis! 
Each column contains exactly the same info:

| 2015-10-14 | $1,000 | ID |
| 10/14/2015 | 1000 | I.D. |
| 10/14/15 | 1,000 | US-ID |
| Oct 14, 2015 | 1000 dollars | idaho |
| Wed, Oct 14th | US$1000 | Idaho, |
| 42291 | $1k | Ihaho |

Multi-valued cells limit ability to manipulate, clean, and use the data:

| “Using OpenRefine by Ruben Verborgh and Max De Wilde, September 2013” | | |
| "University of Idaho, 875 Perimeter Drive, Moscow, ID, 83844, p. 208-885-6111, info@uidaho.edu" | | |

Luckily, Refine provides powerful visualizations and tools to discover these types of data issues, then isolate and fix them.
