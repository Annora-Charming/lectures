---
title: Basic - HTML
---

## Введение в HTML

![first web developer](assets/html/web-dev.png)

[Дмитрий Вайнер](https://github.com/dmitryweiner)

[видео](https://drive.google.com/file/d/1OkbiegilaFIY1DPr1JhmBx4Bg8iGSWFU/view?usp=sharing)
---

### Что такое HTML?
* **H**yper **T**ext **M**arkup **L**anguage: язык разметки 
  [гипертекста](https://ru.wikipedia.org/wiki/%D0%93%D0%B8%D0%BF%D0%B5%D1%80%D1%82%D0%B5%D0%BA%D1%81%D1%82).
* HTML произошёл от [SGML](https://ru.wikipedia.org/wiki/SGML)
  * От SGML произошёл также [XML](https://ru.wikipedia.org/wiki/XML), они очень похожи.
* Создатель: [Тим Бернерс-Ли](https://twitter.com/timberners_lee).
* Первый в мире веб-сайт http://info.cern.ch.
* Текущая версия: 5.
---

### Пример HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Заголовок</title>
</head>
<body>
  <h1>Заголовок</h1>
  
  <p>My first paragraph.</p>
</body>
</html> 
```
![head body](assets/html/head-body.png)
---

### Структура документа
* Документ представляет собой иерархическое дерево тегов.
* Документ состоит из корневого тега html, в котором должны лежать body и head.
* Тег, лежащий внутри другого тега, называется потомком, а тот называется родителем.
* Теги на одном уровне называют siblings.
---

![dom tree](assets/html/dom-tree.jpg)
---

### Основные идеи языка
* Теги обозначаются угловыми скобками:
```html
<p>Тест</p>
```
* Теги объясняют браузеру, как отображать их содержимое.
* Тег может содержать текст вложенные теги, если это позволено спецификацией:
```html
<div>
    <p>Тест</p>
</div>
```
* Если тег открылся ```<p>```, он должен закрыться ```</p>```.
---

### Основные идеи языка
* Тег может не подразумевать закрывающего тега, тогда он оканчивается знаком /:
```html
<img src="https://picsum.photos/200" />
```
* Внутри тега могут указываться параметры. Набор параметров специфичен для каждого тега.
* Символы переноса игнорируются (кроме как внутри определённых тегов).
---

### Тег и параметры
* У тега могут быть параметры (атрибуты).
* Они пишутся внутри тега, разделяются пробелом (или переносами), обрамляются двойными кавычками:
```html
<img src="https://picsum.photos/200" width="200" height="200" alt="рандомная картинка" />
```
* Набор параметров зависит от тега.

---

![tags](assets/html/tags.png)
---

### Основные теги
* **h1, h2, ..., h5**: заголовок страницы.
* **p**: параграф текста.
* **br**: перенос.
* **ul**: ненумерованный список.
* **ol**: нумерованный список.
* **div**: блок элементов.
* **img**: картинка.
* **a**: ссылка.
* **button**: кнопка.
* **input**: поле ввода.
* [Полный список](https://html5book.ru/html-tags/), [ещё](https://www.w3schools.com/tags/).
---

# Заголовок 1
## Заголовок 2
### Заголовок 3
#### Заголовок 4
##### Заголовок 5
```html
<h1>Заголовок 1</h1>
<h2>Заголовок 2</h2>
<h3>Заголовок 3</h3>
<h4>Заголовок 4</h4>
<h5>Заголовок 5</h5>
```
---

### &lt;p&gt;
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
```html
<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
</p>
```
---

### &lt;br&gt;
Lorem ipsum dolor sit amet,

consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
```html
<p>
  Lorem ipsum dolor sit amet,<br/>
  consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
</p>
```
---

### &lt;ul&gt;
* Элемент 1
* Элемент 2
* Элемент 3

```html
<ul>
  <li>Элемент 1</li>
  <li>Элемент 2</li>
  <li>Элемент 3</li>
</ul>
```
---

### &lt;ol&gt;
1. Элемент 1
2. Элемент 2
3. Элемент 3

```html
<ol>
  <li>Элемент 1</li>
  <li>Элемент 2</li>
  <li>Элемент 3</li>
</ol>
```
---

### &lt;div&gt;
Просто блок текста, отделённый отступами.

Ещё один блок.

```html
<div>
  Просто блок текста, отделённый отступами.
</div>
<div>
  Ещё один блок.
</div>
```
---


### &lt;img&gt;
* Параметры:
  * **src**: путь до картинки.
  * **width**: ширина.
  * **height**: высота.
  * **alt**: альтернативный текст.

<img src="https://picsum.photos/200" width="200" height="200" alt="рандомная картинка" />

```html
<img src="https://picsum.photos/200" width="200" height="200" alt="рандомная картинка" />
```

---

### &lt;a&gt;
* Параметры:
  * **href**: путь перехода.
  * **target**: открывать ли новую вкладку.

<a href="https://google.com" target="_blank">Ссылка</a>

```html
<a href="https://google.com" target="_blank">Ссылка</a>
```
---

### &lt;button&gt;
* Параметры:
  * **type**: тип кнопки button, reset, submit.

<button>Нажми меня</button>

```html
<button>Нажми меня</button>
```
---

### &lt;input&gt;
* Параметры:
  * **type**: тип поля text, number, radio.

<input type="text" value="я текстовое поле ввода"/>

```html
<input type="text" value="я текстовое поле ввода"/>
```
---

### Entities
* Для вывода символов, встречающихся в HMTL-разметке (как &lt; и &gt;), используются entities.
* Этот же приём используется для вывода эмодзи, разных других интересных символов вроде &copy;.
* [Каталог entities](https://www.freeformatter.com/html-entities.html).
* [Список эмодзи](https://www.w3schools.com/charsets/ref_emoji.asp).
```html
&copy; отображает ©
&#128030; (десятичный код) 
или &#x1F41E; (16-ричный) отображают 🐞
```
---

### Блок &lt;head&gt;
* В этом блоке подключаются:
  * Скрипты JavaScript.
  * Стили.
* Указывается title страницы (то, что отображается в заголовке вкладки).
* И многие другие полезные вещи:
  * Кодировка.
  * Ключевые слова для SEO.
---

### Кодировка
* Весь мир к счастью перешёл на кодировку [UTF-8](https://ru.wikipedia.org/wiki/UTF-8).
* Именно её и стоит указывать:
```html
<head>
    <meta charset="UTF-8">
</head> 
```
---
### Стили
* Стили можно определять непосредственно на странице:
```html
<html>
<head>
    <style>
      .class { 
        background-color: red;
      }
    </style>
</head>
<body>
...
</body>
</html>
```
---

### Стили
* Либо во внешнем файле:

```html
<html>
    <head>
      <link rel="stylesheet" href="styles.css">
    </head>
    <body>
    ...
    </body>
</html>
```
---


### Скрипты
* Активное содержимое страницы описывается на языке JavaScript и тоже располагается в блоке &lt;head&gt;.
* Либо непосредственно в теге &lt;script&gt;:
```html
<head>
    <script type="application/javascript">
      console.log('Hello world!');
    </script>
</head>
```
* Либо в отдельном файле:
```html
<head>
      <script src="script.js"></script>
</head>
```
---

### Относительные и абсолютные пути
* Ссылки на ресурсы могут быть относительными и абсолютными ([подробнее](https://htmlacademy.ru/blog/boost/frontend/links)).
* Абсолютные ссылки указываются вместе с доменом:
```html
<script src="http://google.com/script.js"></script>
```
* Относительные ссылки указываются от текущего файла:
```html
<script src="../scripts/script.js"></script>
```
---
### Полезные ссылки
* https://www.w3schools.com/tags/
* https://www.w3schools.com/html/default.asp
* https://htmlacademy.ru/courses/basic-html-css