# Лабораторне заняття №1 
## Ознайомлення з TypeScript
---
### Завдання 1. Типізація змінних:
#### Умова завдання:
Оголосіть змінні наступних типів: `string`, `number`, `boolean`, `array`, `object`. Створіть функцію, яка приймає як аргумент об'єкт із полями `name` (тип `string`) та `age` (тип `number`) і повертає рядок виду: **"Name: John, Age: 30"**.

#### Код:
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-05-43.png)

#### Перевірки:
JS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-07-03.png)

.D.TS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-07-40.png)

Errors:
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-08-21.png)

Logs:
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-09-04.png)


### Завдання 2. Інтерфейси:
#### Умова завдання:
1. Оголосіть інтерфейс `Person`, який містить поля:
	1. 'name': 'string'
	2. 'age': 'number'
	3. 'address?': 'string' (опціональне поле)
2. Реалізуйте функцію 'printPerson', яка приймає об'єкт типу 'Person' та виводить його дані у консоль.

#### Код:
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-21-40.png)

#### Перевірки:
JS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-22-04.png)

.D.TS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-22-38.png)

Errors
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-23-13.png)

Logs
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-23-42.png)


### Завдання 3. Композитні типи:
#### Умова завдання:
1. Оголосіть об'єднаний тип (union type), наприклад: 
	`type Status = 'success' | 'error' | 'loading';`
2. Реалізуйте конструкцію (наприклад, функцію або умову), яка виводить повідомлення відповідно до значення Status.

#### Код
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-34-39.png)

#### Перевірки:
JS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-35-29.png)

.D.TS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-35-50.png)

Errors
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-36-03.png)

Logs
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-38-35.png)


### Завдання 4. Дженерики:
#### Умова завдання:
1. Реалізуйте функцію `identity<T>(value: T): T`, яка повертає передане їй значення.
2. Використайте її для типів `number`, `string` та `boolean`.

#### Код
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-46-59.png)

#### Перевірки:
JS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-47-34.png)

.D.TS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-47-46.png)

Errors
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-47-51.png)

Logs
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-48-02.png)



### Завдання 5. Класи:
#### Умова завдання:
1. Реалізуйте клас Car, який містить поля:
	1. `model`: `string`
	2. `year`: `number`
2. Додайте метод `getCarInfo()`, який повертає рядок виду: "Model: Toyota, Year: 2020".

#### Код
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-55-45.png)

#### Перевірки:
JS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-56-11.png)

.D.TS
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-56-24.png)

Errors
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-56-47.png)

Logs
![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR2/screenshots/Screenshot%20from%202025-05-07%2014-57-04.png)
