# Questão 2.33

Converta cada uma das equações booleanas do exercício 2.30 em uma tabela-verdade.

---

## a) Função Booleana

\[
F(a, b, c) = a'bc + ab
\]

---

##  Tabela Verdade

| a | a' | b | c | a’bc | ab | F |
|---|----|---|---|------|----|---|
| 0 | 1  | 0 | 0 | 0 | 0 | 0 |
| 0 | 1  | 0 | 1 | 0 | 0 | 0 |
| 0 | 1  | 1 | 0 | 0 | 0 | 0 |
| 0 | 1  | 1 | 1 | 1 | 0 | 1 |
| 1 | 0  | 0 | 0 | 0 | 0 | 0 |
| 1 | 0  | 0 | 1 | 0 | 0 | 0 |
| 1 | 0  | 1 | 0 | 0 | 1 | 1 |
| 1 | 0  | 1 | 1 | 0 | 1 | 1 |

---

- **a’bc = 1** se **a = 0**, **b = 1** e **c = 1**.  
- **ab = 1** se **a = 1** e **b = 1**.

A saída **F = 1** se qualquer um dos termos for **1**.

###  Explicação 

A função está na forma de **Soma de Produtos**, ou seja, cada termo representa uma condição específica para ativar a saída.  
Sempre que **qualquer uma das condições** for satisfeita, a porta **OU** final garante que a saída **F** seja igual a 1.  
Caso nenhuma das combinações gere valor 1 nos termos intermediários, a saída permanece em 0.

---

## b) Função Booleana

\[
F(a, b, c) = a'b
\]

---

##  Tabela Verdade

| a | a' | b | c | F |
|---|----|---|---|---|
| 0 | 1  | 0 | 0 | 0 |
| 0 | 1  | 0 | 1 | 0 |
| 0 | 1  | 1 | 0 | 1 |
| 0 | 1  | 1 | 1 | 1 |
| 1 | 0  | 0 | 0 | 0 |
| 1 | 0  | 0 | 1 | 0 |
| 1 | 0  | 1 | 0 | 0 |
| 1 | 0  | 1 | 1 | 0 |

---

só importa **a** e **b**.  

A saída **F = 1** apenas quando **a’ = 1** (ou seja, **a = 0**) e **b = 1**.

###  Explicação

Embora a função possua três variáveis, o valor de **c não influencia** o resultado final.  
Isso ocorre porque **c não aparece na equação booleana**, logo qualquer variação nessa entrada não altera a saída.  
Na prática, o circuito pode ser implementado apenas com **uma porta NOT** (para gerar \(a'\)) e **uma porta AND**.
