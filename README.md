# Tele2_webAPI
## Задание
Написать приложение (API) с двумы GET запросами.
Дано:
По адресу http://testlodtask20172.azurewebsites.net/task можно получить строку, содержащую информацию о жителях города X. Строка содержит id, имя с фамилией и пол каждого жителя. А по адресу http://testlodtask20172.azurewebsites.net/task/{id} можно получить имя, фамилию, пол и возраст конкретного жителя, id которого можно взять из 1 запроса.
При запуске приложения сохранить список жителей и данные по ним в базу данных MsSQL.

### Описание первого метода API:

- Возвращать список жителей города X. Так же в методе должна быть возможность передавать опциональный параметр, по которому жители будут фильтроваться по полу (возвращать всех, только мужчин, или только женщин). Так же, в методе нужна пагинация (постраничный вывод). Добавить фильтрацию по возрасту (выводить жителей  с возрастом от x до y). Параметр также, опциональный, если его не передавать, то фильтр не учитывается.

### Описание второго метода API:
- Возвращать конкретного жителя по переданному id.

Покрыть реализвацию unit тестами.

## Реализация

### Список используемых библиотек:

- AutoMapper.Extensions.Microsoft.Dependencyinjection\3.2.0\
- Microsoft.EntityFrameworkCore\3.1.0\
- Microsoft.EntityFrameworkCore.SqlServer\3.1.0\
- Moq\4.16.1\
- xunit.core\2.4.1\
- linq

Для подключения своего MsSQL Server в appsettings.json измените "CityConnection" string. Затем в Консоли деспетчера пакетов введите Update-Database. 
Файлы миграций лежат в папке Migrations.
