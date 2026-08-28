# Termo de Abertura de Projeto (TAP) no.: 001

**Nome da empresa:** PUC Minas — Engenharia de Software (Trabalho Interdisciplinar TIS V)

**Data:** 28/08/2026

**Integrantes:**

David Olinda Pomine — [@DavidOlinda](https://github.com/DavidOlinda)
Arthur Modesto — [@ArthurModesto1](https://github.com/ArthurModesto1)
Bernardo Carvalho — [@bernardocdm](https://github.com/bernardocdm)

---

**Professores:**

Prof. Artur Martins Mol
Prof. João Paulo Carneiro Aramuni
Prof. Leonardo Vilela Cardoso

---

_Curso de Engenharia de Software, Campus Coração Eucarístico_

_Instituto de Informática e Ciências Exatas – Pontifícia Universidade Católica de Minas Gerais (PUC MINAS), Belo Horizonte – MG – Brasil_

---

## 1. IDENTIFICAÇÃO DO PROJETO

**1.1 Nome do Projeto:** Ticket Mind

**1.2 Gerente do Projeto:** David Olinda Pomine (Líder / Scrum Master)

**1.3 Cliente do Projeto:** Projeto acadêmico sem parceiro externo. O papel de cliente é exercido pelos professores da disciplina, que atuam como demandantes e avaliadores das entregas. O público-alvo do produto é composto por consumidores de eventos ao vivo, representado no projeto pelas personas descritas na Seção 2 do Documento de Arquitetura.

**1.4 Tipo de Projeto:**

[ ] Manutenção em produto existente
[X] Desenvolvimento de novo produto
[ ] Outro: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**1.5 Objetivo do projeto:**

Desenvolver o Ticket Mind, uma plataforma distribuída de recomendação e notificação em tempo real para o mercado de eventos e ingressos, disponível em ambiente web e móvel. O sistema deve aprender as preferências de cada usuário — artistas, categorias, gêneros e times — e notificá-lo no instante em que surge um evento ou ingresso compatível com o seu perfil.

Do ponto de vista acadêmico, o projeto tem por objetivo aplicar os conceitos de aplicações distribuídas da disciplina TIS V, contemplando comunicação por web service, middleware de mensageria para processamento em tempo real, atendimento concorrente a múltiplos clientes, tratamento de falhas de comunicação, estratégia de testes automatizados e implantação em serviços de nuvem.

**1.6 Benefícios que justificam o projeto:**

- **Para o usuário final:** elimina a necessidade de monitorar manualmente múltiplas plataformas de venda, reduzindo a chance de perder eventos de interesse por desconhecimento ou por tomar ciência da oferta tarde demais.
- **Redução da latência de decisão:** ao notificar em tempo real a abertura de vendas, a queda de preço ou as últimas unidades disponíveis, o sistema amplia a janela útil de compra em um mercado no qual os lotes se esgotam rapidamente.
- **Consolidação da informação:** oferece um ponto único de descoberta para categorias distintas — música, esporte e teatro — hoje dispersas entre diferentes plataformas.
- **Personalização progressiva:** o feedback do usuário sobre as recomendações realimenta o motor de sugestões, tornando as notificações mais aderentes ao seu perfil ao longo do uso.
- **Para a equipe:** consolida na prática competências de arquitetura de aplicações distribuídas, desenvolvimento multiplataforma e gerência ágil de projetos.

**1.7 Qualidade esperada do produto final (requisitos de qualidade):**

A qualidade esperada é definida pelos requisitos não-funcionais RNF001 a RNF011 do Documento de Arquitetura, dos quais se destacam:

- As funcionalidades devem ser expostas por meio de um web service consumido de forma idêntica pelos clientes web e móvel, com paridade das funcionalidades essenciais entre as plataformas;
- As notificações devem ser propagadas aos clientes conectados em tempo real, sem recarregamento manual nem consulta periódica pelo cliente;
- O sistema deve suportar múltiplos clientes conectados simultaneamente, com operações concorrentes sobre a mesma base de eventos, sem inconsistência de dados;
- Cada cliente deve receber apenas as atualizações correspondentes aos seus interesses;
- Falhas de comunicação, timeouts e indisponibilidade de serviços devem ser tratados com políticas de reenvio automático no cliente e no servidor, além de interrupção temporária de chamadas a serviços com falhas recorrentes;
- O sistema deve possuir cobertura de testes unitários, de integração e ponta a ponta, nas plataformas web e móvel;
- A aplicação deve ser implantada em serviços de nuvem de plano gratuito, com deploy automatizado a partir do repositório Git.

## **2. ESCOPO PRELIMINAR E PREMISSAS** |

**2.1 O que será feito (escopo do projeto)**

O escopo do projeto corresponde às funcionalidades priorizadas como **Essenciais** e **Desejáveis** no sequenciador MoSCoW, formalizadas como requisitos funcionais no Documento de Arquitetura:

*Escopo essencial (MVP) — RF001 a RF006:*
- Cadastro e autenticação de usuário;
- Definição e edição do perfil de interesses (artistas, categorias, gêneros e times);
- Listagem e busca de eventos;
- Motor de recomendação de eventos com base no perfil do usuário;
- Notificação em tempo real de eventos compatíveis com o perfil;
- Exibição dos detalhes do evento e direcionamento ao canal oficial de compra.

*Escopo desejável — RF007 a RF009:*
- Notificação de queda de preço e de últimas unidades disponíveis;
- Histórico de eventos visualizados e curtidos;
- Avaliação das recomendações pelo usuário (curtir / não curtir), com refinamento das sugestões futuras.

*Escopo de engenharia e infraestrutura:*
- Web service REST em TypeScript;
- Cliente web em React e cliente móvel híbrido em React Native com Expo;
- Middleware de mensageria em tempo real com filtros de canal;
- Persistência em banco relacional PostgreSQL;
- Políticas de retry, timeout e circuit breaker no cliente e no servidor;
- Suíte de testes unitários, de integração e ponta a ponta (web e móvel);
- Implantação em nuvem com deploy automatizado a partir do repositório Git;
- Documentação de arquitetura e artefatos de gerência mantidos em Markdown no repositório público.

**2.2 O que não será feito no projeto (contra-escopo)**

- **Venda e emissão de ingressos:** o sistema não processa pagamentos, não emite, não valida e não revende ingressos; o usuário é direcionado ao canal oficial de venda do evento;
- **Reserva de ingressos:** o sistema não garante disponibilidade nem realiza qualquer forma de reserva;
- **Integração contratual com plataformas de venda:** não estão previstos acordos comerciais ou integrações oficiais com bilheterias e produtoras;
- **Rede social de eventos:** não serão desenvolvidos perfis públicos, feed social, comentários ou seguidores;
- **Aplicativos nativos separados:** o cliente móvel será exclusivamente híbrido/multiplataforma, a partir de base de código única;
- **Funcionalidades classificadas como Opcionais** no sequenciador MoSCoW (RF010 a RF012 — recomendação para grupos, integração com calendário e compartilhamento social), que somente serão desenvolvidas caso haja folga de prazo após a conclusão do escopo essencial e desejável;
- **Operação em ambiente produtivo com carga real:** a implantação limita-se a serviços de nuvem de plano gratuito, para fins de demonstração acadêmica.

**2.3 Resultados / serviços / produtos a serem entregues**

| **1.** | Documento de Arquitetura de Software (Seções 1 a 8), incluindo Lean Inception, requisitos funcionais e não-funcionais, restrições e mecanismos arquiteturais, modelagem e avaliação da arquitetura pelo método ATAM |
| --- | --- |
| **2.** | Artefatos de gerência de projetos: Termo de Abertura do Projeto, atas de reunião, Product Backlog, backlogs de sprint e relatórios de contribuição semanal |
| **3.** | Aplicação web (React) implantada em serviço de nuvem gratuito |
| **4.** | Aplicação móvel híbrida (React Native + Expo) |
| **5.** | Web service REST (TypeScript) implantado em serviço de nuvem gratuito, com banco de dados PostgreSQL e middleware de mensageria em tempo real |
| **6.** | Suíte de testes automatizados nos níveis unitário, de integração e ponta a ponta |
| **7.** | Protótipo interativo (wireframes) e avaliação heurística de usabilidade |
| **8.** | Apresentação final do projeto e material de divulgação |

**2.4 Condições para início do projeto**

- Definição do tema e da visão de produto, concluída na Sprint 1 por meio da Lean Inception;
- Formação da equipe com a definição dos papéis, incluindo a designação do líder responsável pela gerência do projeto;
- Contas ativas no GitHub para todos os integrantes e aceite do convite do GitHub Classroom;
- Repositório do projeto criado, público e com todos os integrantes adicionados;
- Quadro Kanban configurado no GitHub Projects, com as colunas Product Backlog, Sprint Backlog, Doing e Done;
- Definição da stack tecnológica e das decisões arquiteturais que atendem aos requisitos obrigatórios da disciplina;
- Contas criadas nos serviços de nuvem de plano gratuito previstos para a implantação;
- Aprovação deste Termo de Abertura na reunião de *kickoff*.

## 3. ESTIMATIVA DE PRAZO

**3.1 Prazo previsto (horas):** 306

_Estimativa obtida a partir do calendário da disciplina: 17 semanas de projeto (04/08/2026 a 01/12/2026) × 6 horas semanais de dedicação por integrante × 3 integrantes. O valor é aproximado e deve ser revisto ao final de cada sprint, conforme a velocidade efetiva da equipe._

**3.2 Data prevista de início:** 04 / 08 / 2026

**3.3 Data prevista de término:** 01 / 12 / 2026

## 4. ESTIMATIVA DE CUSTO

O projeto é executado em contexto acadêmico, sem orçamento financeiro alocado. A mão de obra corresponde à carga horária dos integrantes na disciplina, não remunerada, e toda a infraestrutura utilizada opera em planos gratuitos. Por essa razão, o custo financeiro direto do projeto é nulo, ainda que o esforço em horas esteja integralmente registrado.

| Item de custo | Qtd. horas | Valor / hora | Valor total |
| --- | --- | --- | --- |
| **4.1 Recursos Humanos (especifique):** 3 integrantes da equipe de desenvolvimento (mão de obra acadêmica não remunerada) | 306 | R$ 0,00 | R$ 0,00 |
| **4.2 Hardware (especifique):** equipamentos pessoais dos próprios integrantes, já disponíveis | — | R$ 0,00 | R$ 0,00 |
| **4.3 Rede e serviços de hospedagem:** Vercel, Render e Supabase, todos em plano gratuito | — | R$ 0,00 | R$ 0,00 |
| **4.4 Software de terceiros:** ferramentas de código aberto e gratuitas (TypeScript, React, React Native, Expo, PostgreSQL, TanStack Query, Cockatiel, Vitest, Playwright, Maestro) | — | R$ 0,00 | R$ 0,00 |
| **4.5 Serviços e treinamento:** capacitação realizada pelos próprios integrantes por meio de documentação pública | — | R$ 0,00 | R$ 0,00 |
| **4.6 Total Geral:** | **306** | **R$ 0,00** | **R$ 0,00** |

## 5. PARTES INTERESSADAS

| Nome | Papel no projeto | Assinatura |
| --- | --- | --- |
| David Olinda Pomine | Líder do projeto (Scrum Master / Gerente de Projeto) e desenvolvedor | |
| Arthur Modesto | Desenvolvedor | |
| Bernardo Carvalho | Desenvolvedor | |
| Prof. Artur Martins Mol | Cliente / Avaliador | |
| Prof. João Paulo Carneiro Aramuni | Cliente / Avaliador | |
| Prof. Leonardo Vilela Cardoso | Cliente / Avaliador | |

**Observações:**

- As estimativas de prazo e custo são aproximadas e podem variar ao longo do projeto, devendo ser revistas após o detalhamento dos requisitos.

- Este documento, após ser completamente preenchido, deve ser assinado pelos responsáveis do projeto (gestores envolvidos).

- Este documento, se aprovado na **reunião de** _ **kickoff** _, autoriza o início do projeto de acordo com a especificação supra e as normas da empresa.
