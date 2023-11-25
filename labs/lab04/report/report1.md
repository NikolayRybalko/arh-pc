---
## Front matter
title: "Отчёт по лабораторной работе №4"
subtitle: "Архитектура компьютера"
author: "Рыбалко Николай НБИбд-02-23"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью работы является освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Выполнение лабораторной работы


## Программа Hello world!

Создаем каталог lab04 с помощью команды mkdir, затем переходим в него с помощью команды cd 
и создаем файл hello.asm. Указано на рис. [-@fig:001]

![Создание каталога и файла](image/01.png){ #fig:001 width=70%, height=70% }

Открываем файл и вводим код. Указано на рис. [-@fig:002]

![Код программы hello.asm](image/02.png){ #fig:002 width=70%, height=70% }

## Транслятор NASM

С помощью команды nasm транслируем файл, получаем файл hello.o.

Еще раз транслируем файл с использованием доп. опций команды nasm. 
В результате были созданы файл листинга list.lst, объектный файл obj.o . Указано на рис. [-@fig:003]

![Трансляция программы](image/03.png){ #fig:003 width=70%, height=70% }

## Компоновщик LD

С помощью команды ld выполняем компановку.
Выполняем еще одну компановку для объектного файла obj.o и получаем исполняемый файл с именем main.
Запускаем исполняемые файлы. Указано на рис. [-@fig:004]
 
![Компановка и запуск программы](image/04.png){ #fig:004 width=70%, height=70% }

##  Задание для самостоятельной работы

Меняем Hello world на свое имя и запустим файл еще раз. Указано на рис. [-@fig:005] [-@fig:006]

![Программа в файле lab4.asm](image/05.png){ #fig:005 width=70%, height=70% }

![Сборка и проверка программы lab4.asm](image/06.png){ #fig:006 width=70%, height=70% }

# Выводы

Таким образом я освоил процесс компиляции и сборки программ, написанных на ассемблере nasm.
