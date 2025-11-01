# Функции в JavaScript - подробное руководство

## Что такое функции и зачем они нужны?

**Функции** - это блоки кода, которые можно многократно использовать. Они помогают:
- Сократить повторяющийся код
- Упорядочить программу на логические части
- Упростить отладку и тестирование
- Повысить читаемость кода

## Создание и вызов функций

### Синтаксис объявления функции
```js
function имяФункции(параметр1, параметр2, ...) {
    // тело функции - код, который выполняется при вызове
    return результат; // необязательно
}
```

### Простой пример
```js
// Объявление функции
function greet() {
    console.log("Привет, мир!");
}

// Вызов функции
greet(); // "Привет, мир!"
greet(); // "Привет, мир!" - можно вызывать много раз
```

## Функции с параметрами

### Пример с одним параметром
```js
function sayHello(name) {
    console.log(`Привет, ${name}!`);
}

sayHello("Анна");    // "Привет, Анна!"
sayHello("Петр");    // "Привет, Петр!"
```

### Пример с несколькими параметрами
```js
function introduce(name, age, city) {
    console.log(`Меня зовут ${name}, мне ${age} лет, я из ${city}`);
}

introduce("Мария", 25, "Москвы"); 
// "Меня зовут Мария, мне 25 лет, я из Москвы"
```

## Возврат значений с помощью `return`

### Функция без return
```js
function showSum(a, b) {
    console.log(a + b);
}

let result1 = showSum(3, 4); 
// Выведет: 7
// Но result1 будет undefined, так как функция ничего не возвращает
console.log(result1); // undefined
```

### Функция с return
```js
function calculateSum(a, b) {
    return a + b;
}

let result2 = calculateSum(3, 4);
console.log(result2); // 7 - теперь результат сохранен в переменной

// Можно использовать результат в выражениях
let total = calculateSum(5, 2) * 2;
console.log(total); // 14
```

### Практический пример
```js
// Функция проверки совершеннолетия
function isAdult(age) {
    return age >= 18;
}

let userAge = 20;
if (isAdult(userAge)) {
    console.log("Доступ разрешен");
} else {
    console.log("Доступ запрещен");
}
```

## Разделение ответственности функций

### Плохой подход - функция делает слишком много
```js
function calculateAndDisplay(a, b) {
    let sum = a + b;
    console.log(`Сумма: ${sum}`);
    return sum; // смешиваем вывод и вычисления
}
```

### Хороший подход - каждая функция делает одну вещь
```js
function display(text) {
    console.log(text);
}

function add(a, b) {
    return a + b;
}

function subtract(a, b) {
    return a - b;
}

// Использование
let sum = add(10, 5);
display(`Сумма: ${sum}`); // "Сумма: 15"

let difference = subtract(10, 5);
display(`Разность: ${difference}`); // "Разность: 5"
```

## Практические задания

### Задание 1: Калькулятор площади
```js
// Напишите функцию calculateRectangleArea, которая принимает 
// ширину и высоту прямоугольника и возвращает его площадь

// Ваш код здесь:

// Проверка:
// console.log(calculateRectangleArea(5, 10)); // Должно вывести 50
// console.log(calculateRectangleArea(3, 7));  // Должно вывести 21
```

### Задание 2: Конвертер температур
```js
// Напишите функцию celsiusToFahrenheit, которая преобразует 
// температуру из Цельсия в Фаренгейт по формуле: F = C × 9/5 + 32

// Ваш код здесь:

// Проверка:
// console.log(celsiusToFahrenheit(0));    // Должно вывести 32
// console.log(celsiusToFahrenheit(100));  // Должно вывести 212
```

### Задание 3: Проверка четности
```js
// Напишите функцию isEven, которая принимает число и возвращает true, 
// если число четное, и false - если нечетное

// Ваш код здесь:

// Проверка:
// console.log(isEven(4)); // true
// console.log(isEven(7)); // false
```

## Решения заданий

```js
// Решение задания 1
function calculateRectangleArea(width, height) {
    return width * height;
}

// Решение задания 2
function celsiusToFahrenheit(celsius) {
    return celsius * 9/5 + 32;
}

// Решение задания 3
function isEven(number) {
    return number % 2 === 0;
}
```

## Полезные советы

1. **Давайте функциям понятные имена** - имя должно отражать что делает функция
2. **Одна функция - одна задача** - функция должна делать только одну вещь
3. **Используйте параметры** для передачи данных в функцию
4. **Используйте return** для возврата результатов
5. **Избегайте побочных эффектов** - функция не должна изменять внешние переменные

## Дополнительные примеры

```js
// Функция нахождения максимального числа
function findMax(a, b, c) {
    return Math.max(a, b, c);
}

// Функция форматирования строки
function createEmail(username, domain) {
    return `${username}@${domain}.com`;
}

// Использование
let maxNumber = findMax(15, 8, 23);
console.log(`Максимальное число: ${maxNumber}`);

let email = createEmail("ivan", "example");
console.log(email); // "ivan@example.com"
```

Функции действительно являются строительными блоками JavaScript - освоив их, вы сможете создавать сложные и хорошо организованные программы!
