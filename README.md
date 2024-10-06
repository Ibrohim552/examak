CRUD API для управления сотрудниками
Описание проекта
Данный проект представляет собой CRUD API для работы с таблицей Employees, реализованный с использованием .NET 8 и Entity Framework Core. API поддерживает основные операции создания, чтения, обновления и удаления сотрудников, а также предоставляет дополнительные функции для получения информации о сотрудниках.

Технологии
.NET 8 (ASP.NET Core Web API)
Entity Framework Core для работы с базой данных
Dapper для выборки данных
PostgreSQL для хранения данных
Асинхронное программирование
Dependency Injection (DI)
Middleware
API Conventions
Структура базы данных
Таблица Employees содержит следующие поля:

Поле	Тип	Описание
Id	UUID	Идентификатор сотрудника (Primary Key)
FirstName	VARCHAR(100)	Имя сотрудника
LastName	VARCHAR(100)	Фамилия сотрудника
Email	VARCHAR(255)	Электронная почта (уникальное)
Phone	VARCHAR(20)	Номер телефона (мин. 10 символов)
DateOfBirth	DATE	Дата рождения (должна быть раньше текущей даты)
HireDate	DATE	Дата найма на работу
Position	VARCHAR(100)	Должность сотрудника
Salary	DECIMAL(18, 2)	Зарплата сотрудника (неотрицательная)
DepartmentId	UUID	Идентификатор департамента
ManagerId	UUID	Идентификатор руководителя (может быть пустым)
IsActive	BOOLEAN	Статус активности (по умолчанию TRUE)
Address	VARCHAR(255)	Адрес проживания
City	VARCHAR(100)	Город проживания
Country	VARCHAR(100)	Страна проживания
CreatedAt	TIMESTAMP	Дата создания записи
UpdatedAt	TIMESTAMP	Дата последнего обновления записи
Функциональность API
CRUD-операции
Create: Создание нового сотрудника.
Read: Получение информации о сотрудниках.
Update: Обновление информации о сотруднике.
Delete: Удаление записи о сотруднике.
GET-запросы
Получение всех сотрудников: GET /api/employees
Получение сотрудника по Id: GET /api/employees/{id}
Получение сотрудников по статусу активности: GET /api/employees?isActive={isActive}
Получение сотрудников по департаменту: GET /api/employees/department/{departmentId}
Получение статистики по зарплатам: GET /api/employees/salary-statistics
Получение сотрудников, рожденных в определенный период: GET /api/employees/birthdays?startDate={startDate}&endDate={endDate}
Установка и запуск
Клонируйте репозиторий:

bash
Копировать код
git clone https://github.com/ваш_пользователь/ваш_репозиторий.git
Перейдите в директорию проекта:

bash
Копировать код
cd ваш_репозиторий
Установите необходимые зависимости:

bash
Копировать код
dotnet restore
Выполните миграции для настройки базы данных:

bash
Копировать код
dotnet ef database update
Запустите проект:

bash
Копировать код
dotnet run
Middleware
Проект включает пользовательское Middleware, которое обрабатывает определенные запросы и добавляет дополнительную функциональность.

Публикация
Финальная версия проекта опубликована на GitHub. Для получения дополнительной информации о проекте, посетите репозиторий.

Лицензия
Этот проект распространяется под лицензией MIT. Для получения дополнительной информации смотрите файл LICENSE.

Контакты
Если у вас есть вопросы или предложения, вы можете связаться со мной по электронной почте: atahonovibrohim952@gmail.com.



