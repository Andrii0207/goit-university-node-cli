Тема 2. Створення консольних додатків

Крок 1
твори репозиторій з назвою goit-node-cli, склонуй та ініціалізуй в ньому проєкт за допомогою команди npm init. Встанови як залежність проєкту пакет commander
В корінь проєкту помісти файли з папки src

Крок 2
У файл contacts.js зроби імпорт модулів fs (у версії, яка працює з промісами - fs/promises) і path для роботи з файловою системою.

Створи змінну contactsPath і запиши в неї шлях до файлу contacts.json. Для складання шляху використовуй методи модуля path.

Додай асинхронні функції для роботи з колекцією контактів. У функціях використовуй модуль fs та його методи readFile() і writeFile(). Відповідні функції мають повертати необхідні дані за допомогою оператора return. Вивід в консоль в написаних функціях здійснюватись не повинен.

Зроби експорт створених функцій. [скрин за посиланням](image.png)

Крок 3
Зроби імпорт функцій з файла contacts.js в файл index.js.
Далі використовуй готову функцію invokeAction(), яка отримує тип виконуваної дії і необхідні аргументи. Функція має викликати відповідний метод з файлу contacts.js, передаючи йому необхідні аргументи. Результат роботи викликаної функції слід вивести в консоль.

Крок 4
Запусти команди в терміналі і переконайся, що код працює належним чином.

# Отримуємо і виводимо весь список контактів у вигляді таблиці (console.table)

node index.js -a list

# Отримуємо контакт по id і виводимо у консоль об'єкт контакту або null, якщо контакту з таким id не існує.

node index.js -a get -i 05olLMgyVQdWRwgKfg5J6

# Додаємо контакт та виводимо в консоль об'єкт новоствореного контакту

node index.js -a add -n Mango -e mango@gmail.com -p 322-22-22

# Видаляємо контакт та виводимо в консоль об'єкт видаленого контакту або null, якщо контакту з таким id не існує.

node index.js -a remove -i qdggE76Jtbfd9eWJHrssH
