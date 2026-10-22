# **Вариант 5 — мои решения**

## ***Задача 1***
Дано: $\overline{(X < 5)} \lor (X < 3) \land \overline{(X < 2)} \lor (X < 1)$, $X = 4$

Подставляю $X=4$:
- $X < 5 \to 4 < 5 = T \to \overline{(X < 5)} = F$
- $X < 3 \to 4 < 3 = F$
- $X < 2 \to 4 < 2 = F \to \overline{(X < 2)} = T$
- $X < 1 \to 4 < 1 = F$
- Сначала считаем конъюнкцию: $(X < 3) \land \overline{(X < 2)} = F \land T = F$
- Теперь дизъюнкции слева направо: $F \lor F = F$, потом $F \lor F = F$

Ответ: ***False***

---
## ***Задача 2***
### Дано (простые высказывания и обозначения)

- $P_1$: $l \perp a$
- $P_2$: $l \perp b$
- $P_3$: $a \subset \pi$
- $P_4$: $b \subset \pi$
- $P_5$: $a \nparallel b$

### Заключение (простое высказывание)

- $Q$: $\forall c \subset \pi: l \perp c$

---

### Символическая запись составного высказывания

$$
(P_1 \land P_2 \land P_3 \land P_4 \land P_5) \implies Q
$$

Подстановка исходных высказываний:

$$
(l \perp a \land l \perp b \land a \subset \pi \land b \subset \pi \land a \nparallel b) \implies (\forall c \subset \pi: l \perp c)
$$

---

### ***Ответ:***

Утверждение верно;
$$
(l \perp a \land l \perp b \land a \subset \pi \land b \subset \pi \land a \nparallel b) \implies (\forall c \subset \pi: l \perp c)
$$


---

## ***Задача 3***

**Дано:**
$X \to (Y \lor Z) \lor ((\overline{X} \to Y) \lor Z)$

**Ключевые шаги:**
1. $\overline{X} \to Y \equiv X \lor Y$
2. Подставляем: $X \to (Y \lor Z) \lor (X \lor Y \lor Z)$
3. Упрощаем дизъюнкцию: $X \to (X \lor Y \lor Z)$
4. Заменяем импликацию: $\overline{X} \lor (X \lor Y \lor Z)$
5. $\overline{X} \lor X = 1$, значит выражение равно $1$



**Таблица истинности:**

| $X$ | $Y$ | $Z$ | $Y \vee Z$ | $\overline{X}$ | $\overline{X} \to Y$ | $(\overline{X} \to Y) \vee Z$ | $X \to (Y \vee Z)$ | Итог: $X \to (Y \vee Z) \vee ((\overline{X} \to Y) \vee Z)$ |
|:---:|:---:|:---:|:----------:|:------------:|:--------------------:|:-----------------------------:|:------------------:|:--------------------------------------------------------:|
| 0   | 0   | 0   | 0          | 1            | 0                    | 0                             | 1                  | 1                                                      |
| 0   | 0   | 1   | 1          | 1            | 0                    | 1                             | 1                  | 1                                                      |
| 0   | 1   | 0   | 1          | 1            | 1                    | 1                             | 1                  | 1                                                      |
| 0   | 1   | 1   | 1          | 1            | 1                    | 1                             | 1                  | 1                                                      |
| 1   | 0   | 0   | 0          | 0            | 1                    | 1                             | 0                  | 1                                                      |
| 1   | 0   | 1   | 1          | 0            | 1                    | 1                             | 1                  | 1                                                      |
| 1   | 1   | 0   | 1          | 0            | 1                    | 1                             | 1                  | 1                                                      |
| 1   | 1   | 1   | 1          | 0            | 1                    | 1                             | 1                  | 1                                                      |


Ответ: ***1 (тождественно истинно)***

---




