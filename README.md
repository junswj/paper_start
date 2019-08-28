# Research Paper Recommender

### :Review article recommender using PubMed API and Key word exraction from article titles using TF-IDF

During my research period, I have been switching my research topic very frequently, so I know how much the pain involves whenever they had to restart studying on the new field. Thus, I am currently developing the educational platform for junior researchers who just started research, using paper and keyword recommender system.

**Keyword recommendation:** Problem of current research article search engine is providing the keywords based on the keywords provided by article author, and mostly the one-word synonyms. I developed the keyword recommender using texts from titles and abstracts. Proper usage of ngram and TF-IDF provided intuitive keywords which gives information what to look up for the study.

**Paper recommendation:** Best way to learn new field is reading a good review article written by leading scientist in the field. Problem of finding the article by citation number is this will be highly biased towards the date of publication. First article published in the field gets most citation. This recommender provides list of review articles of most active researchers, based on publication number and citation recently, and displays most recently reviews by analyzing PubMed database. 

#### Key words provided by author

```Python
key_paper_lst=key_from_papers(papers)
key_paper_lst.value_counts().head(20)
```
    bioactive glass            141
    bioactive compounds        114
    bioactive peptides          54
    bone regeneration           33
    bioactivity                 31
    antioxidant activity        23
    scaffold                    23
    bioactive                   22
    bioactive glasses           21
    angiogenesis                19
    strontium                   19
    antioxidant                 19
    tissue engineering          18
    bioactive peptide           18
    cytotoxicity                17
    scaffolds                   16
    bone tissue engineering     16
    osteogenesis                16
    mechanical properties       15
    hydroxyapatite              15
    Name: key word from papers, dtype: int64

#### Key Words from Title

```Python
key_title=title_key(papers)
key_title[:20]
```
    tissue engineering       7.418839
    bone tissue              5.608003
    bone regeneration        5.454114
    mesoporous glass         5.142716
    antioxidant activity     5.029007
    mass spectrometry        4.581099
    derived peptides         4.420087
    glass nanoparticles      4.402085
    glass scaffolds          4.288539
    compounds antioxidant    4.107077
    extraction compounds     3.715036
    scaffolds bone           3.529002
    stem cells               3.463278
    liquid chromatography    3.339055
    natural products         3.333138
    glass based              3.149904
    containing glass         3.146186
    mechanical properties    2.952051
    ultrasound assisted      2.790998
    composite scaffolds      2.787624
    dtype: float64

#### Key Words from Abstract

```Python
key_abstract=Abstract_key(papers)
key_abstract[:20]
```
    tissue engineering       4.688455
    antioxidant activity     4.455011
    bone regeneration        4.331385
    bone tissue              4.081456
    mechanical properties    3.919917
    body fluid               3.479476
    anti inflammatory        3.348498
    simulated body           3.313052
    present study            3.296120
    aim study                3.155519
    stem cells               3.103526
    sol gel                  3.087326
    glass nanoparticles      2.968362
    bone defects             2.843119
    fatty acids              2.754742
    natural products         2.712150
    liquid chromatography    2.693476
    mass spectrometry        2.618745
    electron microscopy      2.532576
    scanning electron        2.527362
    dtype: float64