---
## Front matter
title: "Индивидуальный проект"
subtitle: "Шестой этап"
author: "Галиева Аделина Руслановна"

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


Размещение двуязычного сайта на Github.


# Выполнение лабораторной работы


1. Делаем записи для персональных проектов. (рис. @fig:001) (рис. @fig:002) 


![VR-картинг](image/1.png){#fig:001 width=70%}

![Картинг на дому](image/2.png){#fig:002 width=70%}


2. Добавить пост на тему языки научного программирования. (рис. @fig:003) 


![Пост на тему языки научного программирования](image/3.png){#fig:003 width=70%}


3. Пишем пост по прошедшей неделе.(рис. @fig:004) 


![Пост по прошедшей недели](image/4.png){#fig:004 width=70%}

# Выводы

Я разместила двуязычный сайт на Github.

# Список литературы{.unnumbered}

::: {#refs}
:::
