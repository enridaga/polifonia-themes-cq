## Generate list of stories from GH project
```
fx -q queries/list-stories.sparql -o data/stories.csv
```
## Extract competency questions from Stories
```
fx -q queries/competency-questions.sparql -v data/stories.csv |sort|uniq > data/competency-questions.csv
```
And then manually move the csv header to the top

https://docs.google.com/spreadsheets/d/18ZS7G-XHDZRsrzOjWFEs_BFpLk37IdU9HGuwNIHrXog/edit?usp=sharing




