# imdbExt
IMDB movie database using Golang

imdbExt downloads data from datasets.imdbws.com, currently provided by imdb. These are the subsets of IMDb data that are available for personal and non-commercial use. Each dataset is gzipped, TSV (tab-separated-values) formatted file. The first line of each file contains headers.

imdbExt downloads, extracts these file and inserts them into  Solr. Solr is capable of conducting full-text search. The latest version of Solr, 7.2.1 is tested with imdbExt.
### Tech
imdbExt uses a number of open source projects to work properly:

* [Golang] 
* [Solr] 

### Solr
In Solr, a core needs be created for imdbExt to work.

Create core:
```sh
$ solr create -c imdb
```

### Current Status :

<Partially Complete: Download, Decompression, Data insertion in Solr> 

<Under-development & Testing: API, User Input>

At this stage of development, imdbExt only downloads and extracts the necessary files and certain folders need to be created on the root directory of the project.

```sh
    files
    files/archive
    files/decompressed
    files/json
```
File download, decompression, data insertion are managed by imdbExt. Some parts of the project are hard-coded which will be refactored and fixed soon.

License
----
Apache-2.0

[//]: # 
   [Golang]: <https://golang.org/>
   [Solr]: <http://lucene.apache.org/solr/>
