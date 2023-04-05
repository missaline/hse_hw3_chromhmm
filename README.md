# hse_hw3_chromhmm

[Colab](https://colab.research.google.com/drive/14lLGyJpovSOoYkFBMV3M3Pd_ijoLotTA?usp=sharing)

## Гистоновые Метки
Name | File
--- | ---
H3K9me3 | wgEncodeBroadHistoneHepg2H3k09me3AlnRep1.bam
H3K79me2 | wgEncodeBroadHistoneHepg2H3k79me2StdAlnRep1.bam
H3K4me2 | wgEncodeBroadHistoneHepg2H3k4me2StdAlnRep1.bam
H3K4me3 | wgEncodeBroadHistoneHepg2H3k4me3StdAlnRep1.bam
H3K9ac | wgEncodeBroadHistoneHepg2H3k9acStdAlnRep1.bam
H3K4me1 | wgEncodeBroadHistoneHepg2H3k04me1StdAlnRep1.bam
H3K27ac | wgEncodeBroadHistoneHepg2H3k27acStdAlnRep1.bam
H3k36me3 | wgEncodeBroadHistoneHepg2H3k36me3StdAlnRep1.bam
H4k20me1 | wgEncodeBroadHistoneHepg2H4k20me1StdAlnRep1.bam
H3K27me3 | wgEncodeBroadHistoneHepg2H3k27me3StdAlnRep1.bam


## cellmarkfiletable.txt
Клеточная линия | Гистоновая метка | Файл с гистоновой меткой | Файл с контролем
--- | --- | --- | ---
HepG2 |	H3K4me1 | 3k04me1StdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2 |	H3K9me3	| 3k09me3AlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| H3K79me2 | 3k79me2StdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| H3K4me2	| 3k4me2StdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| H3K4me3	| 3k4me3StdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| H3K9ac | 3k9acStdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| 3K27ac | 3k27acStdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| 3K36me3 | 3k36me3StdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| 4K20me1	| 4k20me1StdAlnRep1.bam | ControlStdAlnRep1.bam
HepG2	| 3K27me3	| 3k27me3StdAlnRep1.bam | ControlStdAlnRep1.bam


## ChromHMM
Emission | Overlap | Transition 
 --- | --- | ---
![Image](https://user-images.githubusercontent.com/104971016/230200728-7b990d57-fa2e-4757-bf52-9eda84f84919.png) | ![Image](https://user-images.githubusercontent.com/104971016/230200630-f271d923-17a6-4029-b65c-765ad709bf0f.png) | ![Image](https://user-images.githubusercontent.com/104971016/230200072-71382035-4afa-4289-8ed5-71c6852d89eb.png)

RefSeqTSS | RefSeqTES 
 --- | --- 
![Image](https://user-images.githubusercontent.com/104971016/230200369-11488045-351a-41c6-bc20-d81dbc8777f1.png) | ![Image](https://user-images.githubusercontent.com/104971016/230200504-c93cf944-721a-4e43-942b-69fd509a8270.png)

## Эпигенетические типы
| Состояние | Эпигенетический тип |Встречаемость в гистоновых модификациях| Описание | Изображение из USCC |
|-----------|----------|------|----------|---------------------|
|     1     |  Promoter  |  Во всех, но чаще всего: <ul><li> H3K4me1 <li> H3K4me2 <li> H3K4me3 <li> H3K9ac <li> H3K27ac <li> H3K79me2  |  Данное состояние попадает на экзон <li> Показывает высокий сигнал <li> Чаще всего ассоциировано с <ul><li> RefSeqExon <li> RefSeqGene <li> RefSeqTES <li> RefSeqTSS2kb </li> </li>  В меньшей степени с: <li> CpGIslands |        ![Image](https://user-images.githubusercontent.com/104971016/230207409-f1cf8e8e-09b4-491a-b44b-028926be89ff.png)              |
|     2     |  Enhancer |   Почти не встречается, кроме: <li> H3K9ac  <li> H3K27ac |  <li> Данное состояние частично попадает на экзон и интрон <li> Чаще всего ассоциировано с <ul><li> CpGIslands <li> RefSeqExon <li> RefSeqTES <li> RefSeqTSS <li> RefSeqTSS2kb   |   ![Image](https://user-images.githubusercontent.com/104971016/230207533-07a2b118-fe89-49df-9da5-d704918ffa75.png)        |
|     3     |  Repressed |   Встречается почти во всех, но чаще всего:  <li> H3K4me1  |  <li> Данное состояние нe попало на ген или попала на интрон и экзон <li> Показывает низкий сигнал <li> Чаще всего ассоциировано с  <ul><li> RefSeqTES <li> LaminB1lads   |        ![Image](https://user-images.githubusercontent.com/104971016/230207852-52f4b61e-4369-49e4-baae-4d65cbc9cf2e.png)              |
|     4     |  Heterochromatin  |   Во всех, но чаще: <li> H3K4me1 <li> H3K79me2 <li> H4K20me1  | <li> Данное состояние попадает на интрон гена <li> Показывает низкий сигнал <li> Чаще всего ассоциировано с <ul><li> RefSeqExon <li> RefSeqGene <li> RefSeqTSS |        ![Image](https://user-images.githubusercontent.com/104971016/230208463-e892945d-58b5-4ae2-9fe4-f6d969505ec1.png)              |
|     5     |  Transcribed |  Встречается во всех   |  <li> Попадает в интрон гена <li> Очень слабый сигнал <li> Чаще всего ассоциировано с <ul><li> RefSeqExon <li> RefSeqGene <li> RefSeqTSS  |        ![Image](https://user-images.githubusercontent.com/104971016/230208854-be3e7b41-63c3-4ac0-92eb-3b54899427c5.png)            |
