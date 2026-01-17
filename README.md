# 🚘 Auto Brilho - Smart Quoting Web App

> **Aplicação web para estética automotiva com sistema de pré-orçamento dinâmico e integração via WhatsApp API.**

![Badge Status](http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge)
![Badge Tech](http://img.shields.io/static/v1?label=TECH&message=JAVASCRIPT%20ES6&color=BLUE&style=for-the-badge)

## 💻 Sobre o Projeto (Business Logic)

O **Auto Brilho Web App** não é apenas uma landing page institucional. Ele foi projetado para resolver um gargalo comum em prestadores de serviço: o tempo gasto na triagem inicial de clientes.

A aplicação implementa um funil de vendas onde o usuário "monta" seu pacote de serviços visualmente. O sistema processa essas escolhas e gera um **payload estruturado** (mensagem de texto formatada), que é enviado diretamente para o WhatsApp do vendedor, entregando um lead qualificado e acelerando o fechamento.

---

## ⚙️ Engenharia & Funcionalidades

### 1. Gerador de Orçamento Dinâmico (Algorithm)
Diferente de formulários estáticos, o sistema utiliza lógica de concatenação de strings em tempo real.
- **Input:** O usuário seleciona Marca, Ano, Local e Serviços (Checkbox/Radio).
- **Processamento:** Um *event listener* monitora alterações no DOM, captura os valores, aplica formatação Markdown (negrito/quebras de linha) e atualiza a prévia visual instantaneamente.
- **Output:** Geração de Deep Link para API do WhatsApp (`wa.me/?text=...`).

### 2. Arquitetura Baseada em Dados (Vanilla JS Components)
Para garantir manutenibilidade e escalabilidade, o conteúdo não é "hard-coded" no HTML.
Utilizei estruturas de dados (Arrays de Objetos JSON) para armazenar serviços, depoimentos e galeria.
- **Exemplo:** `const DADOS_SERVICOS = [...]` alimenta a seção de serviços.
- **Benefício:** Para adicionar um novo serviço, basta incluir um objeto no Array, sem tocar no HTML.

### 3. SEO & Performance
- **Schema.org:** Implementação de JSON-LD (`@type": "AutomotiveBusiness"`) para indexação rica no Google.
- **Lazy Loading:** Otimização no carregamento de imagens da galeria.

### 4. UX/UI Interativo
- **Comparador Antes/Depois:** Slider interativo implementado com JavaScript puro para demonstrar resultados de polimento.
- **Mobile First:** Menu hambúrguer responsivo e áreas de toque otimizadas.

---

## 🛠️ Tecnologias

- **Core:** HTML5 Semântico, CSS3 (Variables, Flexbox, Grid), JavaScript (ES6+).
- **Integração:** WhatsApp URL Scheme API.
- **Assets:** Ícones SVG otimizados (injetados via JS para performance).

---

## 🚀 Como Executar

1. Clone o repositório:
```bash
git clone [https://github.com/GustavoCazzine/auto-brilho-app.git](https://github.com/GustavoCazzine/auto-brilho-app.git)
