# Atividade 3: Estratégia e Projeto de Testes do LocalEats

## 1. Identificação

**Turma:** ADS5M26-2C  
**Equipe:** Gabriele de Q. Lapischies   
**Data:** 26/09/2026

### Integrantes

| Nome | Usuário no GitHub |
|---|---|
| Gabriele de Q. Lapischies | @GabrieleQL |

**Elemento de Competência:** Planejar e projetar testes selecionando técnicas adequadas.

**Aplicação:** <https://local-eats-unisenac.vercel.app/>

---

## 2. Tarefa 1: Planejamento dos testes

### 2.1 Objetivo dos testes

A equipe pretende verificar se os usuários possuem um limite de pratos a ser pedido em um pedido.

### 2.2 Escopo

#### Funcionalidades incluídas

| Integrante | Funcionalidade incluída | O que será verificado |
|---|---|---|
| Gabriele | Realizar Pedido | Se o usuário possue um limite de pratos a ser pedido em um pedido | 

#### Funcionalidade não incluída

| Funcionalidade não incluída | Justificativa |
|---|---|
| Favoritar | Não faz parte do fluxo de realizar pedido  |

### 2.3 Abordagem

| Item | Decisão da equipe | Justificativa |
|---|---|---|
| Níveis de teste | Unitário | Deverá ser calculado a quantidade selecionada do mesmo prato em um pedido |
| Tipos de teste | Não Funcional | Verifica a capacidade de interação   |
| Perspectiva caixa-preta ou caixa-branca | Caixa-Preta | Será visto pela ótica do usuário ao tentar selecionar um número x de um mesmo prato |
| Técnicas de teste | Valores-Limite | Deve-se possuir um valor mínimo e máximo para a quantidade de pratos a ser selecionados em um pedido |

### 2.4 Ambiente e responsabilidades

| Item | Definição |
|---|---|
| Ambiente necessário | Logado na aplicação [LocalEats](https://local-eats-unisenac.vercel.app/) |
| Responsáveis pelo planejamento | Gerente de Projetos |
| Responsáveis pela especificação dos casos | Analista de Sistemas ou Negócios |
| Responsáveis pela futura execução | Usuário |

### 2.5 Critérios

| Critério | Definição da equipe |
|---|---|
| Entrada | Usuário localizado na página de algum restaurante já logado na aplicação |
| Saída | Usuário selecionar uma quantidade de pratos dentro do valor limite em um pedido |
| Suspensão | Número de pratos indisponíveis para o pedido |

---

## 3. Tarefa 2: Riscos e técnicas de teste

### 3.1 Análise dos riscos  

| ID | Integrante | Funcionalidade | Risco | Consequência | Probabilidade | Impacto | Prioridade | Justificativa |
|---|---|---|---|---|:---:|:---:|:---:|---|
| R01 | Gabriele | Realizar Pedido | O usuário tentar selecionar uma quantidade acima do valor limite disponível por pedido | O restaurante, por não haver a quantidade exigida pelo usuário | Média | Alto | Alta | A consequência prejudica ao restaurante que oferece o seu cardápio por falta de igredientes ou estoque | 

### 3.2 Aplicação das técnicas 

#### Análise do integrante 1

**Integrante:** Gabriele  
**Funcionalidade:** Realizar Pedido  
**Risco relacionado:** R01  
**Técnica escolhida:** Análise de valor limite

**Por que a técnica foi escolhida:**  
A técnica foi escolhida por possuir nela a ideia de ter um limite inferior e superior.

**Aplicação da técnica:**  
Um pedido pode possuir de 1 a 10 quantidade de um mesmo prato. 
Valores próximos aos limites:  
- 0 qtd; 
- 1 qtd; 
- 2 qtd;  
- 9 qtd;
- 10 qtd;  
- 11 qtd;  

**Casos derivados:**  
- CT01: Tentar realizar um pedido com 0 quantidade de um mesmo prato;  
- CT02: Realizar um pedido com 7 quantidades de um mesmo prato;  
- CT03: Tentar realizar um pedido com 11 quantidades de um mesmo prato.

---

## 4. Tarefa 3: Casos de teste e rastreabilidade

### 4.1 Casos de teste

### CT01: Impedir finalização de pedido com zero quantidade de pratos selecionados

**Integrante responsável:** Gabriele  
**Funcionalidade:** Realizar Pedido  
**Risco ou requisito relacionado:** R01  
**Técnica utilizada:** Análise de valor limite

**Pré-condição:**  
O usuário estar logado e selecionar o botão "Finalizar Pedido" sem adicionar um prato.

**Dados de entrada:**  
Não se aplica.

**Passos:**

1. Acessar um restaurante
2. Selecionar o botão "Finalizar Pedido"  

**Resultado esperado:**  
A plataforma não realiza o pedido e informa ao usuário que ele deve informar pelo menos um prato.

---

### CT02: Finalizar pedido com uma quantidade de pratos dentro do limite estabelecido

**Integrante responsável:** Gabriele  
**Funcionalidade:** Realizar Pedido  
**Risco ou requisito relacionado:** R01  
**Técnica utilizada:** Análise de valor limite

**Pré-condição:**  
O usuário estar logado, selecionar escolher um restaurante, escolher um prato e informar a quantidade desejada.  

**Dados de entrada:**  
Quantidade de pratos do pedido: 3 quantidades

**Passos:**

1. Acessar um restaurante
2. Selecionar o prato  
3. Informar a quantidade  
4. Selecionar o botão "Finalizar Pedido"

**Resultado esperado:**  
A plataforma finaliza o pedido e o usuário pode visualizar os detalhes do seu pedido. 

---  

### CT03: Impedir finalização de pedido com uma quantidade de pratos selecionados acima do valor limite

**Integrante responsável:** Gabriele  
**Funcionalidade:** Realizar Pedido  
**Risco ou requisito relacionado:** R01  
**Técnica utilizada:** Análise de valor limite

**Pré-condição:**  
O usuário estar logado, selecionar escolher um restaurante, escolher um prato e informar uma quantidade acima de 10.  

**Dados de entrada:**  
Quantidade de pratos do pedido: 11 quantidades

**Passos:**

1. Acessar um restaurante
2. Selecionar o prato  
3. Informar a quantidade  
4. Selecionar o botão "Finalizar Pedido"

**Resultado esperado:**  
A plataforma não finaliza o pedido e notifica ao usuário que ele só pode selecionar até 10 quantidades daquele prato por pedido.

---

### 4.2 Matriz de rastreabilidade

| Integrante | Funcionalidade | Risco ou requisito | Técnica utilizada | Casos de teste |
|---|---|---|---|---|
| Gabriele | Realizar Pedido | R01 | Análise de valor limite | CT01, CT02 e CT03 |  

---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
Gemini

**Como foi utilizada:**  
Apenas para para apoio.

**Uma sugestão que precisou ser alterada ou rejeitada:**  
Lidas e analisadas com conhecimentos já obtidos.

**Como as respostas foram verificadas:**  
Como conhecimentos já obtidos.