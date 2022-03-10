# Домашнее задание №2 
### Анализ ChIP-Seq
### Майнор биоинформатика

#### Графики и результаты выдачи FastQC в папке files
#### [Ссылка](https://colab.research.google.com/drive/10yiTXD_kCj7P0BEzCJt2P9eQIPPrtyLX?usp=sharing) на колаб с основной частью
#### [Ссылка](https://colab.research.google.com/drive/1UaofFq8Pje0yJ6u8wfi4Prd-XjX29t2j?usp=sharing) на бонусное задание в колабе

### Анализ результатов FastQC
#### Как можно заметить из выдачи - образец ENCFF983KWQ хорошего качества
 ![](https://github.com/dannygrig/hse_hw2_chip/blob/main/files/FF983KWQ_fastqc.png)
 ![](https://github.com/dannygrig/hse_hw2_chip/blob/main/files/FF983KWQ_fastqc_2.png)
##### У образца ENCFF834DXB есть значимые проблемы с качеством некоторых чтений
 ![](https://github.com/dannygrig/hse_hw2_chip/blob/main/files/FF834DXB_fastqc.png)
 ![](https://github.com/dannygrig/hse_hw2_chip/blob/main/files/FF834DXB_fastqc_2.png)
##### У контроля ENCFF902MPL тоже есть небольшие проблемы с качеством некоторых последовательностей
 ![](https://github.com/dannygrig/hse_hw2_chip/blob/main/files/FF902MPL_fastqc.png)
 ![](https://github.com/dannygrig/hse_hw2_chip/blob/main/files/FF902MPL_fastqc_2.png)
##### Было принято решение подрезать чтения у ENCFF834DXB и у контроля (код в Colab'е)
##### С помощью trimmomatic чтения были подрезаны, однако, качество улучшилось далеко не так заметно (подробнее в files - результаты FastQC для подрезанных образцов)


| Fastq файл | Общее кол-во ридов | Риды уникальные | Риды неуникальные | Риды не выравнились |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| ENCFF834DXB | 17283292 | 417150 (2.41%) | 1473006 (8.52%) | 15393136 (89.06%) |
| ENCFF983KWQ | 40166682 | 1085078 (2.70%) | 3659375 (9.11%) | 35422229 (88.19%) |
| ENCFF902MPL | 37572200 | 1187983 (3.16%) | 4812098 (12.81%) | 31572119 (84.03%) |

##### Полученный график для bam - файла ENCFF441TOI 
 ![](https://github.com/dannygrig/hse_hw2_chip/blob/main/files/result.png)
