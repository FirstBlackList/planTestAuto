# **План автоматизации тестирования возможности записаться на обучение профессии "Тестировщик ПО" [на веб-сайте Netology.ru](https://netology.ru/)**

**Цель плана по автоматизации** - описание процесса автоматизации, необходимых инструментов, затраченного времени и возможных рисков при тестировании перехода к форме записи на курс "Тестировщик ПО" и её заполнения.
#

## <p style="color: turquoise; text-align: center">**Перечень автоматизируемых сценариев**

### <p style="color: green">**UI тестирование сценариев перехода к форме записи на курс**
|Название|Путь до формы|
|-|-|
| **Путь до страницы Тестировщик ПО**|
| Каталог курсов - хедер| Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Кнопка **"Каталог курсов"** -->Программирование -->Новичкам -->прокрутить вниз и найти Тестировщик ПО|
| Все курсы - фильтры| Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Кнопка **"Каталог курсов"** -->Все курсы -->Фильтры: Новичкам -->Кнопка **"Показать курсы"** -->прокрутить вниз и найти Тестировщик ПО|
| Все курсы - строка поиска| Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Кнопка **"Каталог курсов"** -->Все курсы -->Строка поиска (Ввести с клавиатуры Тестировщик ) -->Тестировщик ПО|
| Каталог курсов - футер - фильтры| Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Кнопка **"Каталог курсов"** -->Все курсы -->Фильтры: Платное -->Кнопка **"Показать курсы"** -->прокрутить вниз и найти Тестировщик ПО|
| Каталог курсов - футер - строка поиска| Главная страница [веб-сайт Netology.ru](https://netology.ru/)Каталог курсов --> Строка поиска (Ввести с клавиатуры Тестировщик ) -->Тестировщик ПО|
| Программирование - фильтры| Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Программирование -->Фильтры: Платное -->Кнопка **"Показать курсы"** -->прокрутить вниз и найти Тестировщик ПО|
| Программирование - строка поиска| Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Программирование -->Строка поиска (Ввести с клавиатуры Тестировщик )--> Тестировщик ПО|
| Баннер в нижней части - каталог курсов | Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Прокрутить страницу вниз -->Вкладка **"Обучение"** -->Каталог курсов -->прокрутить вниз и найти Тестировщик ПО|
| Баннер в нижней части - каталог курсов - строка поиска| Главная страница [веб-сайт Netology.ru](https://netology.ru/) -->Прокрутить страницу вниз -->Вкладка **"Обучение"** -->Каталог курсов -->Строка поиска (Ввести с клавиатуры Тестировщик ) -->Тестировщик ПО|
| **Путь до формы записи**|                                                                                                                                           
| Кнопка **"Записаться"**| Главная страница профессии [Тестировщик ПО](https://netology.ru/programs/qa)-->Кнопка **"Записаться"**-->Переадресация в футер страницы **"Записаться / Получить консультацию"** -->Кнопка **"Записаться"**|
| Кнопка **"Условия акции"**| Главная страница профессии [Тестировщик ПО](https://netology.ru/programs/qa)-->Кнопка **"Условия акции"** -->Купить курс -->Переадресация в футер страницы **"Записаться / Получить консультацию"** -->Кнопка **"Записаться"**|
| Форма в футере| Главная страница профессии [Тестировщик ПО](https://netology.ru/programs/qa)-->Футер **"Записаться / Получить консультацию"** -->Кнопка **"Записаться"**|                                                                                      
| Зарегистрированный пользователь| Главная страница профессии [Тестировщик ПО](https://netology.ru/programs/qa)-->При прокрутке вниз появляется кнопка рядом с аватаром пользователя-->Кнопка **"Записаться"** -->Футер **"Записаться / Получить консультацию"** -->Кнопка **"Записаться"**|
#

|**Отправка формы**| **Результат**|
-|-|
| **Позитивный тест:** |
| **Заполнение полей [формы](https://netology.ru/programs/qa#/order)** валидными данными -> клик по кнопке **"Записаться"**. | данные успешно отправлены и могут быть просмотрены в используемой базе данных, появится всплывающее окно об успешном завершении записи |
| **Негативные тесты:**|
| **Отправка пустой [формы](https://netology.ru/programs/qa#/order)** -> клик по кнопке **"Записаться"**| отправки данных не произойдет, под незаполнеными полями появятся сообщения **"Обязательное поле"**|
| **Отправка [формы](https://netology.ru/programs/qa#/order) с одним пустым полем "ИМЯ":** поле имя остается пустым, поле **"ТЕЛЕФОН"** заполняется валидными данными -> клик по кнопке **"Записаться"**| отправка данных не произойдет, под незаполнеными полями появятся сообщения **"Обязательное поле"**|
| **Отправка [формы](https://netology.ru/programs/qa#/order) с одним пустым полем "ТЕЛЕФОН":** поле телефон остается пустым, поле **"ИМЯ"** заполняются валидными данными -> клик по кнопке **"Записаться"**| отправки данных не произойдет, под полем телефон появится сообщение **"Обязательное поле"**|
| **Проверка валидации полей:** |
| **Поле "ИМЯ" [формы](https://netology.ru/programs/qa#/order) заполняется не валидными данными**, поле **"ТЕЛЕФОН"** заполняется валидными данными -> клик по кнопке **"Записаться"**| отправки данных не произойдет, под полем **"ИМЯ"** появится сообщение **"Имя должно состоять из русских букв, дефисов и пробелов"**|
| **Поле "ИМЯ" [формы](https://netology.ru/programs/qa#/order) заполняется одним буквенным символом**, поле **"ТЕЛЕФОН"** заполняется валидными данными -> клик по кнопке **"Записаться"**| отправки данных не произойдет, под полем имя появится сообщение **"Должно быть не короче 2 символов"**|
| **Поле "ТЕЛЕФОН" [формы](https://netology.ru/programs/qa#/order) заполняется не валидными данными**, поле **"ИМЯ"** заполняется валидными данными -> клик по кнопке **"Записаться"**| отправки данных не произойдет, под полем телефон появится сообщение **"Введите номер в формате: +9 (999) 999-99-99"**|
| **Отправка [формы](https://netology.ru/programs/qa#/order) с данными из ранее успешно отправленой формы:** заполнение полей ранее успешно отправленными валидными данными -> клик по кнопке **"Записаться"** (из пункта успешная отправка) | данные отправлены, появится всплывающее окно о ранее созданной записи|

### **<p style="color: green">API тестирование при отправке POST запроса на status code и отсутствие новых записей в БД:**

- Проверка статуса и совпадения валидных данных отправленных через UI формы записи на курс **"Тестировщик ПО"** с данными в body POST-запроса к серверу и новыми данными из БД -> результат:
  - **статус 200, совпадения валидных данных**
- Проверка статуса и отсутствие новых записей в БД при отправке пустого body в POST-запросе отправки формы записи на курс **"Тестировщик ПО"** -> результат:
  - **статус 500, отсутствие новых записей в БД**
- Проверка статуса и отсутствие новых записей в БД при отправке пустого значения у атрибута name в body в POST-запросе отправки формы записи на курс **"Тестировщик ПО"** -> результат:
  - **статус 500, отсутствие новых записей в БД** 
- Проверка статуса и отсутствие новых записей в БД при отправке пустого значения у атрибута phone в body в POST-запросе отправки формы записи на курс **"Тестировщик ПО"** -> результат:
  - **статус 500, отсутствие новых записей в БД** 

#

## <p style="color: turquoise; text-align: center">**Перечень используемых инструментов с обоснованием выбора**

**1. Среда разработки - IntelliJ IDEA** Обладает широкими возможностями проверки качества и валидности кода с помощью инспекций, которые выполняются "на лету", один из самых популярных и удобных редакторов для Java с поддержкой всех последних технологий и фреймворков.

**2. Язык программирования: Java JDK 11** Имеет набор готового ПО для разработки и запуска приложений.

**3. Система автоматической сборки: Gradle**
- Приемущества:

  - позволяет выполнять инкрементные сборки, проверяет, какие задачи обновлены, а какие нет как следствие -> гораздо меньшее время сборки.
  - Gradle - настраиваемое свойство благодаря чему может быть модифицирован под различные технологии для различных проектов.
  - Gradle Wrapper. Опция разрешает реализацию сборок, созданных в Gradle, на машинах, где система не установлена. Это упрощает непрерывную интеграцию серверов.
  - выигрывает у Maven, когда речь идёт о зависимостях API и реализации, а также возможности одновременного безопасного кэширования. Хранение метаданных репозитория вместе с кэшированными зависимостями, гарантируют, что два или более проекта, использующих один и тот же кэш, не перезапишут друг друга.
  - совместим с IVY Metadata, что позволяет определить пользовательские правила для указания версии для динамической зависимости и разрешать конфликты версий.
  - скрипт Gradle проще и меньше, разница заметна при реализации сборок с большим числом зависимостей.
  - структурирование сборки. Благодаря использованию общих принципов проектирования Gradle позволяет создать удобный, понятный и быстро реализуемый проект.
  - открытый код, множество полезных плагинов, библиотек и других компонентов.

**4. Тестовая среда: TestNG**
- Приемущества:

  - имеет, по сравнению с JUnit, множество опций у аннотаций Before и After
  - поддерживает зависимые тесты
  - многопоточное выполнение
  - улучшенная система отчётов

**5. Selenide для UI тестирования** 
- Приемущества:

  - поставляется с хорошими API
  - поддержка Ajax
  - интеллектуальное ожидание
  - удобные методы
  - автоматические скриншоты
  - транспарентный web-driver

**6. Rest Assured для API тестирования** - библиотека Java для тестирования API RESTful, позволяет автоматизировать тестирование get и post запросов.

**7. Lombok** - библиотека Java, позволяющая сократить шаблонный код, тем самым оптимизировать работу разработчика.

**8. JavaFaker** - библиотека для генерации случайных тестовых данных.

**9. Система репортинга: Allure** - гибкий и легкий инструмент построения отчётов автотестов, упрощающий их анализ. Позволяет получить не только краткую информацию о ходе выполнения тестов, но и предоставит максимум полезной информации.

**10. Git и GitHub** - Git достаточно прост и удобен для управления исходным кодом, самая популярная система контроля версий, поэтому достаточно хорошо взаимодействует с различными ОС. GitHub специализированный веб-сервис с удобным интерфейсои, интегрирован с Git.

**11. Docker Desktop** - платформа контейнеризации с открытым исходным кодом. для автоматизации развёртывания приложений в виде переносимых автономных контейнеров (например СУБД MySQL)
#

## <p style="color: turquoise; text-align: center">**Перечень необходимых разрешений, данных и доступов**

1. Письменное разрешение на тестирование и автоматизацию от руководства Нетологии
2. Технические данные для полей ввода (что является вылидными/невалидными данными)
3. Доступ в тестовый режим сервиса и тестовую базу данных для проверки результатов отправки валидных/невалидных тестовых данных через форму для записи
 - (Прим.) Желательно наличие статистики в которй отображены наиболее предпочтительные пути пользователей при взаимодействии с сайтом на выбор данного направления в обучении.

#

## <p style="color: turquoise; text-align: center">**Перечень и описание возможных рисков при автоматизации**

1. Инструменты автоматизированного тестирования могут отнять достаточно много времени и средств.
2. Недостаточное (или же полное отсутствие) статистики по предпочтительному пути поиска реальным пользователем, несёт риск не проверить ее в первую очередь.
3. Есть риск отправить "ложный" запрос для записи на курс в службу обработки заявок и обратный звонок
4. Действия пользователя могут не совпадать со сценарием тестов, предвидеть и покрыть тестами все возможные негативные сценарии невозможно.
5. Падение автотестов даже при незначительном изменении структуры сайта: элементов, локаторов. (Например: рекламный баннер для записи на курс ).
6. Поддрежание тестов может занять больше времени, чем было запланировано.

#

## <p style="color: turquoise; text-align: center">**Перечень необходимых специалистов для автоматизации**

<p style="text-align:center">
С данным проектом вполне может справиться junior автоматизатор, который знаком и уже работал с перечисленными выше инструментами, обладающий практическим основами UI и API тестирования, а также навыками написания автотестов с использованием паттерна Page Object.
</p>

#

## <p style="color: turquoise; text-align: center">**Интервальная оценка с учётом рисков в часах**
Для junior QA (с запасом ~20%) --> 36 часов.
- Входит:

  - подготовка мануальных тестов
  - настройка окружения 
  - автоматизация мануальных тестов
  - прогон тестов
  - формирование отчета о тестировании
