# Руководство пользователя
## 1. Общая информация
### 1.1. Назначение системы
Система предназначена для управления очередью линии производства, создания внутреннего заказа на производство партий капкейков и информирования в случае возникновения ошибок для их скорейшего решения.
### 1.2 Краткое описание возможностей
Функциональность компонентов системы обеспечивает следующие возможности:
1. Просмотр очереди;
2. Редактирование очереди;
3. Остановка линии производства, если оно запущено;
4. Запуск линии производства, если оно приостановлено;
5. Создание внутреннего заказа;
6. Просмотр сообщений об ошибках;
7. Просмотр сообщений об устранении ошибок;
8. Просмотр истории внутренних заказов;
9. Выгрузка отчётов о процессе производства;
10. Получение уведомлений о возникновении проблемы;
11. Отправление уведомлений о решении проблемы;
12. Отражение статуса линии производства и списка уведомлений на информационном табло.

### 1.3. Уровень подготовки пользователей
Пользователь Системы должен уверенно пользоваться ПК, обладать знаниями методологии производства капкейков, используя линию производства.
### 1.4 Список принятых терминов и сокращений
- БД - база данных
- ПК - персональный компьютер
- ЛКМ - левая кнопка мыши
- ПКМ - правая кнопка мыши
- Система - система управления линии производства
## 2. Работа в системе
### 2.1. Вход в систему
Для входа в Систему необходимо в адресной строке браузера ввести адрес <http://...> и подтвердить переход по адресу нажатием кнопки «Enter».
В случае успешного перехода по ссылке Система отобразит форму авторизации.
### 2.2. Авторизация
Для авторизации в системе необходимо ввести имя пользователя и пароль в соответствующие поля формы авторизации и подтвердить ввод нажатием на кнопку «Sign in».  
В случаях ввода в форму авторизации ошибочных данных Система отобразит информационное сообщение «Invalid username or password». Для устранения возникшей проблемы необходимо проверить правильность раскладки клавиатуры и нажатие клавиши «Caps Lock» и повторно ввести данные для авторизации. В случаях если авторизация по-прежнему невозможна, необходимо обратиться к сотрудникам, отвечающим за техническую поддержку системы.
После успешного прохождения процедуры авторизации открывается главная страница Системы, состоящей из:
1.	Формы очереди линии производства;
2.	Формы параметров партии капкейков, находящихся в производстве.
### 2.3. Работа с очередью линии производства
#### 2.3.1. Просмотр информации об очереди
Информация об очереди линии производства доступна на главной странице, на которой отражаются: 
- Партия, находящаяся в производстве;
- Параметры партии, ноходащейся в производстве;
- Последовательность партий в очереди;
- Список возникших ошибок в течение заданного промежутка времени.

#### 2.3.2. Создание внутреннего заказа для линии производства
Для создания внутреннего заказа необходимо нажать кнопку "Изготовить партию" на форме очереди линии производства. В открывшемся окне необходимо ввести основные параметры внутреннего заказа: 
- количество капкейков в партии;
- тип капкейков;
- положение заказа в очереди (на данном этапе невозможно приостановить текущее производство партии и заменить на только что созданное);
- время предположительного окончания производства партии (данный параметр будет рассчитан автоматически и не допустит "наслоения" производства одной партии на другую, но при его редактировании возникнет риск простоя, который берёт на себя создатель данного заказа).

По завершении ввода параметров необходимо нажать на кнопку "Сохранить".

#### 2.3.3. Редактирвоание заказа для линии производства
Для редактирования заказа необходимо выбрать соответствующий заказ в очереди (Система не допустит редактирования заказа, уже находящегося в производстве) и нажать на икноку "карандаш". В открывшемся окне будут выведены сохранённые значения парметров. Необходимо изменить значения парметра\ов и нажать на кнопку "Сохранить".
#### 2.3.4. Удаление заказа для линии производства
Для удаления заказа необходимо выбрать соответствующий заказ в очереди (Система не допустит удаления заказа, уже находящегося в производстве) и нажать на иконку "мусорное ведро". В открывшемся окне необходимо подтвердить удаление, нажатием на кнопку "Удалить".
#### 2.3.5. Остановка линии производства
Для остановки линии необходмо нажать на кнопку "Остановить производство". В открывшемся окне необходимо подтвердить остановку линии производства нажатием на кнопку "Остановить".
#### 2.3.6. Запуск линии производства
Для запуска линии необходимо нажать на кнопку "Возобновить производство". В открывшемся окне необходимо подтвердить возобновление линии производства нажатием на кнопку "Возобновить".
### 2.4. Работа с ошибками линии производства для работника цеха
#### 2.4.1. Просмотр списка ошибки на линии производства
На форме очереди линии производства в окне списка ошибок возникнет наименование ошибки с кратким описанием и статусом "Блокирующая" (ошибки с данным статусом выделяются на фоне остальных). Данная ошибка также выведется на информационном табло.
Пользователь с ролью "Работник цеха" также увидит наименование и краткое описание ошибки на планшетной версии Системы.
#### 2.4.2. Решение ошибки
После того, как работник физически устранит ошибку, блокирующую производство, и нажмёт на кнопку "Проблема устранена" на планшетной версии Системы, статус ошибки изменится на "Устранена". Данная ошибка также исчезнет с информационного табло.
### 2.5. Выгрузка отчётов о процессе производства
Возможность выгрузки отчёта доступна на форме очереди линии, настроив временной диапазон и нажав на кнопку "Выгрузить отчёт".
Отчёт выгружается в формате .xlsx и содержит:
- Выбранный временной диапазон;
- Список произведённых внутренних заказов;
- Внутренний заказ, находящийся в производстве в конце выбранного диапазона (если такой есть);
- Параметры всех внутренних заказов;
- Список всех ошибок;
- Наименования, кр. описания и статусы ошибок;
- Уведомления о решении ошибок в привязке к ошибкам.
## 3. Действия при отказах работы системы
В данном разделе приведено описание действий пользователя в случаях отказа технических средств, при несанкционированном вмешательстве в данные проекта, а также действий в случаях обнаружения сбоев в работе Системы и ошибок в передаче данных.
### 3.1.	Действия при отказах Системы или иных ошибок 
В случаях отказа Системы или иных ошибок необходимо обратиться к сотрудникам:
- ФИО
- ФИО
- ...
### 3.2.	Несанкционированное вмешательство в данные
В случаях обнаружения несанкционированного вмешательства в данные, необходимо обратиться к сотрудникам, отвечающим за техническое обеспечение защиты информации от несанкционированного доступа:
- ФИО
- ФИО
- ...

### 3.3.	Действия при обнаружении сбоев в работе Системы
Для восстановления работоспособности в случае отсутствия ответа Системы на действия пользователя, необходимо осуществить повторный вход в Систему.
Если при повторном входе в систему работоспособность не востановлена, необходимо обратиться к сотрудникам, приведённым в [3.1.](https://github.com/bel64enok/Test-Cupcake/edit/main/docs/User_guide.md#31%D0%B4%D0%B5%D0%B9%D1%81%D1%82%D0%B2%D0%B8%D1%8F-%D0%BF%D1%80%D0%B8-%D0%BE%D1%82%D0%BA%D0%B0%D0%B7%D0%B0%D1%85-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B-%D0%B8%D0%BB%D0%B8-%D0%B8%D0%BD%D1%8B%D1%85-%D0%BE%D1%88%D0%B8%D0%B1%D0%BE%D0%BA)
