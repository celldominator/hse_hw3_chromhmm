# hse_hw3_chromhmm

### Google Colab ноутбук со списком всех запущенных команд (в т. ч. бонусного задания): 
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

# Выдача ChromHMM (Pngs)
|![HSMM_10_RefSeqTSS_neighborhood](https://user-images.githubusercontent.com/60548614/160277728-52f94d61-5ab6-4b07-85c7-3adc3fe15baf.png)|![HSMM_10_RefSeqTES_neighborhood](https://user-images.githubusercontent.com/60548614/160277744-c76ac96c-1e75-4512-9ae9-f4130e85eaa1.png)|
| ------------- | ------------- |

|![transitions_10](https://user-images.githubusercontent.com/60548614/160277843-af90a78c-f313-466b-bfff-f6e2dd4467d8.png)|![emissions_10](https://user-images.githubusercontent.com/60548614/160277850-82ae74f2-5401-4e8e-84dc-b87ac2060942.png)|![HSMM_10_overlap](https://user-images.githubusercontent.com/60548614/160277856-9ab0596d-48fa-47b6-b137-be88ce39ab02.png)|
| ------------- | ------------- | ------------- |

P.S. Все файлы выдачи находятся в папке, прикрепленной к репозиторию. Однако ввиду своего размера один загрузить не удалось (HSMM_10_dense.bed)

## Эпигенетические типы
**Состояние** | **Особенности** | **Модификации гистонов** | **Эпигенетический тип**
------------ | ------------- | ------------- | ------------- 
1 | Располагается в доменах, ассоциированных с ядерной ламиной| H3k27me3 | Repressed Heterochromatin
2 | Самое частое эпигенетическое состояние для генома данной линии. Большая доля выпадает на домены, ассоциированных с ядерной ламиной| - | Repressed Heterochromatin
3 | Вероятнее всего представляет собой репрессированный гетерохроматин, потому что также совпадает с домеомнами, ассоциированными с ядерной ламиной| H3k9me3 | Repressed Heterochromatin
4 | Большой процент находится в TES, то есть в начале гена | H3k36me3 | Transcriptional Elongation
5 | Чаще всего встречаются в интронах генов | H3k79me2 | Intron
6 | Также большой процент в RefSeqGene, находится в интронах | H3k79me2, H3k4me1, H2k4me2 | Intron
7 | Характерно для энхансеров | H2k4me2, H2k4me2 | Strong enhancer
8 | Хаотично разросано по геному, сложно определить функцию, которую он несет по геномной карте, поэтому я воспользовался литературой | H3k27ac, H2k4me2, H2k4me1 | Enhancer (DOI: 10.1042/EBC20200014)
9 | В области ярко выраженных промоторов, наполняет CpG-островки и TSS | H2k4me3, H2k4me2, H3k9ac | Active Promoter
10 | То же, что и "9" | H2k4me3, H2k4me2 | Active Promoter

## Скриншоты из UCSC GenomeBrowser, подтверждающие предположения о назначенных эпигенетических типах.
1, 2 и 3 состояние
![image](https://user-images.githubusercontent.com/60548614/160284788-b91d789d-928c-4f1f-b529-313cc3acab19.png)

4, 5 и 6 состояние
![image](https://user-images.githubusercontent.com/60548614/160284798-e38970e0-dcb9-4bb6-b53e-5ac10b0d278f.png)

7 состояние
![image](https://user-images.githubusercontent.com/60548614/160284852-0239c4d4-e9d9-42a9-a015-ebdf7fbb5fb1.png)

9 и 10 состояние
![image](https://user-images.githubusercontent.com/60548614/160284907-3dcc2446-1a84-4c62-9a05-93c1c33d94a9.png)

## Бонусное задание
Состояния названы и отображаются на карте
![image](https://user-images.githubusercontent.com/60548614/160285992-77e83e7d-586f-46d4-8cab-0e3719ec280c.png)
