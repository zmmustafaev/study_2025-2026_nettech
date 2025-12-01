---
## Front matter
title: "Отчёт по лабораторной работе 4"
subtitle: "Подготовка экспериментального стенда GNS3"
author: "Заур Мустафаев"

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
papersize: a
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

Установка и настройка GNS3 и сопутствующего программного обеспечения.

# Выполнение работы

## Запуск GNS3 VM и подключение клиента GNS3

1. Виртуальная машина **GNS3 VM** была запущена в среде **VMware**.  
   После загрузки отображается информация о версии сервера, IP-адресе, параметрах виртуализации и доступных сервисах.  
   Из данных можно отметить:
   - **GNS3 server version:** 3.0.5  
   - **Ubuntu version:** noble  
   - **Qemu version:** 8.2.2  
   - **Virtualization:** vmware  
   - **IP-адрес сервера:** `192.168.133.130`  
   - **Порт:** `80`  
   - **SSH-доступ:** `ssh gns3@192.168.133.130`  
   - **Пароль:** `gns3`

   ![Информация о запущенном сервере GNS3](Screenshot_1.png){ #fig:001 width=80% }

2. В приложении **GNS3** при первом запуске был запущен мастер настройки (**Setup Wizard**).  
   Для подключения к удалённому контроллеру указаны следующие параметры:
   - **Protocol:** HTTP  
   - **Host:** `192.168.133.130`  
   - **Port:** `80 TCP`  
   - **Username:** `admin`  
   - **Password:** `gns3`  

   После ввода данных и нажатия **Next** выполняется проверка соединения с сервером.

   ![Настройка подключения к GNS3 VM](Screenshot_2.png){ #fig:002 width=70% }

## Добавление образа маршрутизатора FRR

1. Для установки нового сетевого устройства был выбран пункт **New template** и категория **Routers**.  
   В списке доступных образов выбрано устройство **FRR (FRRouting)**.  

   ![Выбор маршрутизатора FRR](Screenshot_3.png){ #fig:003 width=80% }

2. Далее система предложила выбрать версию образа для установки.  
   Для версии **FRR 8.2.2** отображается статус **Ready to install**, что указывает на доступность всех необходимых файлов.  

   ![Выбор версии FRR для установки](Screenshot_4.png){ #fig:004 width=80% }

3. После завершения установки появилось окно с инструкцией по использованию образа.  
   Указано, что шаблон будет находиться в категории **Routers**, а данные для входа:
   - **Пользователь:** `root`  
   - **Пароль:** `root`  

   ![Информация об установленном образе FRR](Screenshot_5.png){ #fig:005 width=70% }

4. Для проверки работы образа был запущен экземпляр маршрутизатора **FRR**.  
   После запуска через **PuTTY** отобразился процесс инициализации системы и приглашение командной строки FRRouting.

   ![Запуск маршрутизатора FRR](Screenshot_6.png){ #fig:006 width=80% }

## Добавление образа маршрутизатора VyOS

1. Аналогично, через меню **New template** выбран образ маршрутизатора **VyOS**.  
   Для установки использована версия **VyOS 1.3.3 (qemu)**, статус — **Ready to install**.  
   Основной образ `vyos-1.3.3-amd64.qcow2` был найден локально.  

   ![Выбор и установка образа VyOS](Screenshot_7.png){ #fig:007 width=80% }

2. После завершения установки запущен экземпляр **VyOS**.  
   В консоли видно процесс загрузки системы на основе Debian и приглашение для входа в систему (`vyos login:`), что подтверждает корректную работу образа.  

   ![Запуск маршрутизатора VyOS](Screenshot_8.png){ #fig:008 width=80% }

# Вывод

В ходе выполнения лабораторной работы была выполнена настройка среды **GNS3** с использованием виртуальной машины **GNS3 VM** в **VMware**.  
Удалённое подключение к серверу GNS3 выполнено по протоколу **HTTP** на порт **80**.  
В систему успешно добавлены образы маршрутизаторов **FRRouting (FRR)** и **VyOS**, проверена их загрузка и работоспособность через консольный доступ.  
