
# Web-приложение для определения заполненных форм

#### Тестовое задание Python Junior+ (ООО е.Ком)


#### Принцип работы приложения:

- Приложение получает на вход 4 типа данных;
- Сопоставляет эти типы данных в валидаторе с названиями + проверяет их корректность;
- Исходя из названий оно сопоставляется с шаблонами из БД;
- Если шаблон имеется - возвращаем название шаблона / Если шаблон отсутствует - возвращаем типы полей.

#### Стек:

Python 3.11 | Flask 3.0 | TinyDB 4.8 | pytest 7.4.3

## Установка

#### Колнируем репозиторий
```
  git@github.com:Anstane/test_task_leadhit.git
```

#### Переходим в папку с приложением
```
  cd test_task_leadhit/
```

#### Запускаем docker compose
```
  docker compose up
```
## Референс запросов

#### POST-запрос получающий в ответ название шаблона

```
  POST /get_form
```

```json
{
    "f_name_1": "test@test.ru",
    "f_name_2": "+79101112233"
}
```

#### POST-запрос возвращающий типы полей

```
  POST /get_form
```

```json
{
    "f_name_1": "another random text",
    "f_name_2": "random text"
}
```



## Запуск тестов вручную

```
  docker-compose exec app poetry run pytest -v
```


## Автор

- [Михаил Московкин](https://github.com/Anstane)

