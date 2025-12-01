---
## Front matter
lang: ru-RU
title: Сетевые технологии
subtitle: Адресация IPv4 и IPv6. Двойной стек (Лабораторная работа №6)
author:
  - Заур Мустафаев
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 11 ноября 2025

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
Изучить распределение адресного пространства и настройку IPv4/IPv6 в GNS3:
- Разбиение сетей на подсети (VLSM, IPv6-subnetting)
- Настройка **FRRouting (FRR)** и **VyOS**
- Анализ трафика: **ARP, ICMP, ICMPv6**

# Разбиение сети IPv4

## IPv4: сеть 172.16.20.0/24 → подсети

| Подсеть | Префикс | Диапазон узлов | Broadcast |
|---|---:|---|---|
| №1 (126 узлов) | /25 | 172.16.20.1 – 172.16.20.126 | 172.16.20.127 |
| №2 (62 узла)  | /26 | 172.16.20.129 – 172.16.20.190 | 172.16.20.191 |
| №3 (62 узла)  | /26 | 172.16.20.193 – 172.16.20.254 | 172.16.20.255 |

## Разбиение IPv4: пример VLSM

Сеть **10.10.1.0/26**

- Требуется подсеть на **14 узлов** → `/28`

| Подсеть | Маска | Диапазон узлов |
|---|---|---|
| 10.10.1.16/28 | 255.255.255.240 | 10.10.1.17 – 10.10.1.30 |

# Разбиение сети IPv6

## IPv6: сеть 2001:db8:c0de::/48

Две подсети:

| Подсеть | Префикс |
|---|---|
| A | 2001:db8:c0de:0::/49 |
| B | 2001:db8:c0de:8000::/49 |

## IPv6: разбивка по IID

| Подсеть | Префикс |
|---|---|
| 2001:db8:c0de:0::/65 |
| 2001:db8:c0de:0:8000::/65 |

# Построение сети в GNS3

## Используемое оборудование

![Топология сети](Screenshot_1.png)

## Пример — PC1

![Конфигурация PC1](Screenshot_2.png)

## Интерфейсы

![FRR config](Screenshot_5.png)

## Проверка соединений IPv4

![Ping](Screenshot_8.png)

## Пример — PC3

![IPv6 PC3](Screenshot_10.png)

## Настройка VyOS

![VyOS config](Screenshot_13.png)

## Проверка соединений IPv6

![Ping IPv6](Screenshot_15.png)

## Анализ трафика

![ARP](Screenshot_17.png)

## Анализ трафика

![ICMP](Screenshot_18.png)

## Анализ трафика

![ICMPv6](Screenshot_19.png)

# Самостоятельное задание

## Итоговое адресное пространство

| Устройство | IPv4 | IPv6 |
|---|---|---|
| PC1 | 10.10.1.100/27 | 2001:db8:1:1::a/64 |
| PC2 | 10.10.1.20/28  | 2001:db8:1:4::a/64 |
| Router eth0 | 10.10.1.97/27 | 2001:db8:1:1::1 |
| Router eth1 | 10.10.1.17/28 | 2001:db8:1:4::1 |

## Конфигурация маршрутизатора VyOS

![VyOS конфигурация](Screenshot_23.png)

## Проверка связности

![IPv4 ping/trace](Screenshot_24.png)

## Проверка связности

![IPv6 ping/trace](Screenshot_25.png)

# Выводы

- Выполнено разбиение IPv4 и IPv6 (VLSM и Subnetting)
- Смоделированы сети в GNS3 с использованием **FRR и VyOS**
- Проверена связность по **IPv4 и IPv6**
- Проанализированы кадры ARP, ICMP, ICMPv6 в Wireshark  


