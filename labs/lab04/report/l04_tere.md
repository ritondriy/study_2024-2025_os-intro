---
## Front matter
title: "Отчёт по лабораторной работе № 4"
subtitle: "Операционные системы"
author: "Терещенкова М.В."

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

Получение навыков правильной работы с репозиториями git.

# Задание

- Выполнить работу для тестового репозитория.

- Преобразовать рабочий репозиторий в репозиторий с git-flow и conventional commits.

# Теоретическое введение

**Общая информация:**

Gitflow Workflow опубликована и популяризована Винсентом Дриссеном.

Gitflow Workflow предполагает выстраивание строгой модели ветвления с учётом выпуска проекта.

Данная модель отлично подходит для организации рабочего процесса на основе релизов.

Работа по модели Gitflow включает создание отдельной ветки для исправлений ошибок в рабочей среде.

Последовательность действий при работе по модели Gitflow:

Из ветки master создаётся ветка develop.

Из ветки develop создаётся ветка release.

Из ветки develop создаются ветки feature.

Когда работа над веткой feature завершена, она сливается с веткой develop.

Когда работа над веткой релиза release завершена, она сливается в ветки develop и master.

Если в master обнаружена проблема, из master создаётся ветка hotfix.

Когда работа над веткой исправления hotfix завершена, она сливается в ветки develop и master.

# Выполнение лабораторной работы

## Установка git-flow 
 
Для установки git-flow в Fedora был использован репозиторий Copr. После успешной установки была проверена работоспособность git-flow.

![Установка git-flow](/media/sf_screens/лаба4/photo1.jpg){#fig:001 width=70%}

![Установка git-flow.2](/media/sf_screens/лаба4/photo2.jpg){#fig:002 width=70%}

## Установка Node.js 
 
Для поддержки инструментов семантического версионирования и стандартизированных коммитов был установлен Node.js вместе с pnpm.

![Установка Node.js](/media/sf_screens/лаба4/photo3.jpg){#fig:003 width=70%}

![Установка Node.js.2](/media/sf_screens/лаба4/photo4.jpg){#fig:004 width=70%}

## Настройка Node.js  

Добавлен каталог с исполняемыми файлами в PATH с помощью команд **pnpm setup**, **source ~/.bashrc**

![Добавление каталога](/media/sf_screens/лаба4/photo5.jpg){#fig:005 width=70%}

После этого были установлены утилиты: **commitizen** — для стандартизированных коммитов;**standard-changelog** — для генерации журнала изменений.  

![Установление утилитов](/media/sf_screens/лаба4/photo6.jpg){#fig:006 width=70%}

## Практическое использование Git  

### Создание и подключение репозитория 
 
На GitHub был создан репозиторий git-extended, после чего выполнена его инициализация и первый коммит.

![Репозиторий на GitHub](/media/sf_screens/лаба4/photo7.jpg){#fig:007 width=70%}

![Репозиторий на GitHub](/media/sf_screens/лаба4/photo8.jpg){#fig:008 width=70%}

### Настройка формата коммитов
  
Был инициализирован package.json с настройками:

![Инициализация package.json](/media/sf_screens/лаба4/photo9.jpg){#fig:009 width=70%}

Добавлена конфигурация для commitizen:

![Добавление конфигурации](/media/sf_screens/лаба4/photo10.jpg){#fig:010 width=70%}

После этого были добавлены файлы и выполнен коммит через git cz:

![Добавление файлов и выполнение коммита](/media/sf_screens/лаба4/photo11.jpg){#fig:011 width=70%}

## Конфигурация git-flown

Выполняю инициализацию.Установливаю префикс для версий v. Проверяю, что активная ветка — develop и загружаю весь репозиторий.

![Добавление файлов и выполнение коммита](/media/sf_screens/лаба4/photo12.jpg){#fig:012 width=70%}

## Создание релиза 
 
Создаю релиз 1.0.0;

![Создание релиза 1.0.0](/media/sf_screens/лаба4/photo14.jpg){#fig:014 width=70%}

![Создание релиза 1.0.0](/media/sf_screens/лаба4/photo15.jpg){#fig:015 width=70%}

Создаю релиз на GitHub с помощью команды: **gh release create v1.0.0 -F CHANGELOG.md**

![Создание релиза на GitHub](/media/sf_screens/лаба4/photo16.jpg){#fig:016 width=70%}

## Работа с репозиторием  

### Разработка новой функциональности 
 
Создана ветка новой функциональности с помощью команды: **git flow feature start feature_branch**. После внесения изменений выполнено объединение с develop **git flow feature finish feature_branch**. Создаю новый релиз 1.2.3: **git flow release start 1.2.3**. Обновляю package.json, затем выполняю генерацию журнала изменений и коммит Завершаю релиз и отправляю на GitHub.

![Работа с репозиторием](/media/sf_screens/лаба4/photo17.jpg){#fig:017 width=70%}

# Выводы

Получила навыки правильной работы с репозиториями git.

# Список литературы{.unnumbered}

::: {#refs}
:::
