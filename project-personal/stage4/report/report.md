---
## Front matter
title: "Отчёт по индивидуальному проекту"
subtitle: "Этап 4"
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
Добавить к сайту ссылки на научные и библиометрические ресурсы.

# Задача
1. Зарегистрироваться на соответствующих ресурсах и разместить на них ссылки на сайте:
    - eLibrary : https://elibrary.ru/;
    - Google Scholar : https://scholar.google.com/;
    - ORCID : https://orcid.org/;
    - Mendeley : https://www.mendeley.com/;
    - ResearchGate : https://www.researchgate.net/;
    - Academia.edu : https://www.academia.edu/;
    - arXiv : https://arxiv.org/;
    - github : https://github.com/.
2. Сделать пост по прошедшей неделе.
3. Добавить пост на тему по выбору:
    - Оформление отчёта.
    - Создание презентаций.
    - Работа с библиографией.



# Выполнение индивидуального проекта
1.	Для начала надо было зарегистрироваься на всех представленых сайтах 
![eLibrary](img%20/1.png)
![Google Scholar](img%20/2.png)
![ORCID](img%20/3.png)
![Mendeley](img%20/4.png)
![ResearchGate](img%20/5.png)
![Academia.edu](img%20/6.png)
![arXiv](img%20/7.png)
![github](img%20/16.png)  
2. Далее я начала редактировать файл, который находится в ~/work/blog/content/authors/admin/index.md. И добавила туда ссылки и поменяла иконки 
![добавление ссылок](img%20/15.png)
3. Перешла в ~/work/blog/content/post/Lastweek3. Добавила фото и написала пост в файл index.md о  прошедшей неделе
![добавление фото](img%20/11.png)
![код поста](img%20/12.png)
4. Перешла в ~/work/blog/content/post/Report. Добавила фото и написала пост в файл index.md по теме Оформление отчёта
![добавление фото](img%20/13.png)
![код поста](img%20/14.png)

# Выводы
В результате работы добавила к сайту ссылки на научные и библиометрические ресурсы.