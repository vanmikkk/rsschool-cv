# Иван

## Контактная инфоромация

- Telegram: [@blackteawithme](https://t.me/blackteawithme)

## О себе

Моя цель - стать fullstack-разработчиком

Имею среднее специальное образование по направлению
"Разработчик веб- и мультимедийных приложений".

Имею опыт разработки веб-приложений с использованием PHP,
Laravel, Vue.js и других современных веб-технологий.

## Навыки

### Языки программирования и технологии

- HTML
- CSS
- JavaScript
- PHP
- AJAX

### Дополнительно

- Работа с API
- Разработка серверной и клиентской части веб-приложений
- Работа с базами данных

## Пример кода контроллера Laravel:

```php
public function indexId(Request $request)
{
    $token = $request->bearerToken();
    $user_id = optional(Token::where("token", $token)->first())->user_id;
    if($user_id == null){
        return response()->json("Неверный токен авторизации", 401);
    }
    $course_id = $request->input("course_id");

    $course = User_in_course::where("user_id", $user_id)->where("course_id", $course_id)->first();
    $ownerCourse = Course::where("user_id", $user_id)->where("id", $course_id)->first();

    if($course == null && $ownerCourse == null){
        return response()->json("У вас нет доступа к этому курсу", 422);
    }

    $course = Course::where("id", $request->input("course_id"))->first();

    return response()->json($course, 200);
}
```

## Опыт работы

### Дипломный проект Laravel 10 + Vue.js

В рамках дипломного проекта было разработано веб-приложение
с использованием Laravel 10 и Vue.js

Проект включал разработку сервеной части на Laravel и
клиентской части на Vue.js

На данный момент проект недоступен онлайн, так как хостинг
больше не оплачивается.

## Образование

### Среднее специальное образование

Специальность: "Разработчик веб- и мультимедийных приложений".

## Английский язык

### A2-B1

Изучаю английский язык и продолжаю развивать навыки
чтения, понимания технической документации и общения.