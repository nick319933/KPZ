## Практично-лабораторне заняття №6

### Розробка UI для реалізації CRUD-операцій

### Мета
Створити користувацький інтерфейс для взаємодії з реалізованим RESTful API, що надає можливість перегляду, створення, редагування та видалення екземплярів певної сутності. Розробка ведеться на базі React з використанням TanStack Router для реалізації маршрутизації.

### Завдання

Використовуючи boilerplate-проєкт [vite-react-boilerplate](https://github.com/RicardoValdovinos/vite-react-boilerplate), для сутності Post, яка була створена в роботі “Реалізація нової сутності, створення CRUD-операцій та відповідного RESTful API”

1. Сторінка колекції екземплярів сутності (/posts)
	- Реалізувати рендеринг списку всіх доступних екземплярів сутності.
	- Для кожного елемента відображати основну інформацію (ключові поля).
	- Передбачити можливість переходу на сторінку конкретного екземпляра (/posts/:id).
	- Додати кнопку "Створити новий екземпляр", яка веде на маршрут /posts/new.
	- Реалізувати можливість видалення елемента з колекції (з підтвердженням дії).
2. Сторінка окремого екземпляра сутності (/posts/:id або /posts/new)
- У режимі перегляду (/posts/:id) реалізувати:
	- відображення повної інформації про екземпляр;
	- можливість редагування (форма з полями);
	- кнопку для збереження змін (Update).
- У режимі створення (/posts/new) реалізувати:
	- форму з порожніми полями для введення нових даних;
	- кнопку для збереження нового екземпляра (Create).

## React компоненти
1. React компонент для відображення списку постів
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-20-40.png)
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-20-56.png)
2. React компонент для редагування поста
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-19-33.png)
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-21-26.png)
4. React компонент для створення нового поста
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-22-31.png)
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-23-16.png)

## Роутери
1. Роутер для React компоненту для відображення списку постів
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-25-20.png)
2. Роутер для React компоненту для редагування поста
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-27-12.png)
3. Роутер для React компоненту для створення нового поста
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-27-50.png)

## Mок-функцій
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-28-56.png)


## Результати роботи:
1. Список постів
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-32-01.png)
2. Редагування поста
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-34-08.png)
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-34-45.png)
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-35-02.png)
4. Видалення поста
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-35-48.png)
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-35-56.png)
5. Створення поста
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-36-51.png)
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-37-04.png)
	![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR6/screenshots/Screenshot%20from%202025-05-27%2021-37-37.png)
