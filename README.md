# Python 6 Data Science
## HomeWork # 04

[![Language](https://img.shields.io/badge/language-python-blue)](https://www.python.org)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/VlodyaKr/Python-6-Web-HomeWork-13)

---
# Завдання:

## Частина перша

Є набір даних `speed`, який є значенням швидкості для деякого транспортного засобу в певний момент спостереження. Очевидно, що дані мають дискретний вигляд. Відомо, що спостереження відбувалися з періодом одну годину.

1. Приймемо, що в нульовій координаті у нас швидкість 25 км/год, згідно з набором даних speed. Помістіть у змінну time — вектор часу, створений за допомогою `np.linspace` (всього 12 спостережень, від 0 до 11 годин)
2. Виконайте виведення масиву `time`
3. Виконайте виведення графіка - значення точок швидкості (`plot` або `scatter`). Встановіть розмір області (0, 11) та (0, 130). Задайте відображення сітки
4. Виконайте інтерполяцію за допомогою `interp1d`(`kind='cubic'`) та отримайте функцію на `10000` значень. Побудуйте безперервний графік отриманої функції.
5. Відповідно до фізичного змісту першої похідної, похідна функції у точці є миттєва швидкість точки, тобто $ν(t) = s′(t) = \frac{dt}{ds}.$ Звідси,
$ds = v(t) dt.$ Інтегруючи отриману рівність у межах від $t_{1}$ до $t_{2}$, отримуємо $$\int ds = \int_{t_{1}}^{t_{2}} v(t) dt$$ Тоді шлях, пройдений точкою при нерівномірному русі по прямій зі змінною швидкістю $v(t)$ за період часу $[t_{1},t_{2}]$ виражається інтегралом $$S = \int_{t_{1}}^{t_{2}} v(t) dt$$ Обчисліть інтеграл для отриманої інтерполяційної функції на проміжку $[0, 11]$.
6. Виконайте також пункти 4 та 5 для `kind='quadratic'`

## Частина друга

Нехай все населення ($N$ індивідів) ділиться на три групи: індивіди, які сприйнятливі до цієї хвороби, але здорові (susceptible) $S(t)$; заражені індивіди (infected) - $I(t)$ (вони хворі самі і є носіями хвороби) та здорові індивіди, які мають імунітет до даної хвороби (recovered) - $R(t)$.

Приймемо, що 
$$S(t) + I(t) + R(t) = N \quad\quad\quad \textbf{(1)}$$

Вважаємо, що коли кількість інфікованих перевищує певне фіксоване значення $I^{*}$, швидкість зміни числа сприйнятливих до хвороби індивідів буде пропорційно числу самих сприйнятливих індивідів. $$\frac{dS}{dt} = -αS \quad\quad\quad \textbf{(2)}$$
Тепер, коли кожен сприйнятливий до хвороби індивід зрештою занедужує і стає інфекційним, то швидкість зміни інфікованих індивідів це різниця за одиницю часу між захворілими і тими хто одужує. $$\frac{dI}{dt} = αS - βI \quad\quad\quad \textbf{(3)} $$
Постійні пропорційності $α$ та $β$ називають коефіцієнтами захворюваності та одужання відповідно.

Швидкість зміни числа індивідів, що одужують: $$\frac{dR}{dt} = \beta S \quad\quad\quad \textbf{(4)}$$
Щоб рішення відповідних рівнянь визначалися однозначно, необхідно задати початкові умови. Приймемо, що:


*   $α = 0.5$
*   $β = 0.3$
*   $N = 1000000$
*   $S(0) = 990000$
*   $I(0) = 7000$
*   $R(0) = 3000$
*   $t_{0}, t_{f} = 0,25$

Необхідно виконати:

1. Розв'язати диференціальне рівняння (2) та побудувати графік функції  $S(t)$
2. Розв'язати диференціальне рівняння (3) та побудувати графік функції  $I(t)$


---

#### Автор
[![GitHub Contributors Image](https://contrib.rocks/image?repo=VlodyaKr/Python-6-Data-Science-HomeWork-04)](https://github.com/VlodyaKr)

#### Володимир Кравченко
[Написати автору листа](mailto:vlodya@gmail.com?subject=Python-6-Data-Science-HomeWork-04)
