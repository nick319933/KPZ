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
- ![[screenshot-2025-06-20_11:11:49.png]]
#### 2. Створити конфігурацію Axios:

- Створити окремий файл (наприклад, src/api/axios.ts)
    
- Налаштувати базовий baseURL, заголовок Content-Type, токен авторизації:
```
axios.defaults.baseURL = import.meta.env.VITE_API_BASE_URL;
	axios.defaults.headers.common['Authorization'] = `Bearer ${import.meta.env.VITE_API_AUTH_TOKEN}`;
```
- ![[screenshot-2025-06-20_11:11:10.png]]

#### 3. Замінити мок-функції на реальні HTTP-запити:
У файлі з API-функціями (src/api/posts.ts або аналогічному) замінити реалізацію:
- getAllEntities() → GET /posts
- getEntityById(id) → GET /posts/:id
- createEntity(data) → POST /posts
- updateEntity(id, data) → PUT /posts/:id
- deleteEntity(id) → DELETE /posts/:id
- ![[screenshot-2025-06-20_11:33:49.png]]

#### Виконання CRUD-операцій через UI (DevTools → вкладка Network)
- GET /posts
	- ![[screenshot-2025-06-20_11:04:16.png]]
- POST /posts
	- ![[screenshot-2025-06-20_11:07:31.png]]
	- ![[screenshot-2025-06-20_11:07:57.png]]
- GET /posts/:id
	- ![[screenshot-2025-06-20_11:08:44.png]]
- PUT /posts/:id
	- ![[screenshot-2025-06-20_11:32:26.png]]
- - DELETE /posts/:id
	- ![[screenshot-2025-06-20_11:09:38.png]]
	- ![[screenshot-2025-06-20_11:09:55.png]]
	