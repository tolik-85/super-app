<script>
import inputText from './components/inputText.vue'
import inputCheckox from './components/inputCheckox.vue'
import inputRadio from './components/inputRadio.vue'
import inputRange from './components/inputRange.vue'
import inputDate from './components/inputDate.vue'

export default {
  components: { inputText, inputCheckox, inputRadio, inputRange, inputDate },
}
</script>

<template>
  <div class="container">
    <inputText />
  </div>
  <div class="container">
    <inputCheckox />
  </div>
  <div class="container">
    <inputRadio />
  </div>
  <div class="container">
    <inputRange />
  </div>
  <div class="container">
    <inputDate />
  </div>
</template>

<!--

Основные элементы ввода (<input>)

Текстовое поле → <input type="text"> --
Пароль → <input type="password">
Чекбокс → <input type="checkbox"> --
Радио-кнопка → <input type="radio"> --
Кнопка отправки → <input type="submit">
Кнопка сброса → <input type="reset">
Обычная кнопка → <input type="button">
Файл (загрузка) → <input type="file">
Скрытое поле → <input type="hidden">

Числовые и специальные поля

Число → <input type="number">
Ползунок (диапазон) → <input type="range"> --
Дата → <input type="date">
Дата и время → <input type="datetime-local">
Месяц → <input type="month">
Неделя → <input type="week">
Время → <input type="time">
Цвет → <input type="color">

Контактные поля

E-mail → <input type="email">
Телефон → <input type="tel">
URL (сайт) → <input type="url">
Поиск → <input type="search">

Другие элементы ввода

Многострочное текстовое поле → <textarea>
Выпадающий список → <select> + <option>
Группа опций → <optgroup> (внутри <select>)
Множественный выбор (тег <select> с multiple)
Кнопка → <button> (лучше, чем <input type="button">)
Метка для поля → <label> (для удобства пользователя)
Группа полей → <fieldset> + <legend>
Автозаполнение списка → <datalist> + <input list="id">
Описание поля (подсказка) → <output>



-->
