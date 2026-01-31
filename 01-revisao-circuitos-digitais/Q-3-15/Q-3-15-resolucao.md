## Seção 3.2: Armazenando um bit - Flip-Flops

### Questão 3.15

Compare os comportamentos de um latch D e um flip-flop D complementado o diagrama de tempo da Fig. 3.78. Assuma que cada dispositivo armazena inicialmente um 0. Dê uma breve explicação do comportamento de cada dispositivo.

![Circuito da Questão 2.30 - item a](figuras/Questão3.15.jpeg)

---

## Princípios Fundamentais (As "Regras do Jogo")

Antes de seguir a linha do tempo, precisa-se lembrar as duas regras de ouro:

### Latch D (Sensível ao Nível)

- Quando **C = 1** (nível alto): O latch é "transparente". A saída **Q** imediatamente copia e segue a entrada **D**.  
- Quando **C = 0** (nível baixo): O latch "trava". A saída **Q** mantém o último valor que tinha.

### Flip-Flop D (Sensível à Borda)

- A saída **Q** só pode mudar no instante exato da **borda de subida de C** (quando C vai de 0 para 1).  
- Nesse instante, ele "fotografa" o valor de **D** e o armazena.  
- Em todos os outros momentos, **Q** mantém seu valor, ignorando **D**.

---

## Diagrama Completo

![Circuito da Questão 2.30 - item a](figuras/Diagrama.jpeg)

---

## Análise Passo a Passo do Diagrama de Tempo

Percorrendo o tempo da esquerda para a direita, focando nas bordas do clock.

---

### Primeiro Pulso de Clock

**Na 1ª borda de subida de C:**

- **Latch:** C sobe para 1, o latch se torna transparente. D está em 1, então Q(latch) sobe para 1.  
- **Flip-Flop:** Vê a borda de subida e amostra D. D está em 1, então Q(FF) sobe para 1.

**Enquanto C está em 1:**

- **Latch:** A entrada D desce para 0. Como o latch é transparente, Q(latch) imediatamente segue e desce para 0.  
- **Flip-Flop:** Ignora a mudança em D porque não é uma borda de subida. Q(FF) continua em 1.

**Na 1ª borda de descida de C:**

- **Latch:** C desce para 0, o latch trava. No momento da descida, D estava em 0, então Q(latch) trava em 0.  
- **Flip-Flop:** A borda de descida não tem efeito. Q(FF) continua em 1.

---

### Segundo Pulso de Clock

**Na 2ª borda de subida de C:**

- **Latch:** C sobe para 1, torna-se transparente. D está em 1, então Q(latch) sobe de 0 para 1.  
- **Flip-Flop:** Vê a borda de subida e amostra D. D está em 1. Q(FF) já estava em 1, então ele permanece em 1.

**Enquanto C está em 1:**  
D permanece em 1, então Q(latch) também permanece em 1. Q(FF) não muda.

**Na 2ª borda de descida de C:**

- **Latch:** C desce, o latch trava. D está em 1, então Q(latch) trava em 1.  
- **Flip-Flop:** Continua mantendo o valor 1.

---

### Terceiro Pulso de Clock

**Na 3ª borda de subida de C:**

- **Latch:** C sobe para 1, transparente. D está em 0, então Q(latch) desce de 1 para 0.  
- **Flip-Flop:** Vê a borda de subida e amostra D. D está em 0, então Q(FF) desce de 1 para 0.

**Enquanto C está em 1:**

- **Latch:** A entrada D sobe para 1. Sendo transparente, Q(latch) imediatamente segue e sobe para 1.  
- **Flip-Flop:** Ignora a mudança em D. Q(FF) contínua em 0. (Outro ótimo exemplo da diferença!)

---

O padrão continua assim pelo resto do diagrama.

Enquanto a entrada **C (clock)** for 1, o **latch D** irá armazenar o valor de **D** (após um pequeno atraso de porta).  
O **flip-flop D** só irá armazenar o valor de **D** na borda de subida de **C** (após um pequeno atraso de porta).

Enquanto a entrada **C (clock)** for 1, o **latch D** irá armazenar o valor de **D** (após um pequeno atraso de porta).  
O **flip-flop D** só irá armazenar o valor de **D** na borda de subida de **C** (após um pequeno atraso de porta).

