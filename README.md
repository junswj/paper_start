# Research Paper Recommender

### :Review article recommender using PubMed API and Key word exraction from article titles using TF-IDF

During my research period, I have been switching my research topic very frequently, so I know how much the pain involves whenever they had to restart studying on the new field. Thus, I am currently developing the educational platform for junior researchers who just started research, using paper and keyword recommender system.

**Keyword recommendation:** Problem of current research article search engine is providing the keywords based on the keywords provided by article author, and mostly the one-word synonyms. I developed the keyword recommender using texts from titles and abstracts. Proper usage of ngram and TF-IDF provided intuitive keywords which gives information what to look up for the study.

**Paper recommendation:** Best way to learn new field is reading a good review article written by leading scientist in the field. Problem of finding the article by citation number is this will be highly biased towards the date of publication. First article published in the field gets most citation. This recommender provides list of review articles of most active researchers, based on publication number and citation recently, and displays most recently reviews by analyzing PubMed database. 