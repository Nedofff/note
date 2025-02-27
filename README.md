- HTML-разметка:<br/>
  Создайте базовую HTML-страницу с следующими элементами:
  - Поле ввода (например, `<input type="text" id="taskInput" placeholder="Введите задачу">`) для ввода текста новой задачи.
  - Кнопка (например, `<button id="addTaskBtn">Добавить задачу</button>`) для добавления задачи.
  - Контейнер (например, `<ul id="taskList"></ul>`) для отображения списка задач.
- JavaScript:<br/>Реализуйте логику с использованием следующих шагов:
  - Объявление переменных и создание массива:
    - Объявите переменную для хранения массива задач.
    - Каждая задача должна быть объектом со следующими свойствами:
      - `id`: уникальный идентификатор (например, число или строка);
      - `title`: текст задачи;
      - `completed`: логическое значение (по умолчанию `false`).
  - Функция `addTask`:<br/> Создайте функцию, которая:
    - Считывает значение из поля ввода.
    - Использует условие для проверки, что строка не пуста.
    - Создаёт объект задачи и добавляет его в массив (используйте оператор `push`).
    - Выводит в консоль созданный объект задачи.
    - Вызывает функцию обновления отображения задач (например, `renderTasks`).
  - Функция `renderTasks`:<br/>Напишите функцию, которая:
    - Очищает контейнер списка задач.
    - С помощью цикла (например, `for` или `forEach`) проходит по массиву задач.
    - Для каждой задачи создаёт элемент (например, `<li>`) с текстом задачи и кнопкой «Удалить».
    - Добавляет обработчик события (клик) для кнопки «Удалить», который:
      - Использует методы массива (например, `filter`) для удаления соответствующего объекта.
      - Обновляет отображение списка, вызывая `renderTasks` повторно.
    - При клике на сам элемент задачи можно также реализовать переключение статуса выполнения (функция `toggleTask`).
  - Функция `toggleTask`:<br/>Дополнительно создайте функцию, которая при клике (или при нажатии на чекбокс, если добавите его) меняет свойство `completed` у задачи:
    - Используйте условный оператор для проверки текущего значения.
    - Измените стиль отображения задачи (например, зачеркивание текста) в зависимости от статуса.
    - Выведите обновлённую информацию о задаче в консоль.
   
- Результат:
  - Пользователь сможет вводить текст задачи и добавлять её в список.
  - Каждая задача будет отображаться в виде элемента списка с кнопкой удаления.
  - При взаимодействии (добавление, удаление, изменение статуса) соответствующая информация будет выводиться в консоль.
