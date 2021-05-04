## Курсовой проект по дисциплине "Проектирование информационных систем"

## ФИО, ИДБ-17-06

### 1. Определение требований к модели [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

**Тема ВКР:** Разработка системы визуализации трехмерной сцены музея промышленных достижений

**Объект исследований:** виртуальные музеи

**Предмет исследований:** системы трехмерного моделирования реалистичных сцен

**Процессы верхнего уровня:** [✋](https://github.com/stankin/design-part-2/wiki/sem1)
* **А1** Управление
* **А2** Формирование трехмерной сцены
* **А3** Визуализация

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

![A3](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/06_A3.png)


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

* A12 Автоматизация процесса А12

![A12](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/05_A12.png)

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

* **Диаграмма UML Sequence[https://github.com/imoldobaew/imoldobaew.github.io/blob/main/txt/UML%20Sequence.txt]:**

![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/UML%20Sequence.png)

### 7. Описание состава [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Component) [✋](https://github.com/stankin/design-part-2/wiki/LR-7)

* **Описываемый объект:** Структура программных средств системы

* **Диаграмма [UML Component](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/txt/UML%20Component.txt):**


![none](https://github.com/imoldobaew/imoldobaew.github.io/blob/main/UML%20Component.png)

### 8. Демонстрация реализации (личная страница)

<ссылка или скриншоты>

### 9. Подготовка к интерпретации построенных моделей

**9.1 Используемые паттерны проектирования и разработки [✋](https://github.com/stankin/design-part-2/wiki/sem2):**

* **Процессная модель для сравнения:**

* **Используемые в разработке паттерны и фреймворки:**

**9.2 Используемые паттерны выявления проблем [✋](https://github.com/stankin/design-part-2/wiki/sem3):**
* Муда: <муда>
* Мура: <мура>
* Мури: <мури>

**9.3 Возможные антипаттерны [✋](https://github.com/stankin/design-part-2/wiki/sem4):**

| Категория  | Антипаттерн (риск) | Действие по избежанию |
|---|---|---|
| Разработка | <антипаттерн> | <действие> |
| Архитектура | <антипаттерн> | <действие> |
| Организация | <антипаттерн> | <действие> |
| Среда | <антипаттерн> | <действие> |

### 10. Интерпретация построенных моделей [✋](https://github.com/stankin/design-part-2/wiki/cp-guide)

**10.1 Определение числовых показателей для поставленной цели моделирования:**

**10.2 Определение числовых показателей и расчет экономического эффекта от проекта автоматизации: [✋](https://github.com/stankin/design-part-2/wiki/interpret_process):**

**10.3 Определение числовых показателей и расчет затрат на реализацию проекта автоматизации:**

**ВЫВОДЫ**

