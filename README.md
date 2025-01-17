Данный репозиторий содержит инструкцию по вкатыванию в Backend на Java.
Инструкция описана на языке разметки Markdown. Для генерации использован статический генератор сайтов [MkDocs](https://www.mkdocs.org/). Тема - [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)

## Локальное развертывание и отладка

### Установка Python

Python 3.7+. Python можно поставить как из пакетного менеджера операционной системы, так и скачав дистрибутив с [официального сайта](https://www.python.org/).

### Настройка виртуального окружения

Открываем терминал. Для начала, устанавливаем пакет для работы с виртуальными окружениями Python:

`py -m pip install virtualenv`

Создаем папку виртуального окружения:

`py -m virtualenv venv`

После чего, в корне проекта можно увидеть папку venv.
Активируем виртуальное окружение:

`.\venv\Scripts\activate`

Устанавливаем в виртуальное окружение все необходимые для работы пакеты:

`pip install mkdocs-material mkdocs-git-revision-date-localized-plugin mike`

### Запуск

Выполняем в терминале команду:

`mkdocs serve`

В результате будет запущен сайт с инструкцией по адресу `127.0.0.1:8000`.
Подробнее можно почитать [ТУТ](https://squidfunk.github.io/mkdocs-material/creating-your-site).

### Дополнение для контрибьютеров

Принцип расширения документации не меняется. Пишем, используя [Markdown](https://www.markdownguide.org/) ,  а [MkDocs](https://www.mkdocs.org/) отображает в удобном для нас формате. Чтобы понять принцип, по которому строится навигация сайта, стоит обратить внимание на раздел *nav* в файле *mkdocs.yml* в корне репозитория. Верхний уровень навигации автоматически отображается в части сайта (см. св-во *navigation.tabs*) под заголовком.
Визуальное отображение динамически подхватывает изменения, достаточно сохранить редактируемый markdown-файл, зажав в редакторе комбинацию `CTRL + S`.
[MkDocs](https://www.mkdocs.org/) имеет огромное количество плагинов, интересные подборки можно подсмотреть [тут](https://github.com/mkdocs/best-of-mkdocs) и, конечно же, [тут](https://squidfunk.github.io/mkdocs-material/reference/). 
Наконец, я бы обратил внимание на разделы [Setup](https://squidfunk.github.io/mkdocs-material/setup/) и [Reference](https://squidfunk.github.io/mkdocs-material/reference/) в [документации](https://squidfunk.github.io/mkdocs-material/).


## Развертывание онлайн (на платформе Github Pages)

В папке *github/workflows* расположен файл *ci.yml*. В данном файле описана инструкция для платформы *Github Pages*. Как только изменения попадают в ветку *develop*, публикуется новая статическая версия сайта.

**Адрес статической версии сайта**:

 [https://EightM.github.io/JavaBackendStartGuide](https://EightM.github.io/JavaBackendStartGuide)