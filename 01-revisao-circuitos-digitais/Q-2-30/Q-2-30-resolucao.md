# Questão 2.30

Converta a seguinte equação booleana para um **circuito digital**:

\[
F(a, b, c) = a'bc + ab
\]

Essa equação indica que a saída **F = 1 (verdadeira)** quando **pelo menos uma** das condições abaixo é satisfeita:

- \(a = 0\), \(b = 1\) e \(c = 1\)  
- \(a = 1\) e \(b = 1\)

Ou seja, a função representa uma operação **OU** entre dois termos **AND**.

---

##  Tabela Verdade

| a | b | c | a' | a'bc | ab | F |
|---|---|---|----|------|----|---|
| 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 0 | 0 | 0 |
| 0 | 1 | 1 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 0 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 0 | 0 | 1 | 1 |


