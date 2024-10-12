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