## Questão 2.55

Considere a função do alarme de segurança para o museu do Exercício 2.53, mas para um museu com 10 salões. Uma tabela-verdade não é um bom ponto de partida (linha demais), nem uma equação que descreve quando o alarme pode ser obtida rapidamente na forma de uma equação. Projete o circuito para um sistema de segurança de 10 salões, projetando o inverso da função e, então, simplesmente acrescentado um inverso antes da saída da função.

---

### Objetivo

Projetar um circuito de alarme **A** para 10 salões (com sensores **m0 a m9**).

---

### Condição do Alarme

O alarme **A** deve ser **1** (ativado) quando o movimento for detectado em mais de um salão (ou seja, **2, 3, ..., ou 10 salões ao mesmo tempo**).

---

### A Dificuldade

Listar todas as combinações em que 2 ou mais sensores estão ativos seria uma tarefa imensa.  
Uma tabela verdade com 10 entradas teria **2 elevado a 10 = 1024 linhas**.

---

### A Estratégia

Conforme instruído, vamos projetar a função inversa, que chama de **A'**.  
Esta função descreve quando o alarme **NÃO** deve soar.  

No final, o alarme **A** será simplesmente a inversão de **A'**.

Se o alarme (**A**) soa para **"mais de um sensor ativo"**, a função inversa (**A'**) será verdadeira quando a condição for **"não mais que um sensor ativo"**. Isso se divide em duas situações muito mais simples:

- **Condição Zero:** Nenhum sensor está ativo (o número de sensores ativos é 0).  
- **Condição Um:** Exatamente um sensor está ativo.

Portanto, a equação lógica para a nossa função inversa é:
    A' = (Nenhum sensor ativo) OU (Exatamente um sensor ativo)


---

### Projetando o Circuito para "Nenhum Sensor Ativo"

Esta condição verifica se todos os sensores estão em 0.

**Lógica da Condição:**  
m0 = 0 E m1 = 0 E m2 = 0 E ... E m9 = 0.

**Equação Booleana:**  
Em álgebra booleana, isso se traduz como:
    F_zero = m0'⋅m1'⋅m2'⋅...⋅m9'


**Implementação do Circuito:**  
Usando o Teorema de De Morgan, esta expressão é equivalente a:
    F_zero = (m0 + m1 + m2 + ... + m9)'


Este circuito é implementado de forma muito eficiente com uma única **porta NOR de 10 entradas**.  
A saída desta porta será **1 somente se todas as 10 entradas forem 0**.

---

### Projetando o Circuito para "Exatamente Um Sensor Ativo"

Esta condição é mais elaborada, pois é uma soma de 10 possibilidades únicas e exclusivas.

**Lógica da Condição:**  
(Apenas m0 está ativo) OU (Apenas m1 está ativo) OU ... OU (Apenas m9 está ativo).

**Equação Booleana:**  
A expressão para **"apenas m0 estar ativo"** é:
    m0⋅m1'⋅m2'⋅...⋅m9'


A função completa para esta condição (**F_um**) é a soma (OU) de todas as 10 possibilidades:
    F_um = (m0⋅m1'⋅...⋅m9') + (m0'⋅m1⋅...⋅m9') + ... + (m0'⋅m1'⋅...⋅m9)


---

### Circuito Lógico

![Circuito da Questão 2.30 - item a](figuras/Questão2.55.png)
