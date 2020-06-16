---
title: Презентации в Markdown
summary: 
authors:
- Rodina Darya
institute:
- RUDN University, Russian Federation
#authors: []
tags: []
categories: []
date: "2019-02-05T00:00:00Z"
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: black
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula
---

# Презентации в Markdown

Докладчик: Родина Дарья

{{< speaker_note >}}
Еще раз добрый день. Тема моего доклада "Презентации в MD". Зовут меня Родина Дарья. Итак:
{{< /speaker_note >}}

---

## Описание шаблона презентации

- HTML5
- CSS
- JavaScript
- jQuery

{{< speaker_note >}}
- HTML5 - язык гипертекстовой разметки, то, на чем базируется презентация
- CSS - оформление презентации (описание того, где, что и как будет располагаться)
- JavaScript - придает интерактивность веб странице
- jQuery - набор функций javascript
{{< /speaker_note >}}

---

## Примеры шабонов

- fathom.js
- desk.js
- CSS-based Slideshow System - 
- impress.js
- reveal.js

---

# Презентации в теме Academic

---

## Особенности 

1. Простота использования 
2. Поддержка заметок докладчика
3. Возможность написания стилей

---

## Элементы управления
 
- Следующий слайд: «Стрелка вправо» или «Пробел»
- Предыдущий слайд: `Стрелка влево`
- Начало презентации: `Дом`
- Конец презентации: `Конец`
- Обзор: `Esc`
- Заметки выступающего: `S`
- Полноэкранный режим: `F`
- Изменение масштаба: `Alt + Click`
- [Экспорт в PDF] (https://github.com/hakimel/reveal.js#pdf-export): `E`

---

## Выделение кода

Код внутри строки: `variable`

Выведенный блок кода:
```matlab
function y = g(t,x)
    y = (m(t) + k(t)*x)*(300 - x);
end
```

---

## Математические функции

Внутри строки: $a_1(t) + a_2(t)n(t)$

Выделение формулы:

$$
\frac{\mathrm{d}n}{\mathrm{d}t} = (a_1(t) + a_2(t)n(t))(N - n(t))
$$

---

## Постепенное появление текста

```
{{%/* fragment */%}} secret {{%/* /fragment */%}}
{{%/* fragment */%}} secret {{%/* /fragment */%}}
{{%/* fragment */%}} secrert {{%/* /fragment */%}}
```

Key: `Space`

{{% fragment %}} Научпрог {{% /fragment %}}
{{% fragment %}} лучший {{% /fragment %}}
{{% fragment %}} предмет!!! {{% /fragment %}}

---

A fragment can accept two optional parameters:
class: use a custom style (requires definition in custom CSS)
weight: sets the order in which a fragment appears

---


## Заметки для выступающего 

Возможно также добавление заметок в презентацию

```markdown
{{%/* speaker_note */%}}
- ваши заметки
{{%/* /speaker_note */%}}
```

{{< speaker_note >}}
- Научпрог лучший предмет!!!
- Научпрог лучший предмет!!!
- Научпрог лучший предмет!!!
- Научпрог лучший предмет!!!
- Научпрог лучший предмет!!!
- Научпрог лучший предмет!!!
- Научпрог лучший предмет!!!
- Научпрог лучший предмет!!!
{{< /speaker_note >}}

Key: `S`

---

## Темы презентаций

- black: черный фон, белый текст, голубые ссылки (базовый)
- white: белый фон, черный текст, голубые ссылки 
- league: серый фон, белый текст, голубые ссылки
- beige: Beige background, dark text, brown links
- sky: голубой фон, thin dark text, голубые ссылки

---

- night: черный фон, жирный белый текст, оранжевые ссылки 
- serif: фон цвета "капучино", серый текст, коричневые ссылки
- simple: белый фон, черный текст, голубые ссылки 
- solarized: кремовый фон, темно-зеленый текст, голубые ссылки

---

## Настройка слайдов

```markdown
{{</* slide background-image="/img/bobbbb.jpg" */>}}
```

---

{{< slide background-image="/img/bobbbb.jpg" >}}

---

{{</ slide background-color="#990099" />}}

## Настройка слайдов

```markdown
{{</* slide background-color="#990099" */>}}
```

---

{{</ slide class="colorRed" />}}

## Настройка слайдов - CSS

Файл: `assets/css/reveal_custom.css`

```css
.reveal section h1,
.reveal section h2,
.reveal section h3 {
  color: navy;
}

.reveal .colorRed {
  color: red;
}
```

