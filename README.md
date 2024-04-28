[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Z0eBgHwz)
# Патерн одинак (Singleton)

- Потрібно вивчити теоретичний матеріал та написати власноруч приклад коду для патерну будівельник.
- Закомітити даний приклад та зробити pull request.
- Згідно власного варіанту потрібно переписати існуючий проект та додати за потреби нові класи. Варіанти завдань отримати у викладача.
- В README файлі навести UML діаграму класів для коду згідно власного варіанту з короткими поясненнями.
- Закомітити код та зробити pull request.

## Варіант 7
7. Реалізувати Singleton для доступу до конфігураційних даних програми, забезпечуючи централізований доступ до налаштувань бази даних, портів та ключів API.

1. Program.cs: це точка входу програми. Він містить метод Main, який відображає меню для користувача за допомогою методу MainMenu.
Метод ViewConfigurationData викликається, коли користувач вибирає опцію для перегляду даних конфігурації.

2. ConfigurationManager: цей клас відповідає шаблону Singleton, щоб забезпечити існування лише одного екземпляра класу протягом усього життя програми.
Він містить приватний екземпляр класу ConfigurationData, який містить фактичні дані конфігурації. Властивість Instance надає доступ до єдиного екземпляра ConfigurationManager.
Метод GetConfigData повертає екземпляр ConfigurationData.

3. ConfigurationData: цей клас представляє властивості даних конфігурації, такі як рядок підключення до бази даних, порт і ключ API.
Це простий клас контейнера даних.

Клас Program.cs використовує клас ConfigurationManager для доступу до даних конфігурації. Клас ConfigurationManager містить екземпляр класу ConfigurationData, який містить фактичні дані конфігурації.
Шаблон Singleton, реалізований у класі ConfigurationManager, забезпечує існування лише одного екземпляра класу в усій програмі, забезпечуючи централізований доступ до даних конфігурації.
Цей дизайн дотримується принципу поділу інтересів, згідно з яким кожен клас має певну відповідальність. Клас Program.cs обробляє інтерфейс користувача, клас ConfigurationManager керує доступом до даних конфігурації,
а клас ConfigurationData зберігає властивості даних конфігурації.