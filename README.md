# Практика №1
## Задание 1.1

В текущем состоянии приложение представляет собой простой монолит, отвечающий за взаимодействие с пользователем, управление IoT, хранение данных. Взаимодействие происходит по наиболее примитивному сценарию через прямые синхронные запросы между компонентами.

Основные бизнес функции, которые на данный момент выполняет приложение:
- Управление и конфигурация устройств IoT
  - подключение новых устройств (через администратора)
  - прямое управление устройствами IoT
  - настройка конфигурации устройств
- Считывание и хранение данных с сенсоров
  - запрос у IoT данных с сенсоров

Описание системы в формате С4 диаграммы можно посмотреть в /diagrams/1-1

## Задание 1.2

Для реализации всех бизнес требований, а также увеличения гибкости и масштабирования системы было принято решено
перевести проект на микросервисную архитектуру.

### Исходный монолит

Исходный монолит был разделен на несколько новых сервисов по бизнес-доменам:
 - взаимодействие с устройствами IoT
 - считывание и хранение данных с сенсоров
 - настройка конфигурации устройств
 - управление устройствами IoT

### Новые бизнес-функции

Для реализации возможности добавления пользовательских сценариев добавлен "Script Service"

Также пользователь получил возможность самостоятельно настраивать и подключать устройства

За интеграцию с различными устройствами IoT теперь отвечает набор сервисов-адаптеров,
каждый из которых позволяет управлять устройствами IoT по предоставляемому протоколу.
При необходимости, существует возможность масштабирования набора сервисов-адаптеров или добавления новых для будущих интеграций.

Полную схему систему в формате С4 можно посмотреть в /diagrams/1-2