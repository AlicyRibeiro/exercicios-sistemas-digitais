# Questão 2.34

Converta cada uma das seguintes equações booleanas em uma tabela-verdade.

---

## a) Função Booleana

F(a, b, c) = a’ + bc’

---

##  Tabela Verdade

| a | a’ | b | c | c’ | bc’ | F |
|---|----|---|---|----|-----|---|
| 0 | 1  | 0 | 0 | 1  | 0 | 1 |
| 0 | 1  | 0 | 1 | 0  | 0 | 1 |
| 0 | 1  | 1 | 0 | 1  | 1 | 1 |
| 0 | 1  | 1 | 1 | 0  | 0 | 1 |
| 1 | 0  | 0 | 0 | 1  | 0 | 0 |
| 1 | 0  | 0 | 1 | 0  | 0 | 0 |
| 1 | 0  | 1 | 0 | 1  | 1 | 1 |
| 1 | 0  | 1 | 1 | 0  | 0 | 0 |

---

A equação diz que a saída **F** é verdadeira (**1**) se **a for falso (a')**  
**OU** se (**b for verdadeiro E c for falso**).

A saída **F** será a soma (**OU**) da coluna **a'** com a coluna **bc'**.  
**F = 1** se o valor em **a'** for **1** **OU** se o valor em **bc'** for **1**.

---

## b) Função Booleana

F(a, b, c) = (ab)’ + ac’ + bc

---

## Tabela Verdade

| a | b | c | c’ | ab | (ab)’ | ac’ | bc | F |
|---|---|---|----|----|-------|-----|----|---|
| 0 | 0 | 0 | 1 | 0 | 1 | 0 | 0 | 1 |
| 0 | 0 | 1 | 0 | 0 | 1 | 0 | 0 | 1 |
| 0 | 1 | 0 | 1 | 0 | 1 | 0 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 1 | 0 | 0 | 1 | 0 | 0 | 1 |
| 1 | 1 | 0 | 1 | 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 | 1 | 0 | 0 | 1 | 1 |

---

A equação é uma soma de três termos.  
A saída **F** será **1** se **(ab)’** for **1**, **OU** se **ac’** for **1**, **OU** se **bc** for **1**.

A saída **F** é a soma (**OU**) das colunas **(ab)’**, **ac’** e **bc**.  
Se qualquer um desses termos for **1**, **F** será **1**.
