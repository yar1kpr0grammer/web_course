# Анимации
## Анимации по ключевым кадрам

- `animation-name` указывает название анимации
- `animation-duration` указывает продолжительность анимации

При использовании анимации по ключевым кадрам нам нужно указать:
- Начальное состояние
- Промежуточные состояния (необязательно)
- Конечное состояние

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Document</title>
	</head>
	<body>
		<div class="colorful"></div>
		<style>
			.colorful {
				border: 1px solid black;
				width: 150px;
				height: 150px;
				animation-name: change-color;
				animation-duration: 4s;
			}
			@keyframes change-color {
				from {
					background-color: red;
				}

				to {
					background-color: purple;
				}
			}
		</style>
	</body>
</html>

```

>Как только страница прогрузится элементу установится красный цвет, который перейдет в синий за 4 секунды. Затем элемент вернет изначальные свойства

Если мы хотим использовать промежуточные состояния - нужно сказывать состояния в процентах:

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Document</title>
	</head>
	<body>
		<div class="colorful"></div>
		<style>
			.colorful {
				border: 1px solid black;
				width: 150px;
				height: 150px;
				animation-name: change-color;
				animation-duration: 4s;
			}
			@keyframes change-color {
				0% {
					background-color: red;
				}
				20% {
					background-color: orange;
				}
				40% {
					background-color: green;
				}
				60% {
					background-color: aqua;
				}
				80% {
					background-color: blue;
				}
				100% {
					background-color: purple;
				}
			}
		</style>
	</body>
</html>
```

- `animation-delay` указывает задержку перед началом анимации
- `animation-iteration-count` указывает сколько будет повторяться анимация

Измените код CSS класса следующим образом:

```css
.colorful {
	border: 1px solid black;
	width: 150px;
	height: 150px;
	animation-name: change-color;
	animation-duration: 4s;
	animation-delay: 3s; /* <-- */
	animation-iteration-count: 5; /* <-- */
}
```

> Теперь перед началом анимации пройдет 3 секунды и она повторится 5 раз

Если поставить в количество повторений `infinite` - анимация будет повторяться бесконечно

```css
.colorful {
	border: 1px solid black;
	width: 150px;
	height: 150px;
	animation-name: change-color;
	animation-duration: 4s;
	animation-delay: 3s;
	animation-iteration-count: infinite; /* <-- */
}
```

- `animation-direction` указывает направление анимации
	- `normal` - изначальное значение. Когда анимация закончилась - начнется с начала
	- `reverse` - Анимация играется задом наперед
	- `alternate` - Когда анимация кончилась (при следующем повторении) она начнется с конца
	- `alternate-reverse` - alternate, но задом наперед

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Animation Directions</title>
		<style>
			.colorful {
				border: 1px solid black;
				width: 150px;
				height: 150px;
				display: flex;
				align-items: center;
				justify-content: center;
				animation-name: change-color;
				animation-duration: 2s;
				animation-delay: 1s;
				animation-iteration-count: infinite;
				margin-bottom: 10px;
			}
			.normal {
				animation-direction: normal;
				background-color: lightblue;
			}
			.reverse {
				animation-direction: reverse;
				background-color: lightcoral;
			}
			.alternate {
				animation-direction: alternate;
				background-color: lightgreen;
			}
			.alternate-reverse {
				animation-direction: alternate-reverse;
				background-color: lightyellow;
			}
			@keyframes change-color {
				from {
					transform: translateX(0);
				}
				to {
					transform: translateX(300px);
				}
			}
		</style>
	</head>
	<body>
		<div class="colorful normal">normal</div>
		<div class="colorful reverse">reverse</div>
		<div class="colorful alternate">alternate</div>
		<div class="colorful alternate-reverse">alternate-reverse</div>
	</body>
</html>
```

- `animation-timing-function` - определяет кривую скорости в анимации
	- ease - в начале медленно, в середине быстро, потом медленно
	- leaner - на одинаковой скорости
	- ease-in - медленный старт
	- ease-out - медленный конец

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Animation Directions</title>
		<style>
			.colorful {
				border: 1px solid black;
				width: 150px;
				height: 150px;
				display: flex;
				align-items: center;
				justify-content: center;
				animation-name: change-color;
				animation-duration: 2s;
				animation-delay: 1s;
				animation-iteration-count: infinite;
				margin-bottom: 10px;
			}
			.ease {
				animation-timing-function: ease;
				background-color: lightblue;
			}
			.linear {
				animation-timing-function: linear;
				background-color: lightcoral;
			}
			.ease-in {
				animation-timing-function: ease-in;
				background-color: lightgreen;
			}
			.ease-out {
				animation-timing-function: ease-out;
				background-color: lightyellow;
			}
			@keyframes change-color {
				from {
					transform: translateX(0);
				}
				to {
					transform: translateX(300px);
				}
			}
		</style>
	</head>
	<body>
		<div class="colorful ease">ease</div>
		<div class="colorful linear">linear</div>
		<div class="colorful ease-in">ease-in</div>
		<div class="colorful ease-out">ease-out</div>
	</body>
</html>
```

- animation-fill-mode - определяет что делать с элементом, когда анимация не играет
	- none - изначальное значение. До и после анимации элемент не трогают
	- forwards - элемент останется на последнем кадре анимации
	- backwards - элемент вернется к первому кадру анимации
	- both - элемент будет следовать и первому и последнему кадру

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Animation Fill Mode Difference</title>
    <style>
        .container {
            position: relative;
            height: 200px;
            border: 1px solid #ccc;
            margin-bottom: 20px;
        }
        
        .colorful {
            width: 150px;
            height: 150px;
            display: flex;
            align-items: center;
            justify-content: center;
            animation-name: move-and-change;
            animation-duration: 3s;
            animation-delay: 2s;
            margin-bottom: 10px;
            position: absolute;
            top: 0;
        }
        
        .none {
            animation-fill-mode: none;
            background-color: lightblue;
            left: 0;
        }
        .forwards {
            animation-fill-mode: forwards;
            background-color: lightcoral;
            left: 200px;
        }
        .backwards {
            animation-fill-mode: backwards;
            background-color: lightgreen;
            left: 400px;
        }
        .both {
            animation-fill-mode: both;
            background-color: lightyellow;
            left: 600px;
        }
        
        @keyframes move-and-change {
            from {
                transform: translateY(0);
                background-color: purple;
            }
            to {
                transform: translateY(50px);
                background-color: orange;
            }
        }
        
        /* Линии для ориентира */
        .start-line, .end-line {
            position: absolute;
            width: 100%;
            height: 1px;
            background: red;
            left: 0;
        }
        .start-line {
            top: 0;
        }
        .end-line {
            top: 50px;
        }
    </style>
</head>
<body>
    <h3>Наблюдайте за поведением до (2 сек задержка) и после анимации:</h3>
    
    <div class="container">
        <div class="start-line"></div>
        <div class="end-line"></div>
        
        <div class="colorful none">none</div>
        <div class="colorful forwards">forwards</div>
        <div class="colorful backwards">backwards</div>
        <div class="colorful both">both</div>
    </div>
    
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
        <div>
            <h4>До анимации (первые 2 секунды):</h4>
            <ul>
                <li><strong>none</strong>: синий, на своей позиции</li>
                <li><strong>forwards</strong>: красный, на своей позиции</li>
                <li><strong>backwards</strong>: <span style="color: purple">фиолетовый</span>, у верхней линии</li>
                <li><strong>both</strong>: <span style="color: purple">фиолетовый</span>, у верхней линии</li>
            </ul>
        </div>
        
        <div>
            <h4>После анимации:</h4>
            <ul>
                <li><strong>none</strong>: вернется к синему, к начальной позиции</li>
                <li><strong>forwards</strong>: останется оранжевым у нижней линии</li>
                <li><strong>backwards</strong>: вернется к зеленому, к начальной позиции</li>
                <li><strong>both</strong>: останется оранжевым у нижней линии</li>
            </ul>
        </div>
    </div>
</body>
</html>
```

## CSS Transitions

CSS transitions позволяют плавно изменять значения свойств в течение определенного времени, вместо резких изменений.

## Основные свойства transition

- `transition-property` - указывает какие свойства анимировать
- `transition-duration` - указывает продолжительность перехода
- `transition-timing-function` - определяет кривую скорости
- `transition-delay` - указывает задержку перед началом

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS Transitions</title>
    <style>
        .box {
            width: 100px;
            height: 100px;
            background-color: blue;
            transition: all 0.5s ease;
        }
        
        .box:hover {
            width: 200px;
            background-color: red;
            transform: rotate(45deg);
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```

### transition-property
Указывает какие свойства анимировать:

```css
.element {
    /* Анимировать только ширину */
    transition-property: width;
    
    /* Анимировать несколько свойств */
    transition-property: width, height, background-color;
    
    /* Анимировать все изменяемые свойства */
    transition-property: all;
}
```

### transition-duration
Определяет продолжительность перехода:

```css
.element {
    transition-duration: 0.3s;    /* 0.3 секунды */
    transition-duration: 500ms;   /* 500 миллисекунд */
    transition-duration: 2s;      /* 2 секунды */
}
```

### transition-timing-function
Определяет кривую скорости анимации:

```css
.element {
    transition-timing-function: ease;        /* по умолчанию */
    transition-timing-function: linear;      /* постоянная скорость */
    transition-timing-function: ease-in;     /* медленный старт */
    transition-timing-function: ease-out;    /* медленный конец */
    transition-timing-function: ease-in-out; /* медленные старт и конец */
    transition-timing-function: cubic-bezier(0.1, 0.7, 1.0, 0.1); /* кастомная */
}
```

### transition-delay
Задержка перед началом перехода:

```css
.element {
    transition-delay: 0.2s;   /* 0.2 секунды задержки */
    transition-delay: 500ms;  /* 500ms задержки */
}
```

### Сокращенная запись

```css
.element {
    /* property | duration | timing-function | delay */
    transition: all 0.3s ease 0.1s;
    
    /* Несколько свойств с разными настройками */
    transition: width 0.5s ease, height 0.3s linear, background-color 1s;
}
```

### Практические примеры

#### Пример 1: Плавное изменение цвета

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        .button {
            padding: 15px 30px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        .button:hover {
            background-color: #45a049;
        }
        
        .button:active {
            background-color: #3d8b40;
        }
    </style>
</head>
<body>
    <button class="button">Наведите на меня</button>
</body>
</html>
```

#### Пример 2: Анимация нескольких свойств

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        .card {
            width: 200px;
            height: 100px;
            background-color: lightblue;
            margin: 20px;
            padding: 20px;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .card:hover {
            transform: scale(1.05) translateY(-10px);
            background-color: lightcoral;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <div class="card">Наведите на карточку</div>
</body>
</html>
```

#### Пример 3: Разные transition для разных свойств

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        .complex {
            width: 100px;
            height: 100px;
            background-color: blue;
            transition: 
                width 0.5s ease-in-out,
                height 0.3s linear,
                background-color 1s ease,
                transform 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
        }
        
        .complex:hover {
            width: 150px;
            height: 120px;
            background-color: red;
            transform: rotate(180deg);
        }
    </style>
</head>
<body>
    <div class="complex"></div>
</body>
</html>
```

## Какие свойства можно анимировать?

Не все CSS свойства можно анимировать. Вот основные анимируемые свойства:

- `color`, `background-color`, `border-color`
- `width`, `height`, `margin`, `padding`
- `opacity`, `visibility`
- `transform` (translate, rotate, scale, skew)
- `font-size`, `line-height`
- `box-shadow`, `text-shadow`
- `left`, `top`, `right`, `bottom`

## Разница между Animations и Transitions

| Transitions | Animations |
|-------------|------------|
| Запускаются при изменении состояния (hover, focus и т.д.) | Могут запускаться автоматически |
| Простые переходы между двумя состояниями | Сложные многоэтапные анимации |
| Не могут повторяться автоматически | Могут повторяться бесконечно |
| Меньше контроля над промежуточными состояниями | Полный контроль через keyframes |
