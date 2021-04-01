
     .----------------.  .----------------. 
    | .--------------. || .--------------. |
    | |    _______   | || |  _________   | |
    | |   /  ___  |  | || | |_   ___  |  | |
    | |  |  (__ \_|  | || |   | |_  \_|  | |
    | |   '.___`-.   | || |   |  _|  _   | |
    | |  |`\____) |  | || |  _| |___/ |  | |
    | |  |_______.'  | || | |_________|  | |
    | |              | || |              | |
    | '--------------' || '--------------' |
     '----------------'  '----------------' 

---

# Classifying Spanish se constructions: from bag of words to language models

This repository contains a reduced version of the SE-corpus, created for the paper [Classifying Spanish se constructions: from bag of words to language models](http://journal.sepln.org/sepln/ojs/ojs/index.php/pln/article/view/6331/3760) by Nuria Aldama and Álvaro Barbero, published at the SEPLN journal 2021 march edition. A notebook to reproduce the paper experiments is also included.

## SE-corpus reduced version

The SE-corpus reduced version (from now on SE-corpus) is composed of 2140 sentences that come from CORPES XXI. The sentence selection procedure starts picking up, from the whole CORPES XXI, every sentence that contains the word `se` and belongs to the news, leisure and daily life domain in the European Spanish variant. From the output of this retrieval query, 3000 sentences (complete SE-corpus) are randomly selected. Through the last filter, those sentences having more than one instance of `se` are eliminated. Summing-up, the corpus used to carry out this research is composed of 2140 sentences containing a single instance of `se`. The corpus is representative of the news, leisure and daily life domain in the European Spanish variant because it maintains real usage distribution of se constructions.

The annotation process is carried out following the next annotation criteria (examples follow)

* `se-mark`: cases of valency reduction (examples 6-9).
* `expl`: pure pronominal predicates or emphatic contexts (examples 4–5).
* `iobj`: `se` as indirect object of the main predicate (examples 1 and 3).
* `obj`: `se` as direct object of the main predicate (example 2).

Corpus examples

    (1)
    Se      lo     dije         a  Juan ayer      .
    Him-DAT it-ACC tell-PST.1SG to Juan yesterday .
    ‘I told it to Juan yesterday.’

    (2)
    Juan se          peina        .
    Juan himself-ACC comb-PRS.3SG .
    ‘Juan combs himself.’

    (3)	
    Ellos se       envían       cartas.
    They  them-DAT send-PRS.3PL letters.
    ‘They send letters to each other.’
        
    (4)
    Juan se  desmayó       de repente .
    Juan him faint-PST.3SG suddenly   .
    ‘Juan suddenly fainted.’

    (5)	
    Juan (se) comió       un bocadillo.
    Juan him  eat-PST.3SG a  sandwich.
    ‘Juan ate a sandwich.’
        
    (6)	
    El  jarrón se  rompió        .
    The vase   -   break-PST.3SG .
    ‘The vase broke.’

    (7)	
    La  camisa se lava         muy	bien .
    The shirt  -  wash-PRS.3SG very well .
    ‘The shirt washes very well.’
    
    (8)	
    Se buscan           camareros  .
    -  look.for-PRS.3PL bartenders .
    ‘Bartenders are required.’

    (9)	
    Se come        bien aquí .
    -  eat-PRS.3SG well here .
    ‘It's a good place to eat in here.'
    
### Corpus download

The corpus is available as three files:

* [se_classification_train.csv](./se_classification_train.csv): training split.
* [se_classification_test.csv](./se_classification_test.csv): test split.
* [se_classification_balanced_train.csv](./se_classification_balanced_train.csv): oversampled version of training split (for reproducing the paper experiments).

They are tab-separated files with header and one row per text. The columns are:

* **id**: unique identifier of the text.
* **text**
* **se_tag**: "se" usage, among `se-mark`, `expl`, `obj`, `iobj`.

## Notebook

The experiments can be reproduced by using the provided [multiclass_classification_SE.ipynb](./multiclass_classification_SE.ipynb) notebook. We recommend to use a [Google Colab](colab.research.google.com/) instance with GPU.

## Citing us

If you use this corpus or the notebook in this repository, please cite us as

    Aldama-García, N., Barbero, A. (2021). Classifying Spanish se constructions: from bag of words to language models. Procesamiento del Lenguaje Natural 66, 153-164. ISSN 1989-7553. DOI 10.26342/2021-66-13.

## Acknowledgements

We would like to thank Cristina Sánchez López and Amaya Mendikoetxea Pelayo for their help and dedication in the development of this study.

The authors acknowledge financial support from PID2019-106827GB-I00 / AEI / 10.13039/501100011033 and from the European Regional Development Fund and from the Spanish Ministry of Economy, Industry, and Competitiveness - State Research Agency, project TIN2016-76406-P (AEI/FEDER, UE).
