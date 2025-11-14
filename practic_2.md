### Задачи с циклами

1. **Вывод чисел от 1 до 10.**  
    Напиши программу, которая выводит все числа от 1 до 10 в консоль.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ZoV</title>
</head>
<body>
    <script>
      function print(text){
        document.body.innerHTML += text + "<br>"
      }
      for (let num = 1; num <= 10; num ++){
        print(num)
      }
    </script>
</body>
</html>
```
    
2. **Сумма чисел от 1 до N.**  
    Напиши функцию, которая принимает число N и возвращает сумму всех чисел от 1 до N.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}
			
			function soomma(n) {
				let result = 0;
				for (let i = 1; i <= n; i++) {
					result += i;
				}
				return result;
			}
			
			function handleClick() {
				let inputValue = input.value;
				if (!inputValue) {
					print("Введите значение");
				} else {
					print(soomma(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>
```
    
3. **Вывод четных чисел от 1 до 20.**  
    Напиши цикл, который выводит все четные числа от 1 до 20.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			function print(text) {
				output.innerHTML = text;
			}
			function isEven(num) {
				return num % 2 == 0;
			}

			function twentyEvenNumbers() {
				let result = [];
				for (let i = 0; i < 20; i++) {
					if (isEven(i)) {
						result.push(i);
					}
				}
				return result;
			}
			function handleClick() {
				print(twentyEvenNumbers());
			}
		</script>
	</body>
</html>

```

3. **Вывод нечетных чисел от 1 до 20.**  
    Напиши цикл, который выводит все нечетные числа от 1 до 20.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			function print(text) {
				output.innerHTML = text;
			}
			function isOdd(num) {
				return num % 2 != 0;
			}

			function twentyOddNumbers() {
				let result = [];
				for (let i = 0; i < 20; i++) {
					if (isOdd(i)) {
						result.push(i);
					}
				}
				return result;
			}
			function handleClick() {
				print(twentyOddNumbers());
			}
		</script>
	</body>
</html>
```

3. **Таблица умножения.**  
    Напиши функцию, которая выводит в консоль таблицу умножения для введенного числа N от 1 до 10.

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}
			function multyply(a, b) {
				return `${a} * ${b} = ${a * b}`;
			}

			function multyply10(num) {
				let result = [];
				for (let i = 1; i <= 10; i++) {
					result.push(multyply(i, num) + "<br>");
				}
				return result;
			}
			
			function handleClick() {
				let inputValue = input.value;
				if (!inputValue) {
					print("Введите значение");
				} else {
					print(multyply10(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>

```
    
4. **Факториал числа.**  
    Напиши функцию, которая принимает число N и возвращает его факториал (N!).
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function fac(num) {
				let result = 1;
				for (let i = 1; i <= num; i++) {
					result *= i;
				}
				return result;
			}
			function handleClick() {
				let inputValue = input.value;
				if (!inputValue) {
					print("Введите значение");
				} else {
					print(fac(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>
```

4. **Числа от 1 до N, кратные 3 или 5.**  
    Напиши цикл, который выводит все числа от 1 до N, которые кратны 3 или 5.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function isDevidable(a, b) {
				return a % b == 0;
			}

			function isDevidableBy3And5(num) {
				let result = [];
				for (let i = 1; i <= num; i++) {
					if (isDevidable(i, 3) && isDevidable(i, 5)) {
						result.push(i);
					}
				}
				return result;
			}
			function handleClick() {
				let inputValue = input.value;
				if (!inputValue) {
					print("Введите значение");
				} else {
					print(isDevidableBy3And5(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>
```

4. **Вывод чисел по убыванию.**  
    Напиши программу, которая выводит все числа от 20 до 1 по убыванию.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function countDown() {
				let result = [];
				for (let i = 20; i >= 1; i--) {
					result.push(i);
				}
				return result;
			}
			function handleClick() {
				print(countDown());
			}
		</script>
	</body>
</html>
```

5. **Печать звездочек в строке.**  
    Напиши программу, которая печатает строку из 10 звездочек (*******) с помощью цикла на HTML страницу
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function getStarRow() {
				let result = "";
				for (let i = 0; i < 10; i++) {
					result += "*";
				}
				return result;
			}
			function handleClick() {
				print(getStarRow());
			}
		</script>
	</body>
</html>
```
    
6. **Печать прямоугольника**  
    Напиши функцию, которая принимает 2 числа M и N, она должна выводить прямоугольник из символа `#` со сторонами M и N
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="a" />
		<input type="number" id="b" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input1 = document.getElementById("a");
			let input2 = document.getElementById("b");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function getHashRow(len) {
				let result = "";
				for (let i = 0; i < len; i++) {
					result += "#";
				}
				return result;
			}

			function printRect(w, h) {
				output.innerHTML = "";
				for (let i = 0; i < h; i++) {
					output.innerHTML += getHashRow(w) + "<br>";
				}
			}

			function handleClick() {
				let width = input1.value;
				let height = input2.value;

				if (!width && !height) {
					print("Введите значения");
				} else {
					printRect(width, height);
				}
			}
		</script>
	</body>
</html>
```

6. **Поиск делителей числа.**  
    Напиши программу, которая находит все делители числа N и выводит их.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function isDevidable(a, b) {
				return a % b == 0;
			}

			function allDeviders(num) {
				let result = [];
				for (let i = 1; i <= num; i++) {
					if (isDevidable(num, i)) {
						result.push(i);
					}
				}
				return result;
			}
			function handleClick() {
				let inputValue = input.value;
				if (!inputValue) {
					print("Введите значение");
				} else {
					print(allDeviders(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>
```

6. **Сумма чисел в массиве.**  
    Напиши функцию, которая через prompt() спрашиает у пользоателя числа и считает их сумму. Ввод чисел от пользователя считается прекращенным, когда он введет 0.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");
			let sum = 0;

			function print(text) {
				output.innerHTML = text;
			}

			function addToSum(num) {
				return (sum += num);
			}
			function handleClick() {
				let inputValue = input.value;
				if (!inputValue) {
					print("Введите значение");
				} else {
					print(addToSum(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>

```
### Задачи с условиями
    
13. **Определение времени суток.**  
    Напиши программу, которая по числу (от 0 до 23) выводит, какое сейчас время суток: утро, день, вечер или ночь.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" min="0" max="24" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function nameOfTime(hours) {
				if (hours < 0 || hours > 24) {
					return "Ошибка";
				} else if (hours < 4) {
					return "Ночь";
				} else if (hours < 12) {
					return "Утро";
				} else if (hours < 17) {
					return "День";
				} else {
					return "Вечер";
				}
			}
			
			function handleClick() {
				let inputValue = input.value;
				if (!inputValue) {
					print("Ведите значение");
				} else {
					print(nameOfTime(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>
```

13. **Поиск максимального числа.**  
    Напиши функцию, которая находит большее из двух чисел.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="a" />
		<input type="number" id="b" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input1 = document.getElementById("a");
			let input2 = document.getElementById("b");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function findMax(a, b) {
				if (a < b) {
					return b;
				} else {
					return a;
				}
			}
			function handleClick() {
				let a = input1.value;
				let b = input2.value;
				if (!a || !b) {
					print("Ведите значение");
				} else {
					print(findMax(Number(a), Number(b)));
				}
			}
		</script>
	</body>
</html>

```

14. **Проверка, делится ли.**  
    Напиши функцию, которая получает числа M и N. Если M делится нацело на N - функция вернет true, если нет - вернет false
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="a" />
		<input type="number" id="b" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input1 = document.getElementById("a");
			let input2 = document.getElementById("b");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function isDevidable(a, b) {
				return a % b == 0;
			}

			function handleClick() {
				let a = input1.value;
				let b = input2.value;
				if (!a || !b) {
					print("Ведите значение");
				} else {
					print(isDevidable(Number(a), Number(b)));
				}
			}
		</script>
	</body>
</html>
```

14. **Треугольник с прямым углом.**  
    Напиши функцию, которая принимает в себя N и выводит прямоугольный треугольник с звездочек высотой N, например:
    ```
    // получено число 4
    *
    **
    ***
    ****
    ```

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />

		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function getStarRow(len) {
				let result = "";
				for (let i = 0; i < len; i++) {
					result += "*";
				}
				return result;
			}

			function printTriangle(h) {
				output.innerHTML = "";
				for (let i = 0; i < h; i++) {
					output.innerHTML += getStarRow(i) + "<br>";
				}
			}

			function handleClick() {
				let height = input.value;

				if (!height) {
					print("Введите значения");
				} else {
					printTriangle(height);
				}
			}
		</script>
	</body>
</html>
```

14. **Проверка возраста.**  
    Напиши программу, которая проверяет, является ли возраст человека меньше 18 лет (выводит соответствующее сообщение).
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" min="0" />

		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function isAdult(age) {
				return age >= 18;
			}

			function handleClick() {
				let age = input.value;

				if (!age || age < 0) {
					print("ошибка");
				} else {
					if (isAdult(age)) {
						print("Большой");
					} else {
						print("Не большой");
					}
				}
			}
		</script>
	</body>
</html>

```

15. **Определение дня недели.**  
    Напиши функцию, которая получает число и выводит название дня недели (например, 1 — Понедельник, 2 — Вторник и т. д.).
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" min="1" max="7" />

		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function dayOfTheWeek(dayNumber) {
				switch (dayNumber) {
					case 1:
						return "Понедельник";
						break;
					case 2:
						return "Вторник";
						break;
					case 3:
						return "Среда";
						break;
					case 4:
						return "Четверг";
						break;
					case 5:
						return "Пятница";
						break;
					case 6:
						return "Суббота";
						break;
					case 7:
						return "Воскресенье";
						break;
					default:
						return "Ошибка";
				}
			}

			function handleClick() {
				let dayNumber = input.value;

				if (!dayNumber) {
					print("Введите значения");
				} else {
					print(dayOfTheWeek(Number(dayNumber)));
				}
			}
		</script>
	</body>
</html>

```
15. **Оценка по баллам.**  
    Напиши программу, которая по числу баллов выводит оценку: 0–50 — "Не сдал", 51–75 — "Удовлетворительно", 76–90 — "Хорошо", 91–100 — "Отлично".
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" min="1" max="100" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>

		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function gradeName(grade) {
				if (grade < 0 || grade > 100) {
					return "Ошибка";
				} else if (grade <= 50) {
					return "Не сдал";
				} else if (grade <= 75) {
					return "Удовлетворительно";
				} else if (grade <= 90) {
					return "Хорошо";
				} else {
					return "Атлишна";
				}
			}

			function handleClick() {
				let grade = input.value;

				if (!grade) {
					print("Введите значения");
				} else {
					print(gradeName(Number(grade)));
				}
			}
		</script>
	</body>
</html>
```

15. **Поиск наибольшего числа среди трех.**  
    Напиши программу, которая находит наибольшее число среди трех.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="a" />
		<input type="number" id="b" />
		<input type="number" id="c" />
		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>

		<script>
			let inputA = document.getElementById("a");
			let inputB = document.getElementById("b");
			let inputC = document.getElementById("c");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function biggest(num1, num2, num3) {
				if (num1 >= num2 && num1 >= num3) {
					return num1;
				} else if (num2 >= num1 && num2 >= num3) {
					return num2;
				} else if (num3 >= num1 && num3 >= num2) {
					return num3;
				} else {
					return "Ошибка";
				}
			}

			function handleClick() {
				let a = inputA.value;
				let b = inputB.value;
				let c = inputC.value;

				if (!a || !b || !c) {
					print("Введите значения");
				} else {
					a = Number(a);
					b = Number(b);
					c = Number(c);
					print(biggest(a, b, c));
				}
			}
		</script>
	</body>
</html>
```

15. **Проверка на простое число.**  
    Напиши программу, которая проверяет, является ли число простым.
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />

		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function isDevidable(a, b) {
				return a % b == 0;
			}

			function isSimple(num) {
				for (let i = 2; i < num; i++) {
					if (isDevidable(num, i)) {
						return false;
					}
				}
				return true;
			}

			function handleClick() {
				let inputValue = input.value;

				if (!inputValue) {
					print("Ведите значение");
				} else {
					print(isSimple(Number(inputValue)));
				}
			}
		</script>
	</body>
</html>
```

15. **Определение сезона по месяцу.**  
    Напиши программу, которая по номеру месяца (от 1 до 12) выводит сезон года (зима, весна, лето, осень).
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" min="1" max="12" />

		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function seasonName(monthNumber) {
				switch (monthNumber) {
					case 1:
					case 2:
					case 12:
						return "Зима";
						break;
					case 3:
					case 4:
					case 5:
						return "Весна";
						break;
					case 6:
					case 7:
					case 8:
						return "Лето";
						break;
					case 9:
					case 10:
					case 11:
						return "Осень";
					default:
						return "Ошибка";
				}
			}

			function handleClick() {
				let monthNumber = input.value;

				if (!monthNumber) {
					print("Введите значения");
				} else {
					print(seasonName(Number(monthNumber)));
				}
			}
		</script>
	</body>
</html>

```
# Дополнительно
24. Копейка рубль бережет
	 Напиши функцию, которая принимает в себя количество копеек N и выводит количество рублей и оставшихся копеек
```js
console.log(copeyki(123))
// 1 руб и 23 коп
```

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>ZoV</title>
	</head>
	<body>
		<input type="number" id="input" />

		<button onclick="handleClick()">abobaa</button>
		<div id="output"></div>
		<script>
			let input = document.getElementById("input");
			let output = document.getElementById("output");

			function print(text) {
				output.innerHTML = text;
			}

			function copeyki(money) {
				let rub = Math.floor(money / 100); // Округляем в меньшую сторону
				let cop = money % 100;
				return `${rub} руб и ${cop} коп`;
			}

			function handleClick() {
				let monthNumber = input.value;

				if (!monthNumber) {
					print("Введите значения");
				} else {
					print(copeyki(Number(monthNumber)));
				}
			}
		</script>
	</body>
</html>

```
