---
## Front matter
title: "Отчёт по индивидуальному проекту"
subtitle: "Этап 6"
author: "Митичкина Екатерина Павловна"

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

# Задание

1. Сделать поддержку английского и русского языков.
2. Разместить элементы сайта на обоих языках.
3. Разместить контент на обоих языках.
4. Сделать пост по прошедшей неделе.
5. Добавить пост на тему по выбору (на двух языках).


# Выполнение лабораторной работы

1. Для начала я добавила русский язык в ~/work/blog/config/_default/languages.yaml

![Рис 1. добавления языка](img%20/1.png)

2. Длальше я сделала две папки в ~/work/blog/content 

![Рис 2. две папки](img%20/2.png)

3. Перевела всю информацию в ~/work/blog/content/ru/authors/admin/_index.md

![Рис 3. информация обо мне](img%20/3.png)

4. Перевела всю информацию в ~/work/blog/content/ru/home

![Рис 4. опыт ](img%20/4.png)

![Рис 5. достижения ](img%20/5.png)

5. Я перевела все посты на русский язык 

![Рис 6. посты ](img%20/6.png)

6. Также я добавила два новых поста 

![Рис 7. новые посты ](img%20/7.png)

7. Резульат 

![Рис 8. новые посты ](img%20/8.png)


# Выводы

В результате работы разместила двуязычный сайта на Github.

