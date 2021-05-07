## Курсовой проект по дисциплине "Проектирование информационных систем"

## ФИО, ИДБ-17-06

### 1. Определение требований к модели [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

**Тема ВКР:** Разработка системы визуализации трехмерной сцены музея промышленных достижений

**Объект исследований:** виртуальные музеи

**Предмет исследований:** системы трехмерного моделирования реалистичных сцен

**Процессы верхнего уровня:** [✋](https://github.com/stankin/design-part-2/wiki/sem1)
* **А1** Управление
* **А2** Вычисление положения 3D-объектов на сцене
* **А3** Формирование трехмерной сцены

**Точка зрения:** Директор музея

**Цель моделирования:** Демонстрация работы системы визуализации трехмерной сцены

### 2. Функциональное моделирование процессов (IDEF0) [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

* A-0 (контекстная диаграмма)

![A-0](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/01_A0.png)

* A0 (диаграмма верхнего уровня)

![A0](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/02_A0.png)

* A1 (декомпозиция процесса/процессов внутренней среды)

![A1](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/03_A1.png)

* A3 (декомпозиция процесса/процессов внутренней среды)

![A3](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/04_A3.png)


### 3. Функциональное моделирование программных и информационных средств (DFD) [✋](https://github.com/stankin/design-part-2/wiki/LR-2)

**Конфигурация технических средств:** 
* ПК;


Системные требования:

| Компонент | Рекомендуемое значение  | 
|---|---|
| CPU | Ryzen 5 3600/ i5-9600  | 
| GPU | 3070 RTX/ RX 6800  | 
| RAM | 16 |
| Storage device|SSD|
| OC | Windows 10|

**Конфигурация программных средств:** встроенные

**Допустимые виды хранилищ и их размещение:** Запоминающее устройство ПК

* A11 Автоматизация процесса А11

![A11](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/04_A11.png)

* A13 Автоматизация процесса А13

![A13](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/05_A13.png)

### 4. Описание выбранного процесса [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате прецедента (Use Case) [✋](https://github.com/stankin/design-part-2/wiki/LR-4)

Диаграмма [UML Use Case](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/txt/Uml%20Case)

![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/Uml%20Case.png)

**4.1 Идентификатор прецедента:** A1

**4.2 Название прецедента:** Управление

**4.3 Контекст:** А0 

**4.4 Участники (actors) и цели (goals):**

| Участник  | Категория  | Цель (goal) |
|---|---|---|
| Директор музея | Основной  | Запуск системы |
| Директор музея | Основной  | Утверждение планировки выставки |
| Разработчик | Внешний| Корректировка системы/сцены при необходимости|
| ПК| Инструмент| Стабильное количество кадров|

**4.5 Предусловия (pre-conditions):**

* Система скачана и успешна установлена
* Освоены и настроены клавишы управления

**4.6 Постусловия (post-conditions):**

* Визуализированная сцена

**4.7 Основной поток выполнения (main flow)**:

| Участник  | Действие (activity)  | Ожидаемый результат |
|---|---|---|
| Пользователь | Запускает систему | Успешный запуск системы |
| Пользователь | Управляет персонажем и виртуальной камерой | Передвижение по сцене |
| Пользователь | Взаимодействует с 3D-объектами | Просмотр 3D-объектов |
| Пользователь | Взаимодействует с источниками освещения | Изменение освещенности сцены |

**4.8 Исключения (exceptions):**

| Условие (риск) | Последствия | Реакция |
|---|---|---|
| Система не реагирует на нажатия клавиш | Пользователь не сможет управлять персонажем | Обратиться к разрабочитку |

**4.9 Альтернативы (alternates):**

Не предусмотрено

**4.10 Временные параметры:**

* **Триггер (событие, стартующее прецедент):** Необходимость запустить систему
* **Номинальная частота повторения прецедента:** Не ограниченно

* **Продолжительность прецедента:** Не ограниченно

### 5. Описание структуры объекта [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате ERD (Class) [✋](https://github.com/stankin/design-part-2/wiki/LR-5)

* **Описываемый объект:** Система визуализации трехмерной сцены музея промышленных достижений

* **Диаграмма [UML Class](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/txt/UML%20Sequence.txt ):**


![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/ERD%20Class.png)

### 6. Описание алгоритма [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Sequence) [✋](https://github.com/stankin/design-part-2/wiki/LR-6)

* **Описываемые процессы и потоки данных:** A13

* **Диаграмма [UML Sequence](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/txt/UML%20Sequence.txt):**

![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/UML%20Sequence.png)

### 7. Описание состава [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Component) [✋](https://github.com/stankin/design-part-2/wiki/LR-7)

* **Описываемый объект:** Структура программных средств системы

* **Диаграмма [UML Component](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/txt/UML%20Component.txt):**


![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/UML%20Component.png)

### 8. Демонстрация реализации (личная страница)

Личная страница на [GitHub](https://imoldobaew.github.io/moldobaew-page/#!/topics)
### 9. Подготовка к интерпретации построенных моделей

**9.1 Используемые паттерны проектирования и разработки [✋](https://github.com/stankin/design-part-2/wiki/sem2):**

* **Процессная модель для сравнения:** Повысить эффективность планирования музейной выставки.


Решение задачи при помощи методологиии PDCA:
1. Этап Plan (Планирование):

 **Выявленные проблемы:** Тратиться много ресурсов на создание музейной выставки

 **Требования:** Повысить эффективность планирования музейной выставки без увеличения трудозатрат

 **Ожидаемый результат:** Повышение эффективности планирования музейной экспозиции 
 
 **Ресурсы, необходимые для достижения ожидаемого результата:** ПК, Прикладное ПО.

 **Процессы (запланированные действия):**

 * Создание 3D-моделей.
 * Создание необходимых скриптов.
 * Разработка системы.
 * Интеграция рабочей системы.

2. Этап Do(Выполнение):
Разработчки и 3D-художники выполняют поставленные задачи

3. Этап Check (Проверка): По итогу разработчики производят апробацию, и в случае успеха, произвести внедрение
4. Act (Улучшение): 
При успешной работе системы (сокращение временных затрат на проектирование), он внедряется в учреждение, с возможностью доработки или расширения функционала в дальнейшем

Доработка рабочей системы на основе ее оценки. Исправление замечайни\недочетов


**9.2 Используемые паттерны выявления проблем [✋](https://github.com/stankin/design-part-2/wiki/sem3):**
* Муда: Неэффективное использование времени, потери из-за ненужных транспортировок экспонатов
* Мура: Неравномерность распределения нагрузок и ресурсов при создании музейной экспозиции
* Мури: Переутомление куратора выставки

**9.3 Возможные антипаттерны [✋](https://github.com/stankin/design-part-2/wiki/sem4):**

| Категория  | Антипаттерн (риск) | Действие по избежанию |
|---|---|---|
| Разработка | Таинственный код: подразумевает использование аббревиатур вместо мнемоичных имён. Приводит к нечитаемости кода.| Избегается путем документировании и введением регламентов на разработку |
| Архитектура | Квадратное колесо: создание плохого решения, когда существует хорошее известное решение | Проанализировать более лучшие реализации |
| Организация |Единственный знающий человек: когда жизненно важными для проекта сведениями или навыками обладает только один человек в команде | Найм персонала дополнительных специалистов |
| Среда | Чрезмерное усложнение | Не усложнять проект тогда, когда этого не требуется, придерживаться принципа "проще - лучше". |

### 10. Интерпретация построенных моделей [✋](https://github.com/stankin/design-part-2/wiki/cp-guide)

**10.1 Определение числовых показателей для поставленной цели моделирования:**

Определение процессов требующих повышения качества

![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/Процессы.png)

Способ получения: извлечение из диаграмм IDEF0 и DFD.

**10.2 Определение числовых показателей и расчет экономического эффекта от проекта автоматизации: [✋](https://github.com/stankin/design-part-2/wiki/interpret_process):**
Допустим для создания выставки потребуется 100 экспонатов. При создании музейной экспозиции примерно 20% процентов принимаемых решений являются ошибочными, что в последстии приводит к их исправлению и лишней трате ресурсов.
Нужно уменьшит процент ошибочных или нежелательных решений. Для достижения поставленной цели предлагается внедрить данную систему

**10.3 Определение числовых показателей и расчет затрат на реализацию проекта автоматизации:**
Учреждение проводит в  среднем 6 выставок в год. Предположим, что на транспортировку и установку одного экспоната на витрину уходить 3 часа.

В результате принятия ошибочных решений, неэффективно используется 20*3 = 60 ч/выставка = 360ч/год. 

Если использовать данную систему, то процент ошибочных решений сократиться до 1%. Следовательнот неэффективное использование времени составит 1*3 = 6 ч\выставка = 36 ч/год.

Потенциальный эффект экономии времени составит 360ч - 36ч = 324ч/год.

**10.4 Определение числовых показателей и расчет трудозатрат на разработку программных средств:**

Расчет сложности разработки методом FPA IFPUG:

![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/FPA_IFPUG.png)

Расчет трудозатрат на разработку «с нуля» методом COCOMO II:

![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/COCOMO%20II.png)

**ВЫВОДЫ**

Исходя из расчётов трудозатрат, полученных методом COCOMO II делаем вывод, что система является экономически выгодной (с учетом того, что программисты имеют низкие навыки) и может быть реализована за 5 месяцев командой из 4-х человек.
