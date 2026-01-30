# Questão 2.34

Converta cada uma das seguintes equações booleanas em uma tabela-verdade.

---

## c) Função Booleana

F(a, b, c) = ab + ac + ab’c’ + c’

---

##  Tabela Verdade

| a | b | b’ | c | c’ | ab | ac | ab’c’ | F |
|---|---|----|---|----|----|----|-------|---|
| 0 | 0 | 1  | 0 | 1  | 0  | 0  | 1     | 1 |
| 0 | 0 | 1  | 1 | 0  | 0  | 0  | 0     | 0 |
| 0 | 1 | 0  | 0 | 1  | 0  | 0  | 0     | 1 |
| 0 | 1 | 0  | 1 | 0  | 0  | 0  | 0     | 0 |
| 1 | 0 | 1  | 0 | 1  | 0  | 0  | 1     | 1 |
| 1 | 0 | 1  | 1 | 0  | 0  | 1  | 0     | 1 |
| 1 | 1 | 0  | 0 | 1  | 1  | 0  | 0     | 1 |
| 1 | 1 | 0  | 1 | 0  | 1  | 1  | 0     | 1 |

---

A equação é uma soma de quatro termos.  
A saída **F** será **1** se qualquer um destes termos for **1**.

---

## d) Função Booleana

F(a, b, c, d) = a’bc + d’

---

##  Tabela Verdade

| a | b | c | d | a’ | d’ | a’bc | F |
|---|---|---|---|----|----|------|---|
| 0 | 0 | 0 | 0 | 1  | 1  | 0 | 1 |
| 0 | 0 | 0 | 1 | 1  | 0  | 0 | 0 |
| 0 | 0 | 1 | 0 | 1  | 1  | 0 | 1 |
| 0 | 0 | 1 | 1 | 1  | 0  | 0 | 0 |
| 0 | 1 | 0 | 0 | 1  | 1  | 0 | 1 |
| 0 | 1 | 0 | 1 | 1  | 0  | 0 | 0 |
| 0 | 1 | 1 | 0 | 1  | 1  | 1 | 1 |
| 0 | 1 | 1 | 1 | 1  | 0  | 1 | 1 |
| 1 | 0 | 0 | 0 | 0  | 1  | 0 | 1 |
| 1 | 0 | 0 | 1 | 0  | 0  | 0 | 0 |
| 1 | 0 | 1 | 0 | 0  | 1  | 0 | 1 |
| 1 | 0 | 1 | 1 | 0  | 0  | 0 | 0 |
| 1 | 1 | 0 | 0 | 0  | 1  | 0 | 1 |
| 1 | 1 | 0 | 1 | 0  | 0  | 0 | 0 |
| 1 | 1 | 1 | 0 | 0  | 1  | 0 | 1 |
| 1 | 1 | 1 | 1 | 0  | 0  | 0 | 0 |

---

A função tem **4 variáveis** (**a, b, c, d**), portanto, a tabela-verdade terá  
**2⁴ = 16 linhas**.

A lógica é:  
**F = 1** se (**a for falso E b for verdadeiro E c for verdadeiro**) **OU** se **d for falso**.

Note que se **d = 0**, então **d’ = 1**, e a saída **F** será automaticamente **1**, independentemente dos valores de **a**, **b** e **c**.  
Isso já resolve metade da tabela.
