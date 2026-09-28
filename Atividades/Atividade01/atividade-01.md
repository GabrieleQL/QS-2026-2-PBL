# Atividade 1: Fundamentos e Características da Qualidade no LocalEats

## 1. Identificação

**Turma:** ADS5M26-2C  
**Equipe:** Gabriele de Q. Lapischies   
**Data:** 26/09/2026

### Integrantes

| Nome | Usuário no GitHub |
|---|---|
| Gabriele de Q. Lapischies | @GabrieleQL |

**Elemento de Competência:** Compreender os fundamentos de qualidade de software e sua aplicação no desenvolvimento de sistemas.

**Aplicação:** <https://local-eats-unisenac.vercel.app/>

---

## 2. Tarefa 1: Fundamentos da qualidade

### 2.1 Necessidades explícitas e implícitas

| Tipo | Necessidade | Interessado | Consequência se não for atendida |
|---|---|---|---|
| Explícita | Fazer Pedido | Usuário | O usuário não poderá realizar o pedido na plataforma |
| Explícita | Consultar Pedido | Usuário | O usuário não poderá consultar o pedido realizado na plataforma |
| Implícita | Destacar Navegação de Abas | UX/UI | O usuário pode ficar perdido com relação a qual aba da plataforma ele está localizado |
| Implícita | Destacar Botões | UX/UI | O usuário pode se confundir ao selecionar um botão específico |

### 2.2 Questão sobre os fundamentos da qualidade

**Um sistema que implementa todas as funcionalidades explicitamente solicitadas pode, ainda assim, apresentar baixa qualidade? Justifiquem utilizando pelo menos uma necessidade implícita identificada pela equipe.**

Sim. Mesmo que as funcionalidades explícitas sejam implementadas, isso não garante uma alta qualidade para a plataforma. As necessidades implícitas auxiliam a experiência do usuário na plataforma, como por exemplo, o usuário saber que está na aba "Meus Pedidos" por causa da navegação estar destacada em negrito ou em outra cor ou tamanho.

---

## 3. Tarefa 2: Exploração da aplicação

| Integrante | Funcionalidade | O que foi realizado | O que foi observado | Evidência |
|---|---|---|---|---|
| Gabriele | Entrar no Sistema | O usuário informa email 'marcosfm@gmail.com' e senha '123456', usuário autenticado. O usuário informa email 'marcosfm@gmail.com' e senha '123457', credenciais inválidas | O usuário informou senha errada. | [ver evidência](Evidencias/marcos-login-senh-invalida.png) |


---

## 4. Tarefa 3: Requisitos e características de qualidade

| Integrante | Requisito de Qualidade | Característica ou subcaracterística | Justificativa | Como avaliar |
|---|---|---|---|---|
| Gabriele | Segurança | Autenticidade | Pois tem a capacidade de provar que a identidade de um usuário é verdadeira ou não | Observar se, ao informar email e senha, ele conseguirá acessar a plataforma, caso contrário, receberá uma notificação de credencial inválida  |


---

## 5. Uso de inteligência artificial

**Ferramenta utilizada:**  
Gemini

**Como foi utilizada:**  
Apenas para tirar dúvidas de nomes técnicos.

**Como as respostas foram verificadas:**  
Lidas e verificadas/comparadas com o material disponível pelo professor.