# Charles

__Ex_0:__ Сфокусироваться на ниже перечисленных запросах
```
Protocol: http
IP: 162.55.220.72
Port: 5005
```

__Ex_1:__ 
```
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int

response: 
[
    “Str”,
    “Str”
]
```
__Task:__
* Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)
* Подменить url в __Charles__ чтобы в запросе ушло имя которые вы вписали в __Postman__, а вернулось то, которое вы подставили в Charles.

![break_1s](https://user-images.githubusercontent.com/104720406/178478496-85e0f5bb-06ea-4779-b8f9-f8fcb3cea73b.png)

__or__

![Ex_rew_1](https://user-images.githubusercontent.com/104720406/178479021-e6539fc1-244f-4293-b8f7-b105942d8594.png)


_____

__Ex_2:__
```
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
```
__Task:__
* Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)
* Подменить body в __Charles__ так чтобы в запросе ушла salary которую вы вписали в __Postman__, а в u_salary_1_5_year цифра вернулась меньше оригинальной из запроса.

![Ex_2s](https://user-images.githubusercontent.com/104720406/178479282-b38d83c3-90dc-45dd-a31b-0fa7432b40ad.png)


_____


__Ex_3:__
```
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
```
__Task:__
* Сделать и в __Rewrite__, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)
* Подменить параметры запроса в __Charles__ так, чтобы в Postman пришел ответ где другое name, daily_food > weight из запроса, а daily_sleep < weight из запроса.

![ex_3s](https://user-images.githubusercontent.com/104720406/178479515-59bfb420-94c3-4fc4-bed4-98ddd3d6641a.png)


_____


__Ex_4:__
```
Method: GET
EndPoint: /object_info_3
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
```
__Task:__
Сделать и в __Rewrite__, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)
- Сделать через __Charles__ так, чтобы сервер вернул __500 код.__
- Сделать через __Charles__ так, чтобы сервер вернул __405 код.__

![ex_4 1png](https://user-images.githubusercontent.com/104720406/178479840-095cbbe8-6efd-4127-920c-e9e399498b92.png)

![ex_4 405png](https://user-images.githubusercontent.com/104720406/178479869-d88aed06-56ed-4d3d-8c11-1ed4b64644bd.png)


__Ex_5:__
```
Method: GET
EndPoint: /object_info_4
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}

```
__Task:__
Сделать и в __Rewrite__, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)
* Сделать через __Charles__ так, чтобы сервер вернул 405 ошибку.
* Подменить salary в request
* Подменить (salary * 2) в response

![ex_5](https://user-images.githubusercontent.com/104720406/178480255-17bb1107-b209-47b6-bcff-56f441ef2e50.png)


__Ex_6:__
```
Method: POST
EndPoint: /user_info_2
request form data: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }

```
__Task:__
Сделать и в __Rewrite__, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)
* Сделать через __Charles__ так, чтобы в Postman вернулся ответ, в котором __qa_salary_after_1.5_year__ переименовано в __qa_salary_after_1.5_month__
* Сделать так чтобы __qa_salary_after_3.5_years__ было меньше __qa_salary_after_12_months в response__
 
 ![ex6_1s](https://user-images.githubusercontent.com/104720406/178480869-80c16b46-7efb-4251-9529-96d8577a5a97.png)
