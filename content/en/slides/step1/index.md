---
title: Advertising effectiveness
summary: 
authors:
- Rodina Darya
- Kartashova Alice
- Sasin Yaroslav
- Vasilieva Julia
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

# Advertising effectiveness

by:
- Rodina Darya  
- Kartashova Alice  
- Sasin Yaroslav  
- Vasilieva Julia  

---

## Formulation of the problem

How to sell goods on the market?

1. Organize an advertising campaign for a new product  

2. Ensure that profits excessively cover advertising costs  

---

## The main problem

Необходима эффективная рекламная кампания!

---

## The purpose and objectives of the project

### **The main proiect purpose:**

finding the dependence of sales on the effectiveness of an advertising campaign.

### **Project objectives:**

- project model  

- project algorithmization 

- translation of algorithms into code  

---

## What is advertising?

**Advertising** is a direction in marketing communications, within the framework of which information is disseminated to draw attention to the object of advertising with the goal of forming or maintaining interest in it.

---

## Campaign Model

### **Factors**

The main factors influencing sales are:

1. $N$ - the number of potential buyers
2. $t$ - elapsed time from the start of the campaign
3. $n (t)$ - the number of already informed buyers
4. $a (t)$ - the intensity of the advertising campaign

---
## Campaign Model

### Model

$$\frac{\mathrm{d}n}{\mathrm{d}t} = (a_1(t) + a_2(t)n(t))(N - n(t))$$

$\frac{\mathrm{d}n}{\mathrm{d}t}$ - скорость изменения числа потребителей, узнавших о товаре и готовых купить  
$a_1(t)(N – n(t))$ -число уже информированных покупателей пропорционально числу еще не информированных покупателей - модель Мальтуса  
$a_2(t)n(t)(N – n(t))$ - распрастранение информации покупателями, которые уже знают о товаре - логистичесая кривая  
$N - n(t)$ - количество потенциальных покупателей, не знающих о товаре

---

## Campaign Model

### Model

$$\frac{\mathrm{d}n}{\mathrm{d}t} = (a_1(t) + a_2(t)n(t))(N - n(t))$$

For $a_1(t)\gga_2(t)n(t)$ we get a model of the Maltus type:

![](1.png)

---

## Campaign Model

### Model

$$\frac{\mathrm{d}n}{\mathrm{d}t} = (a_1(t) + a_2(t)n(t))(N - n(t))$$

For $a_1(t)\lla_2(t)n(t)$ we get the equation of the logistic curve::

![](2.png)
