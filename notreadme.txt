Кожен модуль може бути викликаний декілька раз, для різних елементів!!!
В такому випадку краще селектори і дата атрибути передавати в параметри модулів, щоб уникати повторення коду
Взяти наприклад slider.js. В йому жостко забиті селектори класів. Якщо виникне потреба створити ще 1 слайдер, відбудеться дублікація коду

() => openModal(modalSelector) - дуже крутий прийом в обробниках подій, якій дозволяє уникнути порушення принципу використання
колбек функцій в обробнику подій. 

modalTrigger.forEach(btn => {
        btn.addEventListener('click', openModal(modalSelector))
    });

Якщо openModal буде викликатись в обробнику подій, то одразу при вході на сторінку, буде висвічуватись модальне вікно
Обгорнувши його в колбек функцію, ми уникаєм цього. При кліку на кнопку, буде викликатись колбек функція, яка викликатиме модальне вікно

Трансплітер - утиліта чи розширення, яке дозволяє перевести сучасний код програми, в старий, для підтримки старих версій браузера
Babel - трансплітер. Є декілька варіантів використання. Проганяти кожен файл окремо через його, або підключити до зборки проекту через нпм пакети

*********BABEL*********
npm i --save-dev @babel/core @babel/cli @babel/present-env
@babel/core - ядро бейбла, його одиниці які будуть проганяти код
@babel/cli - утиліта яка дозволяє запускати babel з командної строки
@babel/preset-env - один з пресетів бейбла - env. ENV підходить для більшості проектів
@babel/polyfill - один з пакетів бейбла. Використовується для продакшену --save
babel-loader - дозволяє працювати бейблу разом з вебпак

corejs - ще одна бібліотека для поліфілів. Включає в себе всі поліфіли, але також дозволяє визначити і включити в роботу лише ті поліфіли
які справді необхідно

corejs теж має свої баги і деякі поліфіли можуть пролітати і не спрацьовувати. В такому випадку їх треба встановлювати окремо

Гарним тоном є те, що всі файли підключаються через 1 скриптовий файл джс, а не окремо на сторінках

Angular:
- node.js - необхідно встановити і вміти працювати з нпм
- Typescript - Розширена версія js. Являється мовою на якій створений сам Angular
- Webpack - ця технологія повина досконало бути вивченою для розуміння як виконується зборка під капотом
- MVC pattern - Model View Controller - Розділяється на 3 складових частини: візуальну, контролюючу та взаємодіючу
- Angular

React:
- JSX
- Babel
- Webpack
- React

Vue:
- Webpack
- Vue