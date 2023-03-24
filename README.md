
## Setup
From a Unix terminal:
```
python3 -m venv .python3
source ./python3/bin/activate
pip install -r requirements.txt
```
To run the notebook:
```
jupyter-lab
```

To exit:
```
deactivate
```
## Generate list of stories from GH project
The following commands require SPARQL Anything CLI.
```
java -jar sparql-anything-0.8.1.sparql -q queries/list-stories.sparql -o data/stories.csv
```
## Extract competency questions from Stories
```
java -jar sparql-anything-0.8.1.sparql -q queries/competency-questions.sparql -v data/stories.csv |sort|uniq > data/competency-questions.csv
```
And then manually move the csv header to the top!





