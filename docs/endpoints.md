# API Booking System (Liberty Fly)

## Аутентификация

### POST /api/auth/register
Регистрация пользователя  
Доступ: Все  

### POST /api/auth/login
Авторизация пользователя (выдача JWT)  
Доступ: Все  

### GET /api/auth/me
Получение информации о текущем пользователе  
Доступ: Авторизованные  



## Ресурсы

### GET /api/resources
Получение списка ресурсов (с фильтрацией и пагинацией)  
Доступ: Все  

### GET /api/resources/{id}
Получение информации о конкретном ресурсе  
Доступ: Все  

### POST /api/admin/resources
Создание ресурса  
Доступ: Admin  

### PATCH /api/admin/resources/{id}
Обновление ресурса  
Доступ: Admin  

### DELETE /api/admin/resources/{id}
Удаление ресурса  
Доступ: Admin  


## Бронирования

### POST /api/bookings
Создание бронирования  
Доступ: Авторизованные  

### GET /api/bookings
Получение списка своих бронирований  
Доступ: User  

### GET /api/admin/bookings
Получение списка всех бронирований  
Доступ: Admin  

### POST /api/bookings/{id}/cancel
Отмена бронирования  
User — только своё  
Admin — любое  


## Отзывы

### POST /api/bookings/{id}/review
Создание отзыва (только после завершённого бронирования)  

### GET /api/resources/{id}/reviews
Список отзывов ресурса  
