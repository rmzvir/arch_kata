# Внедрение аутентификации, шифрования и авторизации для сервисов системы
## Статус
Принят
## Контекст
Профили различных типов клиентов содержат данные, которые требуют ограничение доступа и ролевой модели. Необходим механизм обеспечивающий
авторизуемость, шифрования и аутентифицируемость для ряда сервисов
## Решение
Использование шифрования данных для внешних подключений в системе.
Внедрение сервиса аутентификации для сервиса управления слушателями. Предлагается использование basic аутентификации
Внедрение сервиса аутентификации для сервиса управления мероприятиями. Предлагается использование basic аутентификации
Создание ролевой модели для сервиса управления мероприятиями.
Выделение следующие роли:
- администратор
- менеджер радиостанции
- площадка мероприятия
- исполнитель на мероприятии
- менеджер бизнес-партнера компании
## Последствия
### Позитивные:
- Шифрование обеспечивает конфиденциальность передаваемых данных между клиентов и системой
- Простота реализации
- Не требует отдельного сервиса аутентификации

### Негативные:
- Требуется время на реализацию
		