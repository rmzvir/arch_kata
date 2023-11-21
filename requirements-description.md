# Описание требований
## Описание и диаграммы пользовательских сценариев

1. Сценарии администратора системы:
   - Создание профиля администратора
     - Система устанавливает дефолтной профиль администратора
     - Администратор заходит в систему под дефолтным профилем и создает себе аккаунт через панель администратора

        ![](/user-scenarios/create_admin_account.png)
   - Регистрация площадок мероприятий
     - Администратор создает/обновляет/удаляет профиль площадки мероприятия (обмениваясь информацией через электронную почту/мессенджер с представителем площадки)
    
        ![](/user-scenarios/create_music_worker_account.png)
   - Регистрация исполнителей
      - Администратор создает/обновляет/удаляет профиль исполнителя (обмениваясь информацией через электронную почту/мессенджер с исполнителем)
      - 
        ![](/user-scenarios/create_music_worker_account.png)
   - Регистрация менеджеров радиостанции
      - Администратор создает/обновляет/удаляет профиль менеджеров радиостанции (обмениваясь информацией через электронную почту/мессенджер с менеджером радиостанции)
        
        ![](/user-scenarios/create_company_manager_account.png)
   - Регистрация бизнес-партнера
      - Администратор создает/обновляет/удаляет профиль бизнес-партнера (обмениваясь информацией через электронную почту/мессенджер с бизнес-партнером)
      - 
        ![](/user-scenarios/create_partner_account.png)
1. Сценарии площадки мероприятия:
    - Создания мероприятия:
       - Площадка мероприятия создает мероприятие через интерфейс управления мероприятиями
       - Площадка мероприятия указывает исполнителя, работающих на мероприятии
       - Исполнитель предлагает свой репертуар (набор треков) для мероприятия
       - Площадка мероприятия создает/обновляет/удаляет репертуар (обмениваясь информацией через электронную почту/мессенджер с исполнителем)
       - Создает анонс мероприятия, которое отправляется слушателям, зарегистрированном в системе и исполнителям
       - Подготовка мероприятия:
          - Площадка мероприятия может создавать события (нотификации) для участников мероприятия (слушатели, исполнители)
          - Площадка мероприятия рассылает анонс исполнителям с программой мероприятия
          и ожидает согласия на выступление (детали выступления обсуждаются участниками электронную почту/мессенджер с исполнителем)

         ![](/user-scenarios/create_music_event.png)
   - Обновление мероприятия:
       - Площадка мероприятия сохдает обновление структуры/хода проведения мероприятия
       - Исполнитель и слушатель получают обновление по мероприятию
    
        ![](/user-scenarios/update_music_event.png)
    - События в проведении мероприятия:
       - создает голосования, определяющего очередность выступления:
            - за очередность треков (из фиксированного списка)
        
              ![](/user-scenarios/vote_for_determine_song_at_music_event.png)  
            - за очередность исполнителей        
  
              ![](/user-scenarios/vote_for_custom_song_at_music_event.png)  
       - создает событие, определяющего оценивание репертуара
            - оценка трека
            - оценка исполнителя
              
              ![](/user-scenarios/rating_for_participant_at_music_event.png)  
    - Получение отчетов по мероприятию:
        - площадка мероприятия получает выгрузка отчета о мероприятии (динамика голосования, выставление оценок, показатели оценок с разбивкой по трекам и исполнителям)

        ![](/user-scenarios/create_events_report.png)
2. Сценарии исполнителя на мероприятии:

    - Регистрация исполнителя на мероприятие
        - получение уведомлений площадок о новых мероприятий в мобильном приложении
        - согласие на участие по согласованной программе мероприятия

        ![](/user-scenarios/create_events_report.png)
    - Участие в мероприятии:
        - исполнитель создает голосования за следующий трек
        - исполнитель видит итог голосования за следующий трек
    - Получение отчетов по мероприятию:
        - исполнитель получает выгрузка отчета о своем выступлении (динамика голосования, выставление оценок, показатели оценок)
          
      ![](/user-scenarios/registry_participant_to_event.png)
3. Сценарии слушателя мероприятия:

    - Регистрация профиля слушателя
       - слушатель качает мобильное приложение
       - регистрируется в системе, указывая:
            - ФИО
            - alias (уникальный в рамках системы)
            - пол (опционально)
            - возраст (опционально)
       - профиль хранится локально в бд приложения и обновляется при открытии приложения на мобильном устройстве
       - профиль регистрируется в системе

       ![](/user-scenarios/create_customer_account.png)
    - Получение нотификаций слушателем
        - приложение слушателя получает сообщения о новых мероприятиях
        - слушатель может заявить участия в мероприятии, и подписаться на нотификации по нему (кнопка, опционально)
        - слушатель видит в профиле данные по мероприятия:
            - название
            - место проведения
            - время проведения
            - программу:
                - исполнители
                - треки
                  
      ![](/user-scenarios/registry_customer_to_event.png)
    - Голосование за следующий трек (фиксированный из списка):
        - пользователь набирает название трека
        - трек отправляется на голосование
        - итог голосования отображается пользователю в период голосования
     
       ![](/user-scenarios/customer_vote_for_determine_song.png)
    - Голосование за следующий трек (пожелание пользователя):
        - пользователь набирает название трека
        - трек валидириуется по БД системы, содержащей треки
        - список самых популярных треков встает на голосование
        - итог голосования отображается пользователю в период голосования
     
       ![](/user-scenarios/customer_vote_for_custom_song.png)
    - Оценка исполнителя:
        - пользователь выбирает исполнителя
        - проставляет оценку
        - оценка отображается пользователю в период голосования

      ![](/user-scenarios/customer_rating_for_participant_at_music_event.png)
4. Сценарии  бизнес-партнеров:
    - Создает заявку на получения статистики по мероприятиям
    - Система делает соответсвующую выгрузку
    - Бизнес-партнер отправляет данные партнеру

       ![](/user-scenarios/create_events_report.png)
      
5. Сценарии  бменеджера радиостанции:
    - Создает заявку на получения статистики по мероприятиям
    - Система делает соответсвующую выгрузку
    - Бизнес-партнер отправляет данные партнеру

       ![](/user-scenarios/create_events_report.png)
## Архитектурные свойства (атрибуты качества)

###  Архитектурная аналитика

1. Работа системы планируется на начальном этапе до тысячи человек на одном мероприятии, с перспективой роста до десятков тысяч человек.

2. Количество мероприятий на начальном этапе - до 10 в месяц, в перспективе до сотни в месяц.
   Возможно одновмеренное проведение несколько мероприятий в один момент времени.

3. Средняя длительность мероприятия 3 часа. В рамках такого мероприятия ожидается до 200 треков и выступление до 10 исполнителей, пока каждому из которых возможны голосования и оценка.

4. На начальном этапе входящий трафик с 1 мероприятия оценивается:<br/>
   - в 2_000 рпс
   - 1кб на сообщение
   - 2 мбайта/с
   
   В пиковые дни (выходные):<br/>
   - до 10 мероприятий
   - 20_000 рпс
   - 20 мбайта/с

5. На начальном этапе исходящий трафик с 1 мероприятия оценивается:<br/>
        - 100 байт на сообщение
        - 20 кбайта/с
   В пиковые дни (выходные):<br/>
        - до 10 мероприятий
        - 400 кбайта/с
6. Ведутся переговоры с компаниями-партнерами о продаже статистики музыкальных предпочтений наших слушателей.
   Требуется выгрузка аналитических отчетов на начальном этапе не позже недели с проведения мероприятия.
   Процесс не подразумевает значимой нагрузки

###  Требования к атрибутам качества со стороны бизнеса

| Стейкхолдер                                | Требование                                                                                                                                                                                                                                                                                      | Атрибут качества                                                                        |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| *Радиостанция (менеджмент)*                | - возможности системы подключения тысяч клиентов на крупных мероприятиях<br>- разграничение доступа для разных типов клиентов систем <br>- возможность сохранения статистических результатов мероприятий<br>- возможность использовать базу данных треков, с которыми работает радиостанция<br> | Производительность, совместимость, авторизуемость, аутентифицируемость, бесперебойность |                                                                                                                                                                                                                                                                                             |                                                                                         |                                                                                                                                                                                                                                                                                             |                                                                                         |                                                                                                                                                                                                                                                                                             |                                                                                         |                                                                                                 
| *Радиостанция (технические администраторы* | - быстрое и простое развертывание<br> -динамическая устойчивость к нагрузке<br>                                                                                                                                                                                                                 | модифицируемость, бесперебойность, масштабируемость                                     |
| *Посетители мероприятий*                   | - сохранность личных данных и анонимизация голоса<br>- быстрота работы системы<br>- получение уведомлений                                                                                                                                                                                       | Надежность, конфиденциальность, рассылка нотификаций                                    |                       
| *Исполнители*                              | - стабильность работы системы во время мероприятий<br>- получение уведомлений                                                                                                                                                                                                                   | Бесперебойность, рассылка нотификаций                                                   |  
| *Площадки мероприятий*                     | - возможность выдерживать многократно увеличивающуюся нагрузку на крупных мероприятиях<br> - стабильность работы системы во время мероприятий<br>                                                                                                                                               | Адаптируемость, надежность, масштабируемость                                            |  
| *Бизнес-партнеры*                          | - корректность статистических данных                                                                                                                                                                                                                                                            | Надежность                                                                              |  

###  Ключевые архитектурные свойства
Определив ключевые характеристики архитектуры этого решения, мы сможем определить наименее худшее решение.
Они, наряду с неявными архитектурными характеристиками, затем войдут в общую архитектуру системы.



| Отобранные архитектурные свойства | Источник                                                                                |
|:----------------------------------|:----------------------------------------------------------------------------------------|
| *Совместимость*                   | Использование существующей базы данных треков                                           |
| *Адаптируемость*                  | На крупные мероприятия могут ожидаться взрывной рост трафика на систему                 |
| *Масштабируемость*                | Позитивный пользовательский опыт требует доступность сервиса на популярных мероприятиях |
| *Надежность*                      | Радио стации и ее партнерам нужна корректная информация о пользовательских предпочтений |
| *Производительность*              | Система должна выдерживать целевой трафик от слушателей                                 |

Неявные архитектурные свойства
- авторизуемость, аутентифицируемость
- конфигурируемость
- целостность данных
- масштабируемость (адаптируемость + производительность требует масштабируемость)
- наблюдаемость

###  Архитектурные кванты

| Домен                      | Под-домены                                                                                                                                                                                                | Атрибут качества                                                                                          |
|:---------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| *Пользователи*             | - слушатели концерта (профили)<br>- исполнителя (профили)<br>- площадки мероприятия (профили)<br>- компании-партнеры (профили)<br>- администраторы системы (профили)<br>- менеджеры системы (профили)<br> | Производительность, совместимость, авторизуемость, аутентифицируемость, бесперебойность                   |                                                                                                                                                                                                                                                                                             |                                                                                         |                                                                                                                                                                                                                                                                                             |                                                                                         |                                                                                                                                                                                                                                                                                             |                                                                                         |                                                                                                 
| *Хранение данных*          | - база данных треков<br>- система хранения данных для аналитики<br>- система хранения готовых отчетов<br>- система хранения профилей пользователей<br>- система хранения мероприятий<br>                  | Целостность, масштабируемость                                                                             |
| *Аналитика данных*         | - компании партнеры	<br>- сотрудники радиостанции                                                                                                                                                         | Целостность, производительность, конфигурируемость, масштабируемость, авторизуемость, аутентифицируемость |                       
| *Мероприятие*              | - создание/обновление мероприятием<br>- голосования за следующий трек<br>- оценка трека/исполнителя<br>- голосования за следующего исполнителя                                                            | адаптируемость, надежность, производительность, масштабируемость, наблюдаемость                           |  
| *Рассылка*                 | - нотификации для мобильных приложений                                                                                                                                                                    | наблюдаемость, производительность                                                                         |  
| *Интеграционный интерфейс* | - интеграция с системой рассылки нотификаций<br>- интеграция с базой данных треков радио станции                                                                                                          | совместимость, целостность                                                                                |  

###  Анализ архитектурной аналитики
По результат анализа архитектурных квантов можно сделать следующие выводы
- Не все домены предметной области покрываются основными атрибутами качества, следовательно, нужно использовать распределенный архитектурный стиль
- Атрибуты надежность, производительность требуют гарантий доставки сообщений. В тоже время, часть доменов требуют хранения состояния во внешних системах,
  следовательно, следует рассмотреть использование стиля микросервисов с асинхронной семантикой передачи сообщений
- Часть доменов требует масштабируемость, производительность, адаптивность и обработку большого объема данных в реальном времени (с возможностью исторической аналитики), следовательно, нужно рассмотреть
  возможность использование паттерна event sourcing

Полный список архитектурных решений указан в логе архитектурных решений