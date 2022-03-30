# hse_hw3_chromhmm

## Входные данные
Клеточная линия  NHEK (epidermal keratinocytes)
P.S. в ДЗ-2 у меня была линия PC-3, но её не оказалось в таблице)

## Ссылка на колаб:
https://colab.research.google.com/drive/1KPw0NGql2vOFBDX7_OR9va23uhoOMgR0?usp=sharing
 

## Таблица гистоновых меток
Клеточная линия | Гистоновая метка | Имя файла | Файл с контролем 
| --- | --- | --- | ---
Nhek|H3k27ac|H3k27acStdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k27me3|H3k27me3StdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k36me3|H3k36me3StdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k4me1|H3k4me1StdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k4me2|H3k4me2StdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k79me2|H3k79me2AlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k9me1|H3k9me1StdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k9ac|H3k9acStdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H4k20me1|H4k20me1StdAlnRep1.bam|ControlStdAlnRep1.bam
Nhek|H3k09me3|H3k09me3AlnRep1.bam|ControlStdAlnRep1.bam

## Png из выдачи ChromHMM
|![emissions_10](https://user-images.githubusercontent.com/93254228/160722721-c2c6cae7-96bb-4c68-a382-a6e31965e34d.png)| ![Nhek_10_overlap](https://user-images.githubusercontent.com/93254228/160722737-3d452038-7195-4c53-b19e-9e5a643d52fa.png) | ![Nhek_10_RefSeqTES_neighborhood](https://user-images.githubusercontent.com/93254228/160722748-592a6397-0094-4259-b651-0ef21443d987.png) | ![Nhek_10_RefSeqTSS_neighborhood](https://user-images.githubusercontent.com/93254228/160722761-8f3fc575-2bfe-46e7-b888-d12dbd90b1f8.png) | ![transitions_10](https://user-images.githubusercontent.com/93254228/160722774-bc5f80cb-fc24-4568-be66-53752cbcdc00.png)|
| ------------- | ------------- | ------------- | ------------- | ------------- |

## Анализ UCSC GenomeBrowser

| 9, 10| ![image](https://user-images.githubusercontent.com/93254228/160727167-189b8ac2-729a-48fd-8688-d66e40963771.png)|
|---|---|
| 7, 8| ![image](https://user-images.githubusercontent.com/93254228/160727384-02d35e90-8d27-414f-ac63-5326e9c7960c.png)|
| 6| ![image](https://user-images.githubusercontent.com/93254228/160727347-e7dfc3f8-8807-48b5-ae7f-ae420434e74b.png)|
| 5 | ![image](https://user-images.githubusercontent.com/93254228/160727323-3bdc62f3-84d2-4842-8f3b-67931b192800.png)|
| 4 | ![image](https://user-images.githubusercontent.com/93254228/160727496-15097ee5-351c-4ed8-922d-eb4472c8ba0b.png)|
| 1, 2, 3| ![image](https://user-images.githubusercontent.com/93254228/160727283-893630b6-4613-4cbd-82c9-f7975de50fe1.png)|

## Эпигенетические типы
**Состояние** | **Особенности** | **Модификации гистонов** | **Эпигенетический тип**
------------ | ------------- | ------------- | ------------- 
1 | Располагается в разных частях генов, иногда в конце гена (TES)| H3k36me3 | Open chromatin
2 | Встречается как в интронах, так и экзонах генов | H2k79me2 | Open chromatin
3 | Располагается в разных частях генов, иногда в начале гена (TSS)| H2k79me2, H3k4me1 | Open chromatin
4 | Замечен в областях доменов, ассоциированных с ядерной ламиной, но чаще всего детектируется в интронах | H3k4me1 | Intron
5 | Ассоциирован с зоной энхансера | H3k25ac, H3k4me1 | Enchancer
6 | Достоверный промотор: не только выпадает на эти области, но и содержит CpG-островки | H3k9ac, H3k4me2, H2k27ac |  Active Promoter
7 | Слабый промтор, замечен в начале генов (TSS) | H2k4me2| Weak Promoter
8 | Также располагается в области слабого промотора и иногда в области начала гена | H3k27me3| Weak Promoter
9 | Является репрессированным гетерохроматином, самое популярное состояние для генома | - | Repressed Heterochromatin
10 | Так же, как и "9", совпадает с доменами, ассоциированными с ядерной ламиной | H2k9me3 | Repressed Heterochromatin
