---
title: Резюме и прогресс
categories:
excerpt: >-
  Внешний вид панели для отслеживания прогресса.
layout: post
---

Я подумываю добавить резюме в свой список страниц на сайте.  И для
него я хочу сделать полосы прогресса.  Вот я нашел на странице
[W3school][w3css] стиль, как раз подходящий для этой цели.  Вот такие
панели мне нравятся:

{% for langcard in site.data.resume.languages %}
  <header><h3>{{ langcard.name }}</h3></header>
  {% for aimcard in langcard.aims %}
    {% include aimcard.html %}
  {% endfor %}
{% endfor %}

Для этих задач я думаю сделать отдельные файлы с данными (для языков
это будет `resume/languages.yml`).  Структура этого файла будет такой:
- name : Наименование языка
- aims : Отдельная цель
  - header : Наименование цели
  - cent : Прогресс в процентах
  - bartext : Надпись на панели прогресса
  - text : Подробная расшифровка на карточке

А еще было бы неплохо переместить мой прошлый сайт в этот.

[w3css]: https://www.w3schools.com/w3css/w3css_progressbar.asp
