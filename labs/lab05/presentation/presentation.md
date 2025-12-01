---
## Front matter
lang: ru-RU
title: Сетевые технологии
subtitle: Простые сети в GNS3. Анализ трафика (Лабораторная работа №5)
author:
  - Заур Мустафаев
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 29 октября 2025

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

# Цель лабораторной работы

## Цель
Построить простейшие модели сети в **GNS3**, используя:
- Коммутатор **Ethernet**
- Маршрутизаторы **FRRouting (FRR)** и **VyOS**
- Средства анализа **Wireshark**

# Выполнение лабораторной работы

## Создание топологии в GNS3

![Топология сети](01.png){ width=65% }

## Проверка связи между узлами

![Ping между узлами](03.png){ width=65% }

## Анализ ARP-трафика

![ARP-пакеты](04.png){ width=70% }

## Анализ ICMP, UDP и TCP

![ICMP и TCP анализ](07.png){ width=75% }

## Настройка FRR

![Настройка FRR](11.png){ width=70% }

## Анализ ICMP FRR

![ICMP FRR](13.png){ width=75% }

## Настройка VyOS

![Настройка VyOS](15.png){ width=75% }

## Анализ ICMP и ARP

![Анализ трафика VyOS](17.png){ width=75% }


# Выводы по работе

## Итоги

- Смоделированы сети на базе маршрутизаторов **FRR** и **VyOS**  
- Настроены IP-сети и подтверждена их работоспособность  
- Проведён анализ трафика с помощью **Wireshark**  
- Проверена корректность протоколов **ARP**, **ICMP**, **UDP** и **TCP**  
- Работа выполнена успешно

