---
title: Эффективность рекламы, второй этап
summary: Определение алгоритма для дальнейшего написания программы
authors:
- Родина Дарья
- Карташова Алиса
- Сасин Ярослав
- Васильева Юлия
institute:
- РУДН, Российсская Федерация
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

## Эффективность рекламы
# 1 этап

---

## Модель рекламной кампании

Основными факторами влияния на продажи являютя:

1. $N$ - число потенциальных покупателей
2. $t$ - прошедшее время от начала кампании
3. $n (t)$ - число уже информированных покупателей
4. $a (t)$ - интенсивность рекламной кампании

---

## Модель рекламной кампании

$$\frac{\mathrm{d}n}{\mathrm{d}t} = (a_1(t) + a_2(t)n(t))(N - n(t))$$

$ \frac {\mathrm{d} n}{\mathrm{d} t} $ - скорость изменения числа потребителей, узнавших о товаре и готовых купить  
$ a_1 (t) (N - n (t)) $ - число уже информированных покупателей пропорционально числу еще не информированных покупателей - модель Мальтуса

---

$ a_2 (t) n (t) (N - n (t)) $ - распрастранение информации покупателями, которые уже знают о товаре - логистичесая кривая   
$ N - n (t) $ - количество потенциальных покупателей, не знающих о товаре

---

## Модель рекламной кампании

$$\frac{\mathrm{d}n}{\mathrm{d}t} = (a_1(t) + a_2(t)n(t))(N - n(t))$$

При $a_1(t)\gga_2(t)n(t)$ получаем модель типа Мальтуса:

![](1.png)

---

## Модель рекламной кампании

$$\frac{\mathrm{d}n}{\mathrm{d}t} = (a_1(t) + a_2(t)n(t))(N - n(t))$$

При $a_1(t)\lla_2(t)n(t)$ получаем уравнение логистической кривой:

![](2.png)

---

![](block.png)

---

## Решение дифференциального уравнения

$$ 1. \frac{dn}{dt} =(a_1 + a_2n)(N - n) $$

$$ 2.  \frac{dn}{dt} =(a_1 + a_2(t)n)(N - n) $$ 

Wherein

$$ a_1(t) = a_1t $$

$$ a_2(t) = a_2t $$

---

## Решение дифференциального уравнения

$$ 1.\frac{dn}{(a_1 + a_2n)(N - n)} = dt $$ 

$$ 2.\frac{dn}{(a_1 + a_2n)(N - n)} = tdt $$

---

## Решение дифференциального уравнения


$$ \int\, \mathrm{d}t = t + C $$
$$ \int t\, \mathrm{d}t = \frac{t^2}{2} + C $$
$$ \int \frac{dn}{(a_1 + a_2n)(N - n)}\, \mathrm{d}t = ??? $$

---

$$ -\int \frac{dn}{(a_1 + a_2n)(-N + n)}\, \mathrm{d}t =  $$

$$ = \frac{1}{a_2n+a_1}\int\frac{1}{n-N}\, \mathrm{d}n - $$

$$ - \frac{a_2}{a_2N + a_1} \int \frac{1}{a_2n + a_1} \mathrm{d}n  $$

---

$$ \int \frac{dn}{n-N} = \int \frac{d(n-N)}{n-N} $$
$$ \int \frac{d(n-N)}{n-N} = ln(n-N) $$
$$ \int \frac{dn}{a_1y+a_2} = \frac{ln(a_2n+a_1)}{a_2} $$

---

$$ \frac{1}{a_2N} (\int (\frac{1}{n-N} - \frac{a~2}{a_2n+a_2})dn = $$

$$ \frac{1}{a_2N} (ln(n-N) - ln(a_2n+a_1)) $$

---

$$ n(t) = \frac{a_1 + Ne^{(a_1+a_2N)(T+C)}}{-a_2 + e^{(a_1+a_2N)(T+C)}} $$
 
$$ C = \frac {ln\frac{N_0a_2+a_1}{N_0-N}}{a_1+a_2N} - X_0 $$

---
Если a_1 и a_2 - линейные функции:

$$ X = x $$

Если a_1 и a_2 - константы:

$$ X = \frac {x^2}{2} $$

