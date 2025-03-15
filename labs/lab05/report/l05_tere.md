---
## Front matter
title: "Отчёт по лабораторной работе №5"
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

Познакомиться с pass, gopass, native messaging, chezmoi. Научиься пользоваться этими утилитами, синхранизировать их c git.

# Задание

- Установить дополнительное ПО

﻿﻿﻿- Установить и настроить pass

﻿﻿﻿- Настроить интерфейс с браузером

﻿﻿﻿- Сохранить пароль

﻿﻿﻿- Установить и настроить chezmoi

﻿﻿﻿- Настроить chezmoi на новой машине

﻿﻿﻿- Выполнить ежедневные операции с chezmoi

# Выполнение лабораторной работы

## Менеджер паролей pass

### Установка

Устанавливаю pass

![Установка Pass](/media/sf_screens/лаба5/photo1.jpg){#fig:001 width=70%}

Устанавливаю gopass

![Установка gopass](/media/sf_screens/лаба5/photo2.jpg){#fig:002 width=70%}

### Настройка

Просмотриваю списки ключей gpg.

![Просмотр списка ключей](/media/sf_screens/лаба5/photo3.jpg){#fig:003 width=70%}

Вижу, что ключ есть, поэтому инициализирую хранилище.

![Инициализация хранилища](/media/sf_screens/лаба5/photo4.jpg){#fig:004 width=70%}

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

Познакомилась с pass, gopass, native messaging, chezmoi. Научилась пользоваться этими утилитами, синхранизировать их c git.


# Список литературы{.unnumbered}

::: {#refs}
:::


:::

