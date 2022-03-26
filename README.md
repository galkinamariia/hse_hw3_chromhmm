# hse_hw3_chromhmm

# Домашнее задание №3

> ### Введение:
>
>Целью данного домашнего задания является разбивка (аннотация) генома человека на разные типы эпигенетических состояний. Это будет сделано на основании данных о наличии различных гистоновых модификаций (гистоновый код) в соответствующих участках генома. Для выполнения этого задания мы будем работать с чтениями, полученными в ChIP-seq экспериментах из проекта ENCODE (https://www.encodeproject.org/), которые были выровнены на геном человека (версия hg19) – т.е. у нас будут уже готовые bam-файлы. Автоматическая разбивка генома на эпигенетические типы будет осуществляться с помощью программы ChromHMM. В результате итеративной процедуры (алгоритм Баума-Велша) программа определит сочетание гистоновых меток, которые характерны для каждого из N разных эпигенетических типов (число N указывается пользователем при запуске программы). Наша задача будет заключаться в том, чтобы на основании косвенных независимых наблюдений вручную приписать каждому из N эпигенетических типов возможную биологическую функцию.

> ### Ссылка на мой google colab ноутбук: 

## Часть №1:

В домашнем задании №2 рассматривалась клеточная линия PC-9. Так как она не содержит ChIP-seq эксперименты в рассматриваемых гистоновых метках для ДЗ№3, то была взята другая клеточная линия - GM12878. Гистоновая метка из ДЗ№2 - H3k4me3.
![image](https://user-images.githubusercontent.com/59726719/160252289-dc8f14b0-73a2-4411-8f83-4e502da2c20f.png)

### Список гистоновых меток и ссылки на bam-файлы
| № | Гистоновая метка | Ссылка на bam-файл |
|:-:|:----------------:|:------------------:|
| 1 |H3k4me3|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k4me3StdAlnRep1.bam|
| 2 |Ctcf|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878CtcfStdAlnRep1.bam|
| 3 |Ezh239875|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878Ezh239875AlnRep1.bam|
| 4 |H2az|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H2azStdAlnRep1.bam|
| 5 |H4k20me1|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H4k20me1StdAlnRep1.bam|
| 6 |H3k79me2|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k79me2StdAlnRep1.bam|
| 7 |H3k9ac|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k9acStdAlnRep1.bam|
| 8 |H3k9me3|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k9me3StdAlnRep1.bam|
| 9 |H3k27ac|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k27acStdAlnRep1.bam|
| 10 |H3k27me3|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k27me3StdAlnRep1.bam|

### Файл с контрольным экспериментом для соответствующего типа клеток 

http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878ControlStdAlnRep1.bam

![image](https://user-images.githubusercontent.com/59726719/160252726-46ddbcfa-521e-4703-a22f-330b6d4fe581.png)


### Текстовый файл cellmarkfiletable.txt - [cellmarkfiletable.txt]()

### ChromHMM

### Эпигетические типы

## Часть №2:
