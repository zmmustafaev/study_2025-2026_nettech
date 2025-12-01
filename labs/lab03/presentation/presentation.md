---
## Front matter
lang: ru-RU
title: Сетевые технологии
subtitle: Анализ трафика в Wireshark (Лабораторная работа №3)
author:
  - Заур Мустафаев
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 3 октября 2025

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

Изучение кадров Ethernet, анализ PDU транспортного и прикладного уровней стека TCP/IP с использованием Wireshark.

# Выполнение лабораторной работы

## Получение информации о сетевых интерфейсах

![Вывод команды ipconfig](01.png){ #fig:001 width=70% }

## Определение MAC-адресов

- MAC-адрес состоит из 48 бит (6 байт).  
- Первые 3 байта — OUI производителя.  
- Последние 3 байта — уникальный идентификатор интерфейса.

## Анализ кадров канального уровня

![Ping шлюза](02.png){ #fig:002 width=70% }

## Фильтрация ARP и ICMP пакетов

![Фильтрация пакетов](05.png){ #fig:005 width=70% }

## ICMP Echo Request

![ICMP-запрос](06.png){ #fig:006 width=70% }

## ARP-запрос

![ARP-запрос](04.png){ #fig:004 width=70% }

## Анализ протоколов транспортного уровня

### HTTP (TCP)

![HTTP-трафик](07.png){ #fig:007 width=70% }

### DNS (UDP)

![DNS-трафик](09.png){ #fig:009 width=70% }

### QUIC (UDP)

![QUIC-трафик](10.png){ #fig:010 width=70% }

## Анализ TCP Handshake

![TCP пакеты](11.png){ #fig:011 width=70% }

## Визуализация TCP Handshake

![График TCP потока](12.png){ #fig:012 width=70% }

# Выводы по работе

## Вывод

В ходе работы с помощью Wireshark были проанализированы пакеты Ethernet, ICMP, ARP, HTTP, DNS и QUIC. Подробно изучен процесс установления TCP-соединения (трёхстороннее рукопожатие). Получены практические навыки фильтрации и анализа сетевого трафика.
