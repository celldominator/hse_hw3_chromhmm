# hse_hw3_chromhmm

### Google Colab ноутбук со списком всех запущенных команд и бонусным заданием: 
https://colab.research.google.com/drive/1oeW41oJck-0Jq5DaYChyV3Y2Evw74Lhl?usp=sharing 

Для анализа использовалась клеточная линия HSMM (Human Skeletal Muscle Myoblasts), потому что bam-файлов для прошлой MCF-7 нет. 

### Таблица гистоновых меток
Клеточная линия | Гистоновая метка | Имя файла | Файл с контролем 
| --- | --- | --- | ---
HSMM|H3k27ac|H3k27acStdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k27me3|H3k27me3StdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k36me3|H3k36me3StdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k4me1|H3k4me1StdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k4me2|H3k4me2StdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k4me3|H3k4me3StdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k79me2|H3k79me2StdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k9ac|H3k9acStdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H3k9me3|H3k9me3StdAlnRep1.bam|ControlStdAlnRep1.bam
HSMM|H4k20me1|H4k20me1StdAlnRep1.bam|ControlStdAlnRep1.bam

# Выдача ChromHMM
|![HSMM_10_RefSeqTSS_neighborhood](https://user-images.githubusercontent.com/60548614/160277728-52f94d61-5ab6-4b07-85c7-3adc3fe15baf.png)|![HSMM_10_RefSeqTES_neighborhood](https://user-images.githubusercontent.com/60548614/160277744-c76ac96c-1e75-4512-9ae9-f4130e85eaa1.png)|
| ------------- | ------------- |

|![transitions_10](https://user-images.githubusercontent.com/60548614/160277843-af90a78c-f313-466b-bfff-f6e2dd4467d8.png)|![emissions_10](https://user-images.githubusercontent.com/60548614/160277850-82ae74f2-5401-4e8e-84dc-b87ac2060942.png)|![HSMM_10_overlap](https://user-images.githubusercontent.com/60548614/160277856-9ab0596d-48fa-47b6-b137-be88ce39ab02.png)|
| ------------- | ------------- | ------------- |


