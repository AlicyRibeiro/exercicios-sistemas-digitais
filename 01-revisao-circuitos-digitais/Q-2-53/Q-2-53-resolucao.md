## Seção 2.7: O processo de projeto lógico combinacional

### Questão 2.53

Um museu tem três salões, cada um com um sensor de movimento (**m0, m1 e m2**) que fornece uma saída **1** quando é detectado algum movimento. À noite, a única pessoa no museu é o guarda da segurança que caminha de salão em salão. Crie um circuito que soa um alarme (colocando a sua saída **A** em **1**) apenas quando, em algum momento, um movimento é detectado em mais de um salão, isto é, em dois ou três salões, significando que deve haver um ou mais intrusos no museu. Comece com uma tabela-verdade.

---

### Variáveis de entrada

- **m2**: Sensor do Salão 2  
- **m1**: Sensor do Salão 1  
- **m0**: Sensor do Salão 0  

O valor será **1** se houver movimento e **0** se não houver.

---

### Variável de saída

Tem um alarme como saída.

- **A**: Alarme  

O valor será **1** (alarme soa) se movimento for detectado em mais de um salão (ou seja, em dois ou três salões ao mesmo tempo).  
O valor será **0** (alarme silencioso) se houver movimento em apenas um salão (o guarda) ou em nenhum salão.

---

### Tabela verdade do Circuito

| m2 | m1 | m0 | sensores ativos | A - saída |
|----|----|----|-----------------|-----------|
| 0  | 0  | 0  | 0               | 0         |
| 0  | 0  | 1  | 1               | 0         |
| 0  | 1  | 0  | 1               | 0         |
| 0  | 1  | 1  | 2               | 1         |
| 1  | 0  | 0  | 1               | 0         |
| 1  | 0  | 1  | 2               | 1         |
| 1  | 1  | 0  | 2               | 1         |
| 1  | 1  | 1  | 3               | 1         |

---

### Obtendo a Expressão Booleana

Utilizando o método da **"Soma de Produtos"**, pegando todas as linhas onde a saída **A** é **1**.

- Linha 4: m2=0, m1=1, m0=1 → Termo: `m2'm1m0`  
- Linha 6: m2=1, m1=0, m0=1 → Termo: `m2m1'm0`  
- Linha 7: m2=1, m1=1, m0=0 → Termo: `m2m1m0'`  
- Linha 8: m2=1, m1=1, m0=1 → Termo: `m2m1m0`  

A expressão completa é a soma (OU) desses termos:

A = m2'm1m0 + m2m1'm0 + m2m1m0' + m2m1m0


---

### Simplificando a Expressão

Dada a expressão obtida é possível simplificá-la usando as regras da Álgebra Booleana para criar um circuito mais eficiente.

1. Reorganizado e usado a propriedade **X + X = X** para repetir o último termo:  

    A = (m2'm1m0 + m2m1m0) + (m2m1'm0 + m2m1m0) + (m2m1m0' + m2m1m0)


2. Colocando os termos comuns em evidência em cada par:  

    A = m1m0(m2' + m2) + m2m0(m1' + m1) + m2m1(m0' + m0)


3. Sabendo que **X' + X = 1**, os termos entre parênteses desaparecem:  

    A = m1m0(1) + m2m0(1) + m2m1(1)


4. A expressão simplificada final é:  

    A = m1m0 + m2m0 + m2m1



Essa expressão é muito mais simples e diz logicamente:  
> "O alarme soa se houver movimento nos salões 1 E 0, OU nos salões 2 E 0, OU nos salões 2 E 1".

Isso cobre perfeitamente a condição de **"movimento em pelo menos dois salões"**.

---

### Circuito Lógico
