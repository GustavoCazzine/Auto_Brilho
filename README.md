# 🚘 Auto Brilho - Smart Quoting System

> **Web App de agendamento e pré-orçamento automotivo com geração dinâmica de mensagens via WhatsApp API.**

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge)
![Badge Tech](http://img.shields.io/static/v1?label=TECH&message=JAVASCRIPT%20DOM&color=BLUE&style=for-the-badge)

---

## 💻 O Projeto (The Engineering Problem)

Muitas estéticas automotivas sofrem com um gargalo no atendimento digital: o cliente envia um "Oi" no WhatsApp, e o atendente precisa gastar tempo perguntando modelo do carro, ano e serviços desejados antes de passar um preço.

O **Auto Brilha Smart System** resolve isso invertendo o fluxo. Ele atua como um funil de entrada, coletando e estruturando os dados **antes** do contato humano.

---

## ⚙️ Funcionalidades & Lógica

### 1. Geração Dinâmica de Payload (WhatsApp API)
O sistema não apenas envia um link. Ele constrói uma mensagem de texto complexa baseada nas variáveis de estado da aplicação.
- **Input:** Usuário seleciona *Veículo*, *Ano*, *Local de Atendimento* e *Serviços (Checkbox)*.
- **Processamento:** Um algoritmo em JavaScript monitora o DOM, concatena as strings selecionadas e formata a mensagem com quebras de linha e negrito (Markdown do WhatsApp).
- **Output:** A URL final aciona a API do WhatsApp já com o texto pronto para envio.

### 2. Feedback Visual em Tempo Real (DOM Manipulation)
A seção "Prévia da Mensagem" atualiza instantaneamente a cada clique do usuário, garantindo que ele saiba exatamente o que será enviado.
*(Veja a lógica no arquivo `script.js`)*.

---

## 📸 Screenshots

### Interface de Seleção e Prévia Dinâmica
![Interface de Orçamento](caminho-para-sua-imagem-do-orcamento.png)
*O usuário monta o pacote e o sistema gera o texto automaticamente à direita.*

### Landing Page (Dark Mode & UX)
![Landing Page](caminho-para-sua-imagem-da-lp.png)
*Design focado em conversão e hierarquia visual.*

---

## 🛠️ Tecnologias Utilizadas

- **Core:** `HTML5`, `CSS3` (Flexbox/Grid), `JavaScript` (ES6+).
- **Integration:** WhatsApp URL Scheme API.
- **Design:** UI Dark Mode com foco em alto contraste (Neon/Blue).

---

## 🚀 Como testar

1. Clone o repositório.
2. Abra o arquivo `index.html` no seu navegador.
3. Simule um orçamente selecionando "Lavagem Detalhada" e "Vitrificação".
4. Observe a mensagem sendo construída em tempo real.

---

### 👨‍💻 Autor

**Gustavo Cazzine**
*Software Engineering Student | Java Backend Focus*

[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/gustavo-cazzine/)](https://www.linkedin.com/in/gustavo-cazzine/)
