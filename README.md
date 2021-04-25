# AFM_mutations
## Part 1
0. На сайте IntOGEN нет данных о том, в каких типа рака мутировал данный ген. 
1. Типы мутаций: 
  -  всех мутаций -- **missense** (= относятся к структурным), меняют нуклеиновые кислоты (НК)
  - 25% -- **synonymous** (=относятся к структурным), не меняют НК
  - 6% -- **truncating** (=deletion), укорачивает белок
  - 2% -- **splice-site**, согласно определению "a genetic alteration in the DNA sequence that occurs at the boundary of an exon and an intron (splice site). This change can disrupt RNA splicing resulting in the loss of exons or the inclusion of introns and an altered protein-coding sequence." То есть здесь может произойти и deletion, и insertion, и change. [ссылка на определение](https://www.cancer.gov/publications/dictionaries/genetics-dictionary/def/splice-site-mutation)
2. Самые частотные типы рака, где встречается AFM: 
  - **Skin cancer** (61.2%)
  - **Soft Tissue cancer** (43.28%)
  - **Melanoma** (41%)
  - **Uterine cancer** (20%)
  - **Biliary Tract cancer** (16.9%)

Остальные типы представлены в pdf-файле. \
Все скриншоты по поиску представлены в файле AFM_muts.pdf
## Part 2
Поиск мутаций осуществлялcя с помощью Python:
File | Gene | Found mutations? (Number)| Why chose
------------ | ------------- | ------------- | ------------- 
SSM_AFM-4.ipynb | PCDH15 | Yes (14725568) | AFM в основном есть в **Skin cancer**, поэтому был выбран геном, у которого данный тип рака + проект **MELA-AU**, он первый в [рейтинге](https://dcc.icgc.org/genes/ENSG00000079557/mutations) для AFM
SSM_AFM.ipynb| KCND2 | No | **Uterine cancer** + Проект **LMS-FR** **UTCA-FR** второй по частотности, поэтому было интересно, находится ли там мутации
SSM_AFM-2.ipynb| SGCZ | Yes (1288) | **Melanoma** + Проект **SKCA-BR** третий по частотности
SSM_AFM-3.ipynb| MGAT4C | Yes (1) | **Soft Tussie cancer** + Проект **UTCA-FR** представлен четвертый по частотности

Было ожидаемо, что мутации нашлись в **1**, **3** и **4** случаях, однако тот факт, что их не оказалось в **LMS-FR** показался странным, но в то же самое время мы не проверяли все геномы из **LMS-FR**, возможно, это могло повлиять. \
Файлы с мутациями лежат на github. Таблица для общих мутаций AFM и SGCZ также лежит там. Для MGAT4C таблицу сделать не получился, т.к. слишком большой объем.
