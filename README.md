# Примеры простых запросов SQL

### 1. Задача: 

#### Вывести имена, фамилии и даты рождения всех пользователей, создавших аккаунт в 2017 году
#### - Использовал комманду SELECT

### Запрос: 

#### select first_name, last_name, birth_date  
from account where year (account_creation_date)='2017';

### Результат:

| first_name | last_name | birth_date |
|------------|-----------|------------|
|  Vanessa   |  Karma    | 1992-10-29 |
|  Karen     | Movsesyan | 1995-01-20 |

#### Скрин из DBeaver 22.1.2 
![](https://github.com/AlekseiMysenko/--SQL/blob/main/Вывести%20имена%2C%20фамилии%20и%20даты%20рождения%20всех%20пользователей%2C%20создавших%20аккаунт%20в%202017%20году.jpg)

### 2. Задача:

#### Добавить в базу запись об игре Red Dead Redemption (внести информацию о названии, дате выхода, компании-разработчике)
#### - Использовал команду INSERT

### Запрос: 

#### INSERT INTO game (Game_name, Release_date, Genre, Developer, Is_online, price)
VALUES ('Red Dead Redemption', '2010-02-02',  2, 12, 1, 0);

#### Скрин из DBeaver 22.1.2
![](https://github.com/AlekseiMysenko/--SQL/blob/main/Добавить%20в%20базу%20запись%20об%20игре%20Red%20Dead%20Redemption%20(внести%20информацию%20о%20названии%2C%20дате%20выхода%2C%20компании-разработчике).jpg)

### 3. Задача:

#### Добавить игре Red Dead Redemption цену в 2000
#### - Использовал команду UPDATE

### Запрос: 

#### update game set price = 2000 where Game_name = 'Red Dead Redemption';

#### Скрин из DBeaver 22.1.2
![](https://github.com/AlekseiMysenko/--SQL/blob/main/Добавить%20игре%20Red%20Dead%20Redemption%20цену%20в%202000.jpg)

### 4. Задача:

#### Выбрать онлайн-игры, созданные в USA и вышедших раньше 2011 года
#### - Объединение выборки с разных таблиц с использованием комманды JOIN

### Запрос: 

#### select Game_name, g.id
from game g 
join company c on g.Developer=c.id 
where year (g.Release_date) < '2011' and c.country = 'USA' and g.Is_online =1; 

#### Скрин из DBeaver 22.1.2
![](https://github.com/AlekseiMysenko/--SQL/blob/main/Вывести%20онлайн-игры%2C%20созданные%20в%20USA%20и%20вышедших%20раньше%202011%20г.jpg)

### 5. Задача:

#### Удалить игру Red Dead Redemption из базы
#### - Использовал команду DELETE

### Запрос: 

#### delete from game where Game_name = 'Red Dead Redemption';

#### Скрин из DBeaver 22.1.2
![](https://github.com/AlekseiMysenko/--SQL/blob/main/Удалить%20игру%20Red%20Dead%20Redemption%20из%20базы.jpg)
