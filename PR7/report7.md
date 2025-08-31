### Практично-лабораторне заняття №7

## Інтеграція клієнтської частини з RESTful API

Мета  
Підключити користувацький інтерфейс до реального серверного API. Ознайомитися з підходами до організації HTTP-запитів через Axios, зберігання токенів доступу, обробки помилок, роботи з .env-змінними. Забезпечити повноцінну взаємодію клієнтської частини з бекендом.

  

### Завдання

Використовуючи реалізовану у попередньому завданні клієнтську частину (інтерфейс для роботи з сутністю Post), внести такі зміни:

#### 1. Налаштування змінних оточення:

- У корені проєкту створити файл .env
    
- Додати до нього такі змінні:
```
	VITE_API_BASE_URL=http://localhost:4000/v1  
	VITE_API_AUTH_TOKEN=your_jwt_token_here
```
- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_11_49.png)
#### 2. Створити конфігурацію Axios:

- Створити окремий файл (наприклад, src/api/axios.ts)
    
- Налаштувати базовий baseURL, заголовок Content-Type, токен авторизації:
```
axios.defaults.baseURL = import.meta.env.VITE_API_BASE_URL;
	axios.defaults.headers.common['Authorization'] = `Bearer ${import.meta.env.VITE_API_AUTH_TOKEN}`;
```
- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_11_10.png)

#### 3. Замінити мок-функції на реальні HTTP-запити:
У файлі з API-функціями (src/api/posts.ts або аналогічному) замінити реалізацію:
- getAllEntities() → GET /posts
- getEntityById(id) → GET /posts/:id
- createEntity(data) → POST /posts
- updateEntity(id, data) → PUT /posts/:id
- deleteEntity(id) → DELETE /posts/:id
- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_33_49.png)

#### Виконання CRUD-операцій через UI (DevTools → вкладка Network)
- GET /posts
	- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_04_16.png)
- POST /posts
	- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_07_31.png)
	- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_07_57.png)
- GET /posts/:id
	- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_08_44.png)
- PUT /posts/:id
	- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_32_26.png)
- - DELETE /posts/:id
	- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_09_38.png)
	- ![Screenshot](https://github.com/nick319933/KPZ/blob/main/PR7/screenshots/screenshot-2025-06-20_11_09_55.png)
	
