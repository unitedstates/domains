This project is an attempt to crawl the homepage of every .gov site (e.g. www.state.gov) for all of the hyperlinks in its source code.  

This is an active, open source project that would welcome any suggestions or improvements.  

### Wget terminal query 

````
wget -m -rH -l 1 -D.gov --input domain-list.txt 2>&1 | grep '^--' | awk '{ print $3 }' | grep -v '\.\(css\|js\|png\|gif\|jpg\|JPG\)$' > urls.txt
````

Details: 
* Using wget (wget)
* Mirroring the sites (-m)
* Recursive, spanning any host (-rH)
* Depth of 1 level (-l 1)
* Limited to only .gov domains (-D.gov)
* Read URLs from a file (--input domain-list.txt)
...

### Methodology

Stage 1:  
  
* Take the [federal .gov export](https://github.com/GSA/data/blob/gh-pages/dotgov-domains/current-federal.csv).  I used this snapshot.  
* Divide these domains into a set of categories, resulting in this file. 
* ...

Stage 2:  
  
...  
  
