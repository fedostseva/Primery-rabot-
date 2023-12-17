Задание

1. Выполнить Post запрос из документации. Запомнить place_id созданной локации
2. Выполнить Get запрос, из документации, с полученным place_id и получить 200 статус-код Позитивное тестирование
3. Выполнить Put запрос, из документации, с полученным place_id и получить 200 статус-код Позитивное тестирование
4. Выполнить Delete запрос, из документации, с полученным place_id и получить 200 статус-код - Позитивное тестирование

Задание - Решение 

Метод POST

Запрос:
Base URL: https://rahulshettyacademy.com
Resource: /maps/api/place/add/json
Параметр для всех запросов: key=qaclick123
Body:
{
"location": {
"lat": -38.383494,
"lng": 33.427362
}, "accuracy": 50,
"name": "Frontline house"
"phone_number": "(+91) 983 893 3937",
"address": "29, side layout, cohen 09",
"types": [
"shoe park",

"shop"
],
"website": "http://google.com",
"language": "French-IN"
}


Ответ:
Статус: 200. Запрос прошел успешно
{
"status": "OK",
"place_id": "dea036e58d6773b3f8bfb256249a1593",
"scope": "APP",
"reference": "1f71a23b137407leecbb70eed1054cf9
1f71a23b1374071eecbb70eed1054cf9",
"id": "1f71a23b1374071eecbb70eed1054cf9"
} 


![POST](https://github.com/fedostseva/Primery-rabot-/assets/153892255/e1311cb0-462e-4361-9e0b-b6a57fd76d53)


Метод PUT

Запрос:
Base URL: https://rahulshettyacademy.com
Resource: /maps/api/place/update/json
Параметр для запросов: key = qaclick123
Body:
{
"place_id":"c104d917f4b60e2c9a5feda6c9cbf279", "address":"100 Lenina street, RU",
"key":"qaclick123"
}


Ответ:
Статус: 200, Запрос прошел успешно
{
"msg": "Address successfully updated"
}
Статус: 404. Ошибка, локация с таким place_id отсутствует
{
"msg": "Update address operation failed, looks like the data doesn't exists"
}


![PUT](https://github.com/fedostseva/Primery-rabot-/assets/153892255/c990956e-cb4e-4d27-b584-df7840424e86)

![PUT 1](https://github.com/fedostseva/Primery-rabot-/assets/153892255/ba788d8f-9e87-4432-afaf-c85159289bae)


Метод GET

Base URL: https://rahulshettyacademy.com
Resource: /maps/api/place/get/json
Параметр для запросов: key = qaclick123, place_id


Ответ:
Статус: 200. Запрос прошел успешно
{
"location": {
"latitude": "-38.383494",
"longitude": "33.427362"
},
"accuracy": "50",
"name": "Frontline house",
"phone_number": "(+91) 983 893 3937", "address": "29, side layout, cohen 09", "types": "shoe park,shop", "website": "http://google.com", "language": "French-IN"
}
Статус: 404. Ошибка, локация с таким place id отсутствует
{
"msg": "Get operation failed, looks like place_id doesn't exists"
} 

![GET](https://github.com/fedostseva/Primery-rabot-/assets/153892255/f88d64eb-12a8-4aed-bdb4-f2c3a6e4e19c)

![GET 1](https://github.com/fedostseva/Primery-rabot-/assets/153892255/376a21aa-fe26-4f17-9943-59252f280c09)


Метод DELETE

Запрос:
Base URL: https://rahulshettyacademy.com
Resource: /maps/api/place/delete/json
Параметр для запросов: key = qaclick123
Body:
{ "place_id":"928b51f64aed18713b0d164d9be8d67f"
}


Ответ:
Статус: 200. Запрос прошел успешно
{
"status": "OK"
}
Статус: 404. Ошибка, локация с таким place_id отсутствует
{
"msg": "Delete operation failed, looks like the data doesn't exists"
}

![DELETE](https://github.com/fedostseva/Primery-rabot-/assets/153892255/e10c3f96-d242-470f-a6f0-7e9ac416b93f)

![DELETE 1](https://github.com/fedostseva/Primery-rabot-/assets/153892255/33867543-151a-4d72-9a16-07daadf4f2f0)




