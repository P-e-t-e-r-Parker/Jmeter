#### :heavy_check_mark: 1) http://5.75.203.123/user_info
req. (RAW JSON)
POST
age: int
salary: int
name: str
auth_token


resp.
{'start_qa_salary':salary,
 'qa_salary_after_6_months': salary * 2,
 'qa_salary_after_12_months': salary * 2.9,
 'person': {'u_name':[user_name, salary, age],
                                'u_age':age,
                                'u_salary_1.5_year': salary * 4}
                                }

#### Действия:
Достать из Respose значение из поля 'qa_salary_after_6_months' и передать в поле salary запроса http://162.55.220.72:5005/new_data

===================

#### :heavy_check_mark: 2) http://5.75.203.123/new_data
req.
POST
age: int
salary: int
name: str
auth_token

Resp.
{'name':name,
  'age': int(age),
  'salary': [salary, str(salary*2), str(salary*3)]}

#### Действия:
Достать из Respose значение из поля 'name' и передать в поле name запроса http://162.55.220.72:5005/test_pet_info

===================

#### :heavy_check_mark: 3) http://5.75.203.123/test_pet_info
req.
POST
age: int
weight: int
name: str
auth_token


Resp.
{'name': name,
 'age': age,
 'daily_food':weight * 0.012,
 'daily_sleep': weight * 2.5}


#### Тесты:
Достать из Respose значение из поля age и передать в поле age запроса http://162.55.220.72:5005/get_test_user


Задание ***
0) Изучать как работают Response Assertion.                       
1) Сделать Assertion на провекрку статус код 200                  
2) Сделать Assertion на провекрку 'daily_food':weight * 0.012     

#### :heavy_check_mark: 4) http://5.75.203.123/get_test_user
req.
POST
age: int
salary: int
name: str
auth_token

Resp.
{'name': name,
 'age':age,
 'salary': salary,
 'family':{'children':[['Alex', 24],['Kate', 12]],
 'u_salary_1.5_year': salary * 4}
  }

### Задание ***
#### :heavy_check_mark:Изучать как работают Response Assertion.        
#### :heavy_check_mark: 1) Сделать Assertion на провекрку статус код 200   
2) Сделать Assertion на провекрку 'salary': salary 

### <center>[Ссылка: настройки Jmeter](https://github.com/P-e-t-e-r-Parker/Jmeter/blob/main/HomeWork_2/Settings.jmx)</center>
## 📫 Связаться со мной
[![Telegram](https://img.shields.io/static/v1?style=for-the-badge&logo=telegram&message=telegram&label=&color=4165a3&labelColor=000000)](https://t.me/petrshelkunov)
[![mail](https://img.shields.io/static/v1?style=for-the-badge&logo=gmail&message=mail&label=&color=e8203b&labelColor=000000)](mailto:petia.shelkunov@yandex.ru)
[![LinkedIn](https://img.shields.io/static/v1?style=for-the-badge&logo=linkedin&message=LinkedIn&label=&color=3947c4&labelColor=000000)](https://linkedin.com/in/petr-shhelkunov)
