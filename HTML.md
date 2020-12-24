# HTML 
Markup language for static web pages, first created in 1993, now at version HTLM5.

## Document structure
```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
    <title>Базовая разметка HTML</title>
</head>
<body></body>
</html>
```

## Text structuring tags
<p> <pre> <code>
<h1>, <h2>, ...
<ul>
<ol>
<li>

## Global attributes
align=["right", "left, "center"]
title=<string> -- will be shown on mouse hover
id


## Tables
<table>
    <thead> <!-- Блок с заголовками -->
        <tr> <!-- Строка -->
            <th>Первая ячейка</th>
            <th>Вторая ячейка</th>
            <th>Третья ячейка</th>
        </tr>
    </thead>

    <tbody> <!-- Тело таблицы -->
        <tr> <!-- Вторая строка -->
            <td>Первая ячейка</td>
            <td>Вторая ячейка</td>
            <td>Третья ячейка</td>
        </tr>
    </tbody>
</table>

rowspan and colspan to create merge cells

## Special characters (mnemonics)
&clubs; &mdash; &lt;
https://ru.wikipedia.org/wiki/%D0%9C%D0%BD%D0%B5%D0%BC%D0%BE%D0%BD%D0%B8%D0%BA%D0%B8_%D0%B2_HTML

## Links
<a href="Ссылка на документ">Текст ссылки</a>

## Images
<img src="https://example.com/images.png" alt="Аналитика компании за 2007 год">

## Audio
<audio src="путь к аудио-файлу" controls></audio>

## Video
<video src="https://example.com/our-video.mp4" controls></video>

<video width="500" height="500" controls>
    <source src="https://example.com/our-video.mp4" type="video/mp4">
    <source src="https://example.com/our-video.webm" type="video/webm">
    <source src="https://example.com/our-video.ogg" type="video/ogg">
</video>

## Meta attributes

## Forms
<form action="/search">
  // Данные, после заполнения, будут отправлены на страницу /search
  <input type="text">
</form>

<form>
    <label>
        <input type="checkbox" name="languages" value="HTML">
        Хочу изучать HTML
    </label>
    <label>
        <input type="checkbox" name="languages" value="CSS">
        Хочу изучать CSS
    </label>
    <label>
        <input type="checkbox" name="languages" value="JS">
        Хочу изучать JS
    </label>
</form>

<form>
    <label>
        <input type="radio" name="question" value="yes">
        Да
    </label>
    <br>
    <label>
        <input type="radio" name="question" value="no">
        Нет
    </label>
</form>

<form action="/people">
    <label>
        <input type="radio" name="gender" value="m">
        Mail
    </label>
    <br>
    <label>
        <input type="radio" name="gender" value="f">
        Female
    </label>
	
</form>
<form action="/people">
    <textarea rows="4" cols="30">textarea с 5 строками и 30 столбцами</textarea>
</form>

<form>
    <select>
        <option disabled>Какой курс вы хотите пройти?</option>
        <option>JS</option>
        <option>PHP</option>
        <option>Java</option>
        <option>Racket</option>
        <option>HTML</option>
        <option>CSS</option>
    </select>
</form>

<form>
    <select multiple>
          <option>JS</option>
          <option>PHP</option>
          <option>Java</option>
          <option>Racket</option>
          <option>HTML</option>
          <option>CSS</option>
    </select>
</form>


<form>
    <button>Отправить</button>
</form>

Alltogether

<h2>Форма поиска</h2>
<form>
    <label>
        Введите ваш запрос
        <input type="text">
    </label>
    <select>
        <option disabled>В каком разделе искать?</option>
        <option>JS</option>
        <option>HTML</option>
        <option>CSS</option>
    </select>
    <button>Искать</button>
</form>

## Semantic tags
article
aside
footer
header
main
nav
section

vs

div etc

<section itemscope itemtype="http://schema.org/Organization">
    <h1 itemprop="name">Компания «Прауд»</h1>
    <p>Адрес: <span itemprop="address">г.Мотино, улица Строителей, дом 6</span></p>
    <p>Телефон: <span itemprop="telephone">8 (8765) 333-00-00</span></p>
    <p>Email: <span itemprop="email">info@proud-company.test</span></p>
</section>

<header>
    <img src="/logo.png" alt="Логотип"> <!-- Логотип сайта -->
    <nav> <!-- Меню -->
        <ul>
            <li><a href="/">Главная</a></li>
            <li><a href="/about">О нас</a></li>
        </ul>
    </nav>
</header>

<header>
    <img src="/logo.png" alt="Логотип"> <!-- Логотип сайта -->
    <nav> <!-- Меню -->
        <ul>
            <li><a href="/">Главная</a></li>
            <li><a href="/about">О нас</a></li>
            <li><a href="/contacts">Контакты</a></li>
        </ul>
    </nav>
</header>

<aside> <!-- Боковая панель (сайдбар) -->
    <nav> <!-- Дополнительное меню раздела -->
        <ul>
            <li><a href="/service-1/">Услуга 1</a></li>
            <li><a href="/service-2/">Услуга 2</a></li>
            <li><a href="/service-3/">Услуга 3</a></li>
        </ul>
    </nav>
</aside>

<main>
    <p>Основной контент страницы. Это может быть статья, описание услуги, данные на странице контакты</p>

    <section class="callback-form">
        <h2>Оставить заявку</h2>
        <form>
            <!-- Здесь форма заказа услуги -->
        </form>
    </section>

    <section class="more">
          <h2>Читайте также</h2>
          <article class="article-block">
              <h3>Услуга 2</h3>
              <p>Описание новой услуги</p>
              <a href="#">Ссылка на услугу</a>
          </article>

          <article class="article-block">
              <h3>Услуга 3</h3>
              <p>Описание новой услуги</p>
              <a href="#">Ссылка на услугу</a>
          </article>

          <article class="article-block">
              <h3>Услуга 4</h3>
              <p>Описание новой услуги</p>
              <a href="#">Ссылка на услугу</a>
          </article>
    </section>
</main>