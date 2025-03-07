---
## Front matter
title: "Отчет по лабораторной работе №1"
subtitle: "Операционные системы"
author: "Терещенкова M.В"

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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

1. Создание виртуальной машины
2. Установка операционной системы
3. Работа с операционной системой после установки
4. Установка програмного обеспечения для создания документации

# Выполнение лабораторной работы

##Установка и создание виртуальной машины 

Устанавливаю VirtualBox c сайта, написанного в ТУИС

![Сайт для установки VirtualBox](/media/sf_screens/лаба1/photo1.jpg){#fig:001 width=70%}

Скачиваю Fedora Sway c сайта, написанного в ТУИС

![Сайт для Скачивания Fedora Sway](/media/sf_screens/лаба1/photo2.jpg){#fig:002 width=70%}

Нажимаю "Создать", создаю новую виртуальную машину, указываю её имя, путь к папке машины оставляю по умолчанию,выбираю тип ОС и версию.

![Создание виртуальной машины](/media/sf_screens/лаба1/photo3.jpg){#fig:003 width=70%}

Указываю объём основной памяти виртуальной машины размером 4096МБ

![Указывание объёма памяти](/media/sf_screens/лаба1/photo4.jpg){#fig:004 width=70%}

Создаю новый виртуальный жёсткий диск. Задаю размер диска - 80ГБ. 

## Установка операционной системы

Запускаю и получаю такой интерфейс.

![Интерфейс начальной конфигурации](/media/sf_screens/лаба1/photo5.jpg){#fig:005 width=70%}

Нажимаю **Win+Enter** для запуска терминала. В терминале запускаю liveinst.

![liveinst](/media/sf_screens/лаба1/photo6.jpg){#fig:006 width=70%}

Чтобы перейти к раскладке окон с табами, нажимаю Win+w. ВЫбираю язык для использования в процессе установки русский. 

![Выбор языка интерфейса](/media/sf_screens/лаба1/photo7.jpg){#fig:007 width=70%}


Сохраняю место установки по умолчанию. Задаю имя компьютера в соответсвии с соглашение об именовании **tereshchenkovamargo.net**. Создаю аккаунт админстратора и пароль для супер-пользователя.

![Создание аккаунта администратора](/media/sf_screens/лаба1/photo8.jpg){#fig:008 width=70%}

Создаю пользователя, добавляю административные привилегии для этой учетной записи, чтобы я могла свободно выполнять команды как супер-пользователь. Далее операционная система устанавливается. После установки нажимаю “завершить установку”.

![Завершение установки операционной системы](/media/sf_screens/лаба1/photo10.jpg){#fig:010 width=70%}

Диск не отключался автоматически, поэтому отключаю носитель информации с образом.

![Оптический диск отключен](/media/sf_screens/лаба1/photo11.jpg){#fig:011 width=70%}

##  Работа с операционной системой после установки

Запускаю виртуальную машину. Вхожу в ОС под заданной мной при установке учетной записью

![Вход в OC](/media/sf_screens/лаба1/photo12.jpg){#fig:012 width=70%}

Запускаю терминал и переключаюсь на роль суперпользователя. Обновляю все пакеты.

![Обновления](/media/sf_screens/лаба1/photo13.jpg){#fig:013 width=70%}

![Обновления.2](/media/sf_screens/лаба1/photo14.jpg){#fig:014 width=70%}

Устанавливаю программы для удобства работы в консоли: tmux для открытиянескольких “вкладок” в одном терминале, mc в качестве файлового менеджера втерминале 

![Установка tmux и mc](/media/sf_screens/лаба1/photo15.jpg){#fig:015 width=70%}

Устанавливаю программы для автоматического обновления.

![Установка програмного обеспечения для автоматического обновления](/media/sf_screens/лаба1/photo16.jpg){#fig:016 width=70%}

Запускаю таймер.

![Запуск таймера](/media/sf_screens/лаба1/photo17.jpg){#fig:017 width=70%}

Перемещаюсь в диркторию /etc/selinux, открываю mc, ищу нужный файл **config**.

![Поиск файла](/media/sf_screens/лаба1/photo18.jpg){#fig:018 width=70%}

Изменяю открытый файл: SELINUX=enforcing меняю на значение SELINUX=permissive

![Изменение файла](/media/sf_screens/лаба1/photo19.jpg){#fig:019 width=70%}

Перезагружаю виртуальную машину. Запускаю терминал, переключаюсь на супер-пользователя, устанавливаю пакет dkms.

![Установка пакета dkms](/media/sf_screens/лаба1/photo20.jpg){#fig:020 width=70%}

Подключаю образ дополнительной гостевой ОС 

![Подключение образа дополнительной гостевой ОС](/media/sf_screens/лаба1/photo21.jpg){#fig:021 width=70%}

Примонтирую диск с помощью утилиты **mount**; устанавливаю драйвера.

![Примонтирование диска и установка драйвера](/media/sf_screens/лаба1/photo22.jpg){#fig:022 width=70%}

Перезагружаю виртуальную машину.

![Перезагрузка виртуальной машины](/media/sf_screens/лаба1/photo23.jpg){#fig:023 width=70%}

## Установка программного обеспечения для создания документации.

Устанавливаю pandoc и pandoc-crossref вручную. Скачиваю подходящие друг для друга версии pandoc и pandoc-crossref c github. Распаковала архивы и поместила их в **каталог /usr/local/bin**. 

![Успешная установка pandoc и pandoc-crossref](/media/sf_screens/лаба1/photo25.jpg){#fig:025 width=70%}

Устанавливаю дистрибутив texlive.

![Установка texlive](/media/sf_screens/лаба1/photo26.jpg){#fig:026 width=70%}

# Выводы

Приобрела практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Список литературы{.unnumbered}

::: {#refs}
:::
