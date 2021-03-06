Модуль миграций
===============

Модуль для CMS 1С-Битрикс, помагает реализовывать быстрые изменения схемы данных проекта.

### Введение

Как известно исходный код плотно взаимодействует со структурой данных в проекте. С появлением новых функциональных требований исходный код изменяется,
он требует новые поля для хранения даных либо обределяет новые сущности которые отражаются в отдельных таблицах,
а в проектах основанных CMS Bitrix данные в основном отражены в инфоблоках.

Основная структура хранения данных проекта написанного на Битриксе отличается от общепринятой.
Сущности хранятся не в отдельных таблицах, а абстрагированны в виде инфоблоков в разных местах, поэтому стандартные
инструменты работы с данными, в таких проектах, не всегда справляются со своими задачами.

Модуль миграций основан на исходном коде ядра CMS и поэтому позволяет в наиболее удобной форме осуществлять синхронизацию. Идея состоит в том,
что проект имеет специальный катлог для хранения файлов описывающих приобразование данных, этот каталог обновляется вместе с исходым кодом проекта.
При обновлении исходного кода можно обвновить базу данных проекта чтобы она соответствовала новому функционалу.

Модуль имеет два типа синхронизации:

1. Автоматическая - сихронизируются базовые данные инфоблоков, свойств, секций
2. Сценарии миграции - этап обновления реализуется разработчиком согласно требуемого алгоритма

### Разделы описания

* [Установка и настройка](docs/setup.md)
* [Начало работы](docs/start.md)
* [Обновление площадки](docs/update.md)
* [Интерфейс командной строки](docs/cli.md)
* [Как происходит автоматический учет изменений](docs/auto.md)
* [Скрипты миграций](docs/scripts.md)
