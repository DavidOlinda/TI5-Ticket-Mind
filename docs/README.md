# TICKET MIND

**David Olinda Pomine — [@DavidOlinda](https://github.com/DavidOlinda)**

**Arthur Modesto — [@ArthurModesto1](https://github.com/ArthurModesto1)**

**Bernardo Carvalho — [@bernardocdm](https://github.com/bernardocdm)**

---

Professores:

**Prof. Artur Martins Mol**

**Prof. João Paulo Carneiro Aramuni**

**Prof. Leonardo Vilela Cardoso**

---

_Curso de Engenharia de Software, Campus Coração Eucarístico_

_Instituto de Informática e Ciências Exatas – Pontifícia Universidade Católica de Minas Gerais (PUC MINAS), Belo Horizonte – MG – Brasil_

---

_**Resumo**. O mercado de eventos e ingressos é marcado pela alta rotatividade de ofertas e pela rápida exaustão de lotes, o que faz com que muitos consumidores percam eventos de seu interesse simplesmente por não tomarem conhecimento deles a tempo. Este trabalho apresenta o projeto arquitetural do Ticket Mind, uma plataforma distribuída de recomendação e notificação em tempo real que aprende as preferências do usuário e o alerta assim que um evento ou ingresso compatível com o seu perfil se torna disponível. A arquitetura proposta é composta por um web service REST, clientes web e móvel híbrido construídos sobre um mesmo ecossistema de linguagem, e um middleware de mensageria baseado em canais que sustenta a entrega simultânea de atualizações a múltiplos clientes conectados. O documento detalha os requisitos funcionais e não-funcionais, as restrições e os mecanismos arquiteturais adotados, bem como as justificativas técnicas de cada decisão._

---

## SUMÁRIO

1. [Apresentação](1.apresentacao.md#apresentacao "Apresentação") <br />
   1.1. Problema <br />
   1.2. Objetivos do trabalho <br />
   1.3. Definições e Abreviaturas <br />

2. [Nosso Produto](2.nosso_produto.md#produto "Nosso Produto") <br />
   2.1. Visão do Produto <br />
   2.2. Nosso Produto <br />
   2.3. Personas <br />

3. [Requisitos](3.requisitos.md#requisitos "Requisitos") <br />
   3.1. Requisitos Funcionais <br />
   3.2. Requisitos Não-Funcionais <br />
   3.3. Restrições Arquiteturais <br />
   3.4. Mecanismos Arquiteturais <br />

4. [Modelagem](4.modelagem.md#modelagem "Modelagem e projeto arquitetural") <br />
   4.1. Visão de Negócio <br />
   4.2. Visão Lógica <br />
   4.3. Modelo de dados (opcional) <br />

5. [Wireframes](5.wireframe.md#wireframes "Wireframes") <br />

6. [Avaliação Heuristica](6.avaliacao_heuristica.md#solucao "Projeto da Solução") <br />

7. [Solução](7.solucao.md#solucao "Projeto da Solução") <br />

8. [Avaliação Arquitetura](8.avaliacao_arquitetura.md#avaliacao "Avaliação da Arquitetura") <br />
   8.1. Cenários <br />
   8.2. Avaliação <br />

[Ferramentas](#ferramentas "Ferramentas")<br />

<a name="ferramentas"></a>

# Ferramentas

| Ambiente                  | Plataforma       | Link de Acesso                                         |
| ------------------------- | ---------------- | ------------------------------------------------------ |
| Repositório de código     | GitHub           | https://github.com/DavidOlinda/TI5-Ticket-Mind          |
| Gestão do projeto (Kanban)| GitHub Projects  | _a definir_                                            |
| Hospedagem do front-end   | Vercel           | _a definir_                                            |
| Hospedagem do back-end    | Render           | _a definir_                                            |
| Banco de dados e Realtime | Supabase         | _a definir_                                            |
| Protótipo Interativo      | Figma            | _a definir_                                            |
