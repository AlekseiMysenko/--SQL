# Примеры простых запросов SQL

#### 1. Задача: Вывести имена, фамилии и даты рождения всех пользователей, создавших аккаунт в 2017 году

#### Запрос: select first_name, last_name, birth_date  
from account where year (account_creation_date)='2017';

| first_name | last_name | birth_date |
|------------|-----------|------------|
|  Vanessa   |  Karma    | 1992-10-29 |
|  Karen     | Movsesyan | 1995-01-20 |

#### Скрин из DBeaver 22.1.2 
![](https://github.com/AlekseiMysenko/--SQL/blob/main/Вывести%20имена%2C%20фамилии%20и%20даты%20рождения%20всех%20пользователей%2C%20создавших%20аккаунт%20в%202017%20году.jpg)
