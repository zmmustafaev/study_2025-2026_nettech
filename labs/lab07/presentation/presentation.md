---
lang: ru-RU
title: Сетевые технологии
subtitle: DHCP для IPv4 и IPv6 в GNS3 (Лабораторная работа №7)
author:
  - Заур Мустафаев
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 28 ноября 2025
aspectratio: 169
theme: metropolis
slide_level: 2
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цель лабораторной работы

## Цель
Получить практические навыки настройки DHCP для:
- IPv4  
- IPv6 (Stateless и Stateful)  

с использованием маршрутизатора **VyOS** и среды моделирования **GNS3**.

# Выполнение работы

## Исходная IPv4-топология

![Топология IPv4](01.png){ width=70% }

## Расширенная IPv6-топология

![Топология IPv6](09.png){ width=75% }

## Начальная конфигурация маршрутизатора

![Настройка VyOS](02.png){ width=75% }

## Настройка IPv4 и DHCP-сервера

![DHCPv4 конфигурация](03.png){ width=75% }

## Получение адреса клиентом PC1

![DHCPv4 клиент](04.png){ width=75% }

## Проверка параметров и связности

![Параметры IPv4](05.png){ width=75% }

## DHCPv4 статистика сервера

![Статистика DHCPv4](06.png){ width=80% }

## Журнал DHCP и трафик в Wireshark

![DHCPv4 log](07.png){ width=80% }

## Журнал DHCP и трафик в Wireshark

![DHCPv4 packets](08.png){ width=80% }

## Настройка RA и DHCPv6 Stateless

![Настройка Stateless](11.png){ width=75% }

## Проверка работы Stateless на PC2

![IPv6 SLAAC и DNS](12.png){ width=75% }

## Получение параметров DHCPv6 (Stateless)

![DHCPv6 Stateless параметры](13.png){ width=75% }

## Статистика DHCPv6 Stateless

![DHCPv6 Stateless вывод](14.png){ width=80% }

## Wireshark DHCPv6 Stateless

![DHCPv6 Stateless Wireshark](15.png){ width=80% }

## Настройка DHCPv6 Stateful

![Настройка Stateful](16.png){ width=85% }

# Работа DHCPv6 Stateful на PC3

## Параметры сети до получения адреса

![До получения адреса](17.png){ width=85% }

## Получение IPv6-адреса (Stateful)

![Адрес от DHCPv6](18.png){ width=85% }

## Параметры сети после получения адреса

![Адрес получен](19.png){ width=85% }

## Параметры сети после получения адреса

![Проверка связности](20.png){ width=85% }

## Аренды DHCPv6 Stateful

![DHCPv6 аренды](21.png){ width=85% }

## Пакеты Solicit / Advertise / Request / Reply

![DHCPv6 Stateful Wireshark](22.png){ width=85% }


# Выводы

## Итоги

- Настроены и протестированы DHCPv4, DHCPv6 Stateless и DHCPv6 Stateful  
- IPv4-клиенты получают полный набор настроек автоматически  
- Для IPv6 успешно реализованы оба режима конфигурации  
- Проанализирован сетевой трафик DHCPv4 и DHCPv6 в Wireshark  
- Подтверждена корректность работы адресации и сетевой инфраструктуры  

Работа выполнена успешно.

