# [ChaosOrganazier](https://cherry-pynya.github.io/ahj_diploma_front/)

## Задание

Создать веб страницу с клоном чат-бота органайзера (не в месенджере!) без использования фреймворков, только JS, HTML и CSS.
У бота есть фронт и [бекенд](https://github.com/cherry-pynya/ahj_diploma_back).

## Сборка

За сборку обеих частей приложения отвечает Webpack.
Чтобы локально запустить нужно:
1. Клонировать оба репозитория.
2. Запустить в режиме разработчика (npm run start) или сделать рабочий билд (npm run build).

## Бекенд

Бекенд реализован на node.js, приложение работает на основе библиотеки Koa, соединение с фронтом устанавливается через WebSocket.

## Что умеет этот бот:

* Сохранение в истории ссылок и текстовых сообщений
* Ссылки (то, что начинается с `http://` или `https://`) должны быть кликабельны и отображаться как ссылки
* Сохранение в истории изображений, видео и аудио (как файлов) - через Drag & Drop (срабатывает при дропе файлов на окно с сообщениями) и через иконку загрузки (скрепка в большинстве мессенджеров)
* Скачивание файлов (на компьютер пользователя)
* Ленивая подгрузка: сначала подгружаются последние 10 сообщений, при прокрутке вверх подгружаются следующие 10 и т.д.
* Синхронизация - если приложение открыто в нескольких окнах (вкладках), то контент должен быть синхронизирован
* Поиск по сообщениям (интерфейс + реализация на сервере)
* Отправка геолокации
* Отображение категорий и фильтрация по ним