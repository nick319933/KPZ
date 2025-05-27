# Практично-лабораторне заняття №4
## Тема: Реалізація нової сутності, створення CRUD-операцій та відповідного RESTful API
---
## 1. Створити нову сутність Post:
Визначити поля:
- `id`: UUID, первинний ключ 
- `title`: рядок, обов’язковий
- `content`: текст, необов’язковий
- `createdAt`: дата створення, автоматично заповнюється
- `updatedAt`: дата оновлення, автоматично оновлюється
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-09%2011-51-11.png)

## 2. Створити та застосувати міграцію:
- Згенерувати міграцію для нової сутності.
    ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/photo_2025-05-09_11-19-21.jpg)
    ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-09%2011-36-26.png)
- Запустити міграцію через CLI.
    ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-09%2011-22-44.png)
- Перевірити у базі даних (наприклад, через pgAdmin або консоль), що структура таблиці відповідає очікуваній.
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-09%2011-37-48.png)

## 3. Реалізувати RESTful API для CRUD-операцій:
- Використовувати контролер, DTO, роутер та сервіс за прикладом реалізації для User.
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2015-53-03.png)
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2015-53-22.png)
- Create: створення нового поста
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2016-02-02.png)
- Read:
	- отримання всіх постів
		![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2016-03-41.png)
	- отримання одного поста за ID
		![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2016-04-42.png)

- Update: оновлення поста за ID
    ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2016-07-05.png)
- Delete: видалення поста за ID
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2016-07-05.png)

## 5. Протестувати REST API через Postman:
- Створити окрему колекцію для запитів.
    ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2017-03-09.png)
- Додати приклади:
	- створення поста:
		![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2017-04-02.png)
	- отримання всіх постів:
		![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2017-05-46.png)
	- отримання поста за ID:
		![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2017-06-34.png)
	- оновлення поста:
		![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2017-07-38.png)
	- видалення поста:
		![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR4/screenshots/Screenshot%20from%202025-05-22%2017-08-23.png)

## Висновок:
- Коментарі щодо особливостей реалізації або складнощів під час виконання:
	- **Робота з параметрами запиту та маршруту (query vs params)** 
		Було важливо правильно розділити, коли використовувати `req.params` (для ID в URL) і `req.query` (для фільтрації). Помилкове використання призводило до помилок типу в TypeScript.
	- **Робота з TypeORM  
		Особливу увагу приділив обробці методів findOne, update, delete, які можуть повертати неочікувані значення (наприклад, при неіснуючому ID).
