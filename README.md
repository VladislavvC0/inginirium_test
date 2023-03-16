# inginirium_test
Репозиторий на гитхабе, что создан для чего-то там такого.

Например, снизу описан код на языке Python для подтверждения есть ли такой пользователь на гитхабе с таким же ником:

import requests

# Введите ваше имя пользователя GitHub здесь
username = 'your_username'

# Создаем запрос к API GitHub для получения данных о пользователе
response = requests.get(f'https://api.github.com/users/{username}')

# Если запрос прошел успешно, выводим ник пользователя
if response.status_code == 200:
    user_data = response.json()
    print("Ник: {user_data['login']}")
else:
    print("Не удалось обнаружить что-либо связанное с ником {username}")
