# SpaceshipService

## ТЗ
Сервис для работы с космическими кораблями. Предоставляет полный CRUD функционал.

#### Методы:
- **Create** - создание нового корабля
- **Get** - получение корабля по UUID
- **Update** - обновление существующего корабля
- **Delete** - мягкое удаление корабля

#### Модели данных:
- **SpaceshipInfo** - базовая информация о корабле:
    
    - `name` (string) - название корабля
    - `description` (StringValue) - описание корабля (опционально)
    - `model` (string) - модель корабля
    - `manufacturer` (string) - производитель корабля
    - `price` (double) - цена корабля
- **Spaceship** - полная модель корабля:
    
    - `uuid` (string) - уникальный идентификатор
    - `info` (SpaceshipInfo) - базовая информация
    - `created_at` (Timestamp) - время создания
    - `updated_at` (Timestamp) - время обновления
- **SpaceshipUpdateInfo** - данные для обновления (все поля опциональны):
    
    - `name` (StringValue) - новое название
    - `description` (StringValue) - новое описание
    - `model` (StringValue) - новая модель
    - `manufacturer` (StringValue) - новый производитель
    - `price` (DoubleValue) - новая цена