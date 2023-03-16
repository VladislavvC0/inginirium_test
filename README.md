# inginirium_test
Репозиторий на гитхабе, что создан для чего-то там такого.

Например, снизу описан код на языке Python для подтверждения есть ли такой пользователь на гитхабе с таким же ником:

#Код
import requests

username = 'your_username'

response = requests.get(f'https://api.github.com/users/{username}')

if response.status_code == 200:
    user_data = response.json()
    print("Ник: {user_data['login']}")
else:
    print("Не удалось обнаружить что-либо связанное с ником {username}")
