## c) Função Booleana


F(a, b, c) = abc + ab + a + b + c


---

##  Tabela Verdade

| a | b | c | abc | ab | F |
|---|---|---|-----|----|---|
| 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 | 0 | 1 |
| 0 | 1 | 0 | 0 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 0 | 1 |
| 1 | 1 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 1 | 1 |

---

A expressão será falsa se todos os termos forem falsos.  

Para qualquer outra combinação de entrada, pelo menos uma das variáveis será **1**.  
Como são termos em **OU**, se qualquer um for **1**, a expressão será **1**.

---

##  Simplificando a Expressão

É possível resolver a questão simplificando a expressão booleana:

F = abc + ab + a + b + c

F = a(bc + b + 1) + b + c  
(colocando a em evidência)

F = a(1) + b + c  
(qualquer coisa somada com 1 resulta em 1)

F = a + b + c  
(regra da identidade: X · 1 = X)


---

###  Tabela Verdade da Expressão Simplificada

| a | b | c | F |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

---

## d) Função Booleana


F(a, b, c) = c'


---

##  Tabela Verdade

| a | b | c | c' | F |
|---|---|---|----|---|
| 0 | 0 | 0 | 1 | 1 |
| 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 0 | 1 | 1 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 0 | 1 | 0 | 0 |
| 1 | 1 | 0 | 1 | 1 |
| 1 | 1 | 1 | 0 | 0 |

---

- Se **c = 0**, a saída **F = 1**  
- Se **c = 1**, a saída **F = 0**
