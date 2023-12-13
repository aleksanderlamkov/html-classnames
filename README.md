# Часто используемые имена классов в HTML-разметке

## Общие правила
- в имени класса не стоит использовать цифры
    ```html
    <!-- ❌ Неправильно -->
    <div class="element-1">...</div>
    
    <!-- ✅ Правильно -->
    <div class="first-element">...</div>
    ```
- имя класса лучше писать в нижнем регистре в `kebab-case` нотации, где каждое слово разделено символом дефиса
    ```html
    <!-- ❌ Неправильно -->
    <div class="userinfo">...</div>
    <div class="Userinfo">...</div>
    <div class="userInfo">...</div>
    <div class="UserInfo">...</div>
    <div class="USERINFO">...</div>
    <div class="USER-INFO">...</div>
    <div class="USER_INFO">...</div>

    <!-- ✅ Правильно -->
    <div class="user-info">...</div>
    ```
- имя класса не должно состоять из одной буквы
    ```html
    <!-- ❌ Неправильно -->
    <div class="w">...</div>

    <!-- ✅ Правильно -->
    <div class="wrapper">...</div>
    ```
- в имени класса не стоит злоупотреблять сокращениями: лучше написать `button` вместо `btn` и `link` вместо `lnk` (помните – код мы пишем один раз, а читать его мы и другие разработчики будем гораздо чаще, так что экономить буквы не стоит)
    ```html
    <!-- ❌ Неправильно -->
    <button class="btn">...</button>
    <a class="lnk">...</a>

    <!-- ✅ Правильно -->
    <button class="button">...</button>
    <a class="link">...</a>
    ```
- имя класса в большинстве случаев не должно дублировать имя тега элемента, к которому класс применяется
    ```html
    <!-- ❌ Неправильно -->
    <p class="p">...</p>
    <div class="div">...</div>
    <a class="a">...</a>

    <!-- ✅ Правильно -->
    <p class="paragraph">...</p>
    <div class="wrapper">...</div>
    <a class="link">...</a>
    ```
- имя класса элемента в целом должно отражать его функцию или стиль
    ```html
    <!-- ❌ Неправильно -->
    <button class="some-button">Красная кнопка</button>
    <div class="some-block">Тултип</div>

    <!-- ✅ Правильно -->
    <button class="red-button">Красная кнопка</button>
    <div class="tooltip">Тултип</div>
    ```
- имя класса может состоять из нескольких слов, по количеству – без ограничений, однако логично, что чем меньше слов в имени класса, тем проще его написать, прочесть и запомнить
    ```html
    <!-- ✅ Допустимо -->
    <span class="user-name-first-letter">A</span>
    ```
- в именах классов можно и нужно комбинировать слова, если этого требует контекст элемента (например, блок с классом `user` может содержать внутри себя блоки с классами `user-image` и `user-name`, а `user-name` может содержать, например, элемент с классом `user-name-first-letter`)
    ```html
    <!-- ✅ Правильно -->
    <div class="user">
      <img class="user-image" />
      <div class="user-name">
        <span class="user-name-first-letter">А</span>лександр
      </div>
    </div>
    ```
- зачастую для имени класса лучше использовать существительные, в редких случаях – прилагательные, например, когда класс является неким модификатором компонента; глаголы же в качестве имени классов обычно не используют вовсе
    ```html
  <!-- ❌ Неправильно -->
  <a class="go-back">...</a>
  <button class="submit">...</button>
  <form class="create-user">...</form>
  <div class="run-slider">...</div>

  <!-- ✅ Правильно -->
  <a class="go-back-link">...</a>
  <button class="submit-button">...</button>
  <form class="create-user-form">...</form>
  <div class="slider">...</div>

  <!-- ⚠️ Тоже правильно -->
  <button class="button red wide bold">...</button>
  <section class="section large-padding-y">...</section>
    ```
- существование абсолютно каждого класса в проекте должно быть оправдано: например, если у вас есть 5 абсолютно одинаковых по стилю секций, но с разным наполнением, то не стоит для каждой секции придумывать собственный класс, лучше обойтись одним унифицированным
    ```html
  <!-- ❌ Неправильно -->
  <section class="banner">...</section>
  <section class="features">...</section>
  <section class="catalog">...</section>
  <section class="about">...</section>
  <section class="contacts">...</section>
  <style>
    .banner { padding-block: 30px }
    .features { padding-block: 30px }
    .catalog { padding-block: 30px }
    .about { padding-block: 30px }
    .contacts { padding-block: 30px }
  </style>

  <!-- ✅ Правильно -->
  <section class="section">...</section>
  <section class="section">...</section>
  <section class="section">...</section>
  <section class="section">...</section>
  <section class="section">...</section>
  <style>
    .section { padding-block: 30px }
  </style>
    ```

## Структурные блоки с семантическими тегами
- `page` — элемент `<html>` или `<body>`
- `header` — элемент `<header>
- `content`, `main` — элемент `<main>`
- `footer` — элемент `<footer>`
- `section` — элемент `<section>`
- `aside`, `sidebar`, `widget` — элемент `<aside>`
- `nav`, `menu`, `navigation` — элемент `<nav>`

## Структурные блоки с нейтральными тегами (div, span)
- `inner`, `body` — вспомогательный элемент
- `wrapper`, `wrap` — вспомогательный элемент-обертка
- `container` — контейнер, ограничивающий ширину контентной части
- `grid` — сетка а-ля таблица
- `row` — строка в грид-сетке
- `column`, `col`, `cel` — столбец (ячейка) в грид-сетке

## Списки
- `list`, `items` — элементы `<ul>`, `<ol>` и `<dl>`
- `item` — элемент `<li>`

## Карточки
- `card` — элемент `<article>`

## Изображения
- `image`
- `img`
- `picture`
- `pic`
- `thumbnail`
- `thumb`
- `avatar`
- `logo`
- `icon`

## Текст
- `title`, `subtitle`, `heading`, `subheading`, `headline`, `subject`, `caption`, `label` — элементы от `<h1>` до `<h6>`
- `slogan`, `description`, `text` — слоганы и описания
- `blockquote`, `quote` — цитаты
- `copyright` — копирайт
- `link` — ссылки
- `code`, `snippet` — вставки кода

## Формы
- `form` — элемент `<form>`
- `form-group` — элемент `<fieldset>`
- `form-group-name`, `form-group-title`, `form-group-label` — элемент `<legend>`
- `form-item` — структурный элемент формы, оборачивающий элементы полей ввода

## Классические поля ввода
- `field` — корневой элемент `<div>` компонента поля ввода
- `field-label` — элемент `<label>`
- `field-control` — элементы `<input />`, `<textarea>`, `<select>`

## Чекбоксы
- `checkbox` — корневой элемент `<label>` компонента чекбокса
- `checkbox-control` — элемент `<input />` компонента чекбокса
- `checkbox-emulator` — элемент `<span>` компонента чекбокса для эмуляции "квадрата"
- `checkbox-label` — элемент `<span>` компонента чекбокса для подписи

## Радиокнопки
- `radios` — корневой элемент `<fieldset>` компонента радиокнопок
- `radios-label` — элемент `<legend>` компонента радиокнопок

## Разное
- `button` — элемент `<button>`
- `dropdown` — выпадающий список
- `accordion`, `spoiler` — компонент "аккордеон"
- `modal`, `popup` — модальное окно
- `overlay`, `backdrop` — затемняющий фон (прим. под модальными окнами)
- `tooltip`, `hint` — тултип, всплывающая подсказка
- `slider`, `carousel` — слайдер
- `pagination` — пагинация (горизонтальное меню с номерами страниц и стрелками влево-вправо)
- `breadcrumbs` — "хлебные крошки" (навигация по иерархии веб-приложения, часто следует сразу после шапки страницы)
- `basket`, `cart` — корзина
- `summary`, `total`, `amount` — сумма чего-либо (прим. итоговая сумма заказа)
- `search`, `quick-search` — форма поиска
- `user` — элемент с данными о пользователе
- `features`, `advantages`, `benefints` — элемент с перечислением каких-то особенностей / преимуществ товара или услуги
- `socials`, `soc1als` — социальные сети

## Модификаторы размеров
- `small`
- `tiny`
- `medium`
- `base`
- `big`
- `large`
- `huge`
- `narrow`
- `wide`

## Модификаторы наличия чего-либо
- `has-icon`
- `has-error`
- `has-underline`

## Модификаторы состояний
- `is-current` — текущий пункт меню
- `is-active` — активная кнопка
- `is-visible`, `is-shown` — видимый тултип
- `is-hidden`, `hidden` — скрытая информация
- `is-open` — открытое модальное окно
- `is-expanded` — раскрытый выпадающий список
- `is-invalid`, `is-error` — поле ввода с некорректными введенными данными
- `warning` — предупреждение
- `alert`, `notification` — уведомление
- `success` — статус успешного выполнения чего-либо
- `loading`, `processing`, `pending` — статус загрузки
