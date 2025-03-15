---
## Front matter
lang: ru-RU
title: Лабораторная работа №5
subtitle: Операционные системы
author:
  - Терещенкова М. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 15 марта 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---


## Цель работы

Познакомиться с pass, gopass, native messaging, chezmoi. Научиься пользоваться этими утилитами, синхранизировать их c git.

## Задание

- Установить дополнительное ПО

﻿﻿﻿- Установить и настроить pass

﻿﻿﻿- Настроить интерфейс с браузером

﻿﻿﻿- Сохранить пароль

﻿﻿﻿- Установить и настроить chezmoi

﻿﻿﻿- Настроить chezmoi на новой машине

﻿﻿﻿- Выполнить ежедневные операции с chezmoi

## Выполнение лабораторной работы

### Менеджер паролей pass

#### Установка

Устанавливаю pass

![Установка Pass](/media/sf_screens/лаба5/photo1.jpg){#fig:001 width=70%}

## Выполнение лабораторной работы

Устанавливаю gopass

![Установка gopass](/media/sf_screens/лаба5/photo2.jpg){#fig:002 width=70%}

## Выполнение лабораторной работы

### Настройка

Просмотриваю списки ключей gpg.

![Просмотр списка ключей](/media/sf_screens/лаба5/photo3.jpg){#fig:003 width=70%}

## Выполнение лабораторной работы

Вижу, что ключ есть, поэтому инициализирую хранилище.

![Инициализация хранилища](/media/sf_screens/лаба5/photo4.jpg){#fig:004 width=70%}

### Настройка формата коммитов
  
Был инициализирован package.json с настройками:

![Инициализация package.json](/media/sf_screens/лаба4/photo9.jpg){#fig:009 width=70%}

Добавлена конфигурация для commitizen:

![Добавление конфигурации](/media/sf_screens/лаба4/photo10.jpg){#fig:010 width=70%}

После этого были добавлены файлы и выполнен коммит через git cz:

![Добавление файлов и выполнение коммита](/media/sf_screens/лаба4/photo11.jpg){#fig:011 width=70%}

## Выполнение лабораторной работы

### Конфигурация git-flown

Выполняю инициализацию.Установливаю префикс для версий v. Проверяю, что активная ветка — develop и загружаю весь репозиторий.

![Добавление файлов и выполнение коммита](/media/sf_screens/лаба4/photo12.jpg){#fig:012 width=70%}

## Выполнение лабораторной работы

### Создание релиза 
 
Создаю релиз 1.0.0;

![Создание релиза 1.0.0](/media/sf_screens/лаба4/photo14.jpg){#fig:014 width=70%}

## Выполнение лабораторной работы

### Работа с репозиторием  

#### Разработка новой функциональности 
 
Создана ветка новой функциональности с помощью команды: **git flow feature start feature_branch**. После внесения изменений выполнено объединение с develop **git flow feature finish feature_branch**. Создаю новый релиз 1.2.3: **git flow release start 1.2.3**. Обновляю package.json, затем выполняю генерацию журнала изменений и коммит Завершаю релиз и отправляю на GitHub.

![Работа с репозиторием](/media/sf_screens/лаба4/photo17.jpg){#fig:017 width=70%}


## Выводы

Познакомилась с pass, gopass, native messaging, chezmoi. Научилась пользоваться этими утилитами, синхранизировать их c git.


# ЕЕЕЕЕ