# Blue Yonder Connector — Connector Discovery

**Category:** C46. Warehouse & 3PL Logistics Management  
**Vendor:** Blue Yonder  
**Official Website:** https://blueyonder.com

## 1. Официальный API
- **Базовый URL API:** `https://<tenant>.blueyonder.com/api/v1`
- **Поддерживаемая модель авторизации:** OAuth 2.0 Bearer Token (Client ID + Client Secret)

## 2. Архитектура сущностей
- Ключевые ресурсы платформы Blue Yonder:
  - планы спроса (/demand)
  - запасы (/inventory)
  - транспортировки (/transportation)
  - заказы (/orders)

## 3. Требования к отказоустойчивости и безопасности
- Соблюдение вендорных лимитов запросов (Rate Limiting) с экспоненциальной задержкой.
- Строгая валидация Pydantic-схем на входе и выходе каждого запроса.
- Тестовая точка проверки подключения: `GET /api/v1/inventory/status`.
