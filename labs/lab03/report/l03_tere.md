---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Операционные системы"
author: "Терещенкова М.В"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Научиться оформлять отчёты с помощью легковесного языка разметки Markdown.

# Задание

1. Сделайте отчёт по предыдущей лабораторной работе в формате Markdown.
2. В качестве отчёта предоставить отчёты в 3 форматах: pdf, docx и md (в архиве,
поскольку он должен содержать скриншоты, Makefile и т.д.)

# Выполнение лабораторной работы

Перехожу в каталог, в котором находится шаблон для отчета, с помощью утилиты cd и проверяю содержимое с помощью утилиты ls 

![Перемещение между директориями](/media/sf_screens/лаба3/photo1.jpg){#fig:001 width=70%}

Создаю копию шаблона с помощью утилиты cp и опять проверяю его наличие с помощью утилиты ls.

![Создание копии](/media/sf_screens/лаба3/photo2.jpg){#fig:002 width=70%}

Открываю созданный файл с помощью текстового редактора Mousepad.

![Созданный файл в текстовом редакторе Mousepad](/media/sf_screens/лаба3/photo3.jpg){#fig:003 width=70%}

После изменения шаблона я выполнила его компиляцию с помощью команды make из формата md в PDF и Docx. После компилирования проверила содержимое в каталоге и удалила пустые report.pdf и report.docx

![Компилирование отчета](/media/sf_screens/лаба3/photo4.jpg){#fig:004 width=70%}

Далее отправила созданные и скомпилированные файлы на глобальный репозиторий.

![Отправка файлов на Git](/media/sf_screens/лаба3/photo5.jpg){#fig:005 width=70%}

Выполняю последнее действие в отправке с помощью команды git push

![Отправка файлов на Git](/media/sf_screens/лаба3/photo6.jpg){#fig:006 width=70%}

# Выводы

Научилась оформлять отчёты с помощью легковесного языка разметки Markdown.

# Список литературы{.unnumbered}

::: {#refs}
:::
