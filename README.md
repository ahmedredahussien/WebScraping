# Sprints Web Scrapping Lab
## Web scrapping using Scrapy and Beautiful Soup
### Scrapy:
> Scrapy is an open-source web crawling framework for Python. It facilitates the extraction of data from websites and supports robust, efficient, and flexible scraping. With built-in features like middleware and pipelines, Scrapy provides a comprehensive solution for web scraping tasks.

#### Scrapy Installation Steps
```bash
pip install scrapy
scrapy startproject myscrapyproject
cd myscrapyproject
scrapy genspider myspider https://en.wikipedia.org/wiki/Python_(programming_language)
scrapy crawl myspider
```

#### Scrapy export to different file formats
```bash
scrapy crawl myspider -o output.json
scrapy crawl myspider -o output.csv
scrapy crawl myspider -o output.xml
```

#### Scrapy Shell
```bash
scrapy shell https://en.wikipedia.org/wiki/Python_(programming_language)

>>> response.css('title::text').get()
>>> response.css('#firstHeading > span::text').get()
>>> response.css('#firstHeading').get()
>>> response.css('div#mw-content-text > div.mw-content-ltr.mw-parser-output > p:nth-child(6)').get()
>>> response.css('div#mw-content-text > div.mw-content-ltr.mw-parser-output > p').getall()
>>> response.css('div#mw-content-text > div.mw-content-ltr.mw-parser-output > p').getall()[4]
>>> response.css('div#mw-content-text > div.mw-content-ltr.mw-parser-output > p').getall()[4].strip().replace('\n', '')
>>> response.css('div#mw-content-text > div.mw-content-ltr.mw-parser-output > p').getall()[4].strip().replace('\n', '')
```

### Beautiful Soup:
> Beautiful Soup is a Python library for pulling data out of HTML and XML files. It provides Pythonic idioms for iterating, searching, and modifying the parse tree. Beautiful Soup transforms complex HTML documents into a tree of Python objects, simplifying web scraping tasks by offering intuitive methods to navigate and search the parsed content.

#### Beautiful Installation Steps
```bash
pip install requests beautifulsoup4
```

### Install requirments file for python modules/libraries
```bash
pip install -r requirements.txt
```

---

## Git Commands
### initial push
```bash
git init
git remote add origin https://github.com/ahmedredahussien/sprints-webscrapping.git
git add .
git commit -m "Initial commit"
git pull origin master --allow-unrelated-histories
> Normal first time push : 
git push -u origin master
```

### OnGoing changes
```bash
git checkout -b my-feature
> Optional in case that its new file:
 git add README.md
git commit README.md -m "add git steps to feature branch"" 
> Normal commit push after 1st time :  
git push origin my-feature
```


### After meging with master
```bash
git checkout master
git merge my-feature
git push origin master
> Normal delete :
git branch -d feature/my-feature
> Force delete :
git branch -D feature/my-feature
```

### Force push with overwrite  : 
```bash
git push -u --force origin master
```

## CLoning and exiting repository
```bash
git clone https://github.com/ahmedredahussien/WebScraping.git WebScraping
```

### Force overwrite my local changes from remote version : 
```bash
git reset --hard origin/master
```
Direct Change to Master

changed on server

