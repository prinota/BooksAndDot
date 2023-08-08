# Техническое задание

## Написать приложение - магазин книг

Можно использовать любую комбинацию UI и слоя данных для реализации

### UI фреймворк

 0. Bootstrap 5
 0. React JS.

### Таблицы

 1. Books - книги (Id, автор, название, год издания)
 2. Authors - авторы
 3. Categorys - категории
 4. Shops - магазины
 5. BooksShops - наличие книг в магазинах
 6. Orders - заказы
 7. Users - пользователи
 8. Roles - роли

Для демонстрации взаимосвязей создать UML-диагрмму.

### Механизмы работы с данными

 1. Адаптер БД (MS SQL Server, PostgreSQL, Entity Framework);
 2. Получение данных через WebAPI (RESTfull);
 3. Чтение/запись в/из локального файла для выгрузки и загрузки данных.

### Режимы работы

 1. Веб-приложение на ASP.NET.
 2. Консольный режим
    реализовать две команды: get и buy
    get = возвращает полный список книг, по умолчанию осторитрованный по Id
    флаги:
    --title=%% вернуть книгу(и) если указанная подстрока встречается в названии, если таких книги нет, написать сообщение;
    --author=%% вернуть книгу(и) только с этим автором, если такой книги нет, написать сообщение;
    --date=%% аналогично, но для даты, дата в формате yyyy-MM-dd, если дата указана неправильно, вывести текст ошибки
    --order-by=[title|author|date] отсортировать список книг по указанному полю, если указано неправильное поле, то вывести текст ошибки

    флаги могут использоваться одновременно, например: `get --author="Тютчев" --order-by="date"` - на выходе должен быть список книг с автором "Тютчев", отсортированных по дате публикации

    buy = убирает одну книгу из списка отображаемых
    обязательный флаг:
    --id=%% Id книги, которую нужно купить

## Основной функционал

### Возможности


В приложении должен быть использован микросервисный подход

#### Для пользователя

 0. Авторизация/Регистрация.
 0. Страница с отображением списка книг.
 0. Возможностью сортировать список по любому из параметров.
 0. Корзина. Кнопка "купить".
 0. Фильтрация по книгам/магаизнам/авторам.
 0. Избранное. Возможность добавить книгу в избранное.
 0. Уведомить о поступлении.

#### Администрирование

 0. Добавление/удаление/редактирование (CRUD) книг, магазинов, заказов, пользователей

### Внешнее взаимодействие

В проекте дожны быть использованы внешние сервисы
 0. Яндекс карты для указания местонахождения магазинов.
 0. Отправка уведомлений в Telegram через чат-бота.

### Документирование

 0. Документирование методов
 0. Документирование функционала при помощи Swagger

### Тестирование

 0. Необходимо написать Unit тесты для самых значимых методов.

### Исходный код

Исходный код должен быть опубликован в Git хранилище. Для значимых классов создать UML-диаграммы.

## Примечание

Дизайн UI, дополнительные функции (добавление/изменение и т.п.) НЕ влияют на оценку выполнения задачи

Структура классов, открытая к расширению, приветствуется.

Если данные берутся из файла: скинуть файл со списком книг.
Если данные берутся из БД: прислать бэкап или скрипт развёртывания/заполнения БД.


## BesPredel63 - подключился
