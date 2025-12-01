---
## Front matter
lang: ru-RU
title: Сетевые технологии
subtitle: Подготовка экспериментального стенда GNS3 (Лабораторная работа №4)
author:
  - Заур Мустафаев
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 17 октября 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цели и задачи работы

## Цель лабораторной работы

Установка и настройка среды **GNS3** и сопутствующего программного обеспечения, а также добавление и проверка работы образов маршрутизаторов **FRRouting** и **VyOS**.

# Выполнение лабораторной работы

## Запуск GNS3 VM в VMware

![Информация о сервере GNS3](Screenshot_1.png){ #fig:001 width=70% }

## Настройка подключения клиента GNS3

![Настройка подключения GNS3](Screenshot_2.png){ #fig:002 width=70% }

## Добавление образа маршрутизатора FRR

![Установка образа FRR](Screenshot_3.png){ #fig:003 width=70% }

## Проверка работы маршрутизатора FRR

![Запуск маршрутизатора FRR](Screenshot_6.png){ #fig:004 width=70% }

## Добавление образа маршрутизатора VyOS

![Выбор образа VyOS](Screenshot_7.png){ #fig:005 width=70% }

## Проверка работы маршрутизатора VyOS

![Запуск VyOS](Screenshot_8.png){ #fig:006 width=70% }

# Выводы по работе

## Итоги

- Успешно установлена и настроена среда **GNS3** с использованием **VMware**.  
- Выполнено подключение клиента GNS3 к серверу.  
- Добавлены и протестированы образы маршрутизаторов:
  - **FRRouting (FRR)**  
  - **VyOS**  
- Проверена корректность загрузки и доступности CLI обоих устройств.
