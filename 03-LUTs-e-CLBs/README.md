# Conteúdo: Controle e Datapath

O foco deste bloco é o estudo da **integração entre Bloco de Controle e Datapath**, abordando desde análises temporais básicas até o projeto e a decomposição de sistemas digitais utilizando **máquinas de estados**, **tabelas lookup (LUTs)** e fluxo de dados controlado, com base na obra de **Frank Vahid**.

**Este diretório contém a continuação da primeira lista de exercícios de Sistemas Digitais, organizada separadamente devido ao volume e à complexidade das questões, mantendo total correspondência com o bloco anterior.**

---

## 1. Análise Temporal: Período e Frequência

**Questões:** 3.1 a 3.3  

Estudo da relação entre **frequência**, **período de clock** e comportamento temporal de sistemas síncronos.

**Destaque:**  
Conversão entre frequência e período, fundamentais para o correto funcionamento de circuitos sequenciais e sistemas controlados por clock.

---

## 2. Máquinas de Estados Finitos (FSM) e Bloco de Controle

**Questões:** 3.27 a 3.30, 3.39, 3.44 a 3.45  

Projeto e análise de **blocos de controle baseados em FSM**, incluindo:

- Definição de **estados**, **transições** e **sinais de controle**
- Inclusão de sinais de **reset**
- Análise de **diagramas de tempo**
- Geração de sequências, como **código Gray**
- Integração do controle com circuitos lógicos

---

## 3. Integração entre Controle e Datapath

**Questões:** 5.1 a 5.3, 5.6 a 5.11, 5.15  

Análise da separação funcional entre:

- **Datapath**: responsável pelo fluxo e processamento dos dados
- **Bloco de Controle**: responsável pela geração dos sinais de comando

**Destaque:**  
Estudo da interação entre registradores, multiplexadores, unidades lógicas e sinais de controle em sistemas digitais estruturados.

---

## 4. Decomposição Funcional e Uso de LUTs

**Questões:** 5.18, 5.19, 5.22 a 5.23, 6.32, 6.33, 6.39  

Implementação de funções lógicas e sistemas de controle utilizando **tabelas lookup (LUTs)**:

- Decomposição de funções com múltiplas variáveis
- Uso de LUTs de **3 entradas e 2 saídas**
- Conexões customizadas entre LUTs
- Implementações em cascata (*ripple*)
- Comparadores, funções compostas e lógica combinacional avançada

---

##  Resumo Técnico dos Conceitos Trabalhados

| Tópico | Conceitos Envolvidos |
|------|----------------------|
| Análise Temporal | Período, frequência, clock |
| Controle | FSM, estados, transições |
| Datapath | Registradores, MUX, fluxo de dados |
| Integração | Controle + Datapath |
| Implementação | LUTs, decomposição lógica, cascata |

---

##  Simulações

Algumas resoluções incluem arquivos de simulação que podem ser validados e executados nos softwares:

- **Digital**
- **Logisim**

Os arquivos `.dig` ou `.circ` encontram-se organizados na subpasta:

`/simulações`
