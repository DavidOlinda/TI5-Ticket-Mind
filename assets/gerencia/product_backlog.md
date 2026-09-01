# Planejamento Geral do Projeto — Product Backlog (Versão Inicial)
 
**Projeto:** Ticket Mind
**Disciplina:** Trabalho Interdisciplinar: Aplicações Distribuídas (Engenharia de Software — PUC Minas)
**Artefato:** Planejamento geral do projeto (Product Backlog) — Versão Inicial
**Versão:** 1.1
---
 
## 1. Objetivo do documento
 
Este documento apresenta o planejamento geral do projeto Ticket Mind na forma de um
**Product Backlog** — a lista priorizada de tudo o que se espera que o produto contemple.
Os itens derivam do sequenciador de funcionalidades (MoSCoW) construído na Lean Inception,
dos requisitos funcionais **RF001 a RF012** e não-funcionais **RNF001 a RNF011** do
Documento de Arquitetura, e das restrições e mecanismos arquiteturais já definidos pela equipe.
 
Trata-se de uma **versão inicial**: as estimativas são aproximadas e a alocação por sprint e
por responsável deve ser revista ao final de cada sprint, conforme a velocidade efetiva da
equipe e o cronograma da disciplina. O backlog vivo é mantido no quadro Kanban do
GitHub Projects (GitHub Classroom), com as colunas *Product Backlog*, *Sprint Backlog*,
*Doing* e *Done*; este arquivo é a fotografia versionada desse quadro — incluindo, na
Seção 6, o recorte da sprint em curso, para não depender de um arquivo por sprint.
 
---
 
## 2. Convenções
 
**Estimativa (story points).** Escala de Fibonacci (1, 2, 3, 5, 8, 13), representando
esforço relativo — complexidade, incerteza e volume de trabalho — e não horas.
 
**Prioridade (MoSCoW).**
 
| Sigla | Significado | Uso no projeto |
| --- | --- | --- |
| **M** | *Must have* — Essencial | Compõe o MVP; sem estes itens o produto não entrega valor |
| **S** | *Should have* — Desejável | Agrega valor sobre o MVP; entra se houver capacidade na sprint |
| **C** | *Could have* — Opcional | Evolução prevista; só é desenvolvido se houver folga de prazo |
| **W** | *Won't have (this time)* — Fora de escopo | Registrado para memória; não será feito nesta versão |
 
**Status.** ✅ concluído · 🔄 em desenvolvimento · ⏳ planejado · ❌ não iniciado
 
**Responsável.** Indica quem conduz o item (não impede trabalho em par). Papéis de referência:
 
| Integrante | GitHub | Papel | Frente principal |
| --- | --- | --- | --- |
| David Olinda Pomine | [@DavidOlinda](https://github.com/DavidOlinda) | Líder / Scrum Master e desenvolvedor | Gerência, back-end / web service REST, mensageria, motor de recomendação |
| Bernardo Carvalho | [@bernardocdm](https://github.com/bernardocdm) | Desenvolvedor | Product Backlog, cliente web (React), testes de front-end, histórico e engajamento |
| Arthur Modesto | [@ArthurModesto1](https://github.com/ArthurModesto1) | Desenvolvedor | Ambiente e infraestrutura, protótipo e avaliação heurística, cliente móvel (React Native + Expo), testes automatizados, deploy |
 
---
 
## 3. Épicos
 
| ID | Épico | Descrição | Requisitos relacionados |
| --- | --- | --- | --- |
| **EP00** | Concepção, Arquitetura e Gerência | Definição do tema, Lean Inception, Documento de Arquitetura, artefatos de gerência e protótipo | — |
| **EP01** | Cadastro e Perfil de Interesses | Conta do usuário e configuração dos interesses que orientam as recomendações | RF001, RF002 |
| **EP02** | Descoberta de Eventos | Listagem, busca e detalhamento de eventos, com direcionamento ao canal oficial de compra | RF003, RF006 |
| **EP03** | Recomendação Personalizada | Motor que sugere eventos compatíveis com o perfil e aprende com o feedback do usuário | RF004, RF009 |
| **EP04** | Notificação em Tempo Real | Propagação imediata de eventos compatíveis, quedas de preço e últimas unidades | RF005, RF007 |
| **EP05** | Histórico e Engajamento | Registro e consulta do histórico de eventos visualizados e curtidos | RF008 |
| **EP06** | Social e Integrações | Recomendação para grupos, integração com calendário e compartilhamento social | RF010, RF011, RF012 |
| **EP07** | Plataforma, Resiliência e Qualidade | Web service REST, contrato de tipos compartilhado, mensageria, concorrência, tratamento de falhas, testes e deploy | RNF001–RNF011 |
 
---
 
## 4. Product Backlog
 
### 4.1. EP00 — Concepção, Arquitetura e Gerência
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB01 | Definir o tema do projeto e delimitar o problema em suas duas frentes (falha de descoberta e de tempestividade) | M | 3 | 1 | Todos | ✅ |
| PB02 | Conduzir a Lean Inception: visão de produto, quadros "É / Não é" e "Faz / Não faz", personas (Mariana, Rafael, Camila) e jornada do usuário em cinco etapas | M | 5 | 1 | David | ✅ |
| PB03 | Construir o sequenciador de funcionalidades (MoSCoW) e derivar os requisitos funcionais RF001–RF012 | M | 3 | 1 | David | ✅ |
| PB04 | Especificar os requisitos não-funcionais (RNF001–RNF011) e as restrições arquiteturais | M | 3 | 2 | David | ✅ |
| PB05 | Definir a stack tecnológica e os mecanismos arquiteturais nos estados de análise, design e implementação, com as justificativas de cada decisão | M | 5 | 2 | David / Bernardo | ✅ |
| PB06 | Redigir o Documento de Arquitetura — Seções 1 a 4 (apresentação, produto, requisitos, modelagem e histórias de usuário) — Versão Inicial | M | 5 | 2 | David | ✅ |
| PB07 | Elaborar o Termo de Abertura do Projeto (TAP 001) e o registro das partes interessadas | M | 3 | 2 | David | ✅ |
| PB08 | Configurar o ambiente no GitHub Classroom (repositório público, integrantes e orientadores) — Versão Final | M | 2 | 2 | Arthur | ✅ |
| PB09 | Configurar o quadro Kanban no GitHub Projects com as colunas Product Backlog, Sprint Backlog, Doing e Done | M | 1 | 2 | Arthur | ✅ |
| PB10 | Criar as contas nos serviços de nuvem de plano gratuito (Vercel, Render, Supabase) e no Figma | M | 1 | 2 | Arthur | ✅ |
| PB11 | Consolidar o Planejamento geral do projeto (Product Backlog) — Versão Inicial | M | 3 | 2 | Bernardo | ✅ |
| PB12 | Elaborar o recorte do Sprint Backlog da Sprint 2 (Seção 6 deste documento) e mantê-lo atualizado | M | 2 | 2 | Arthur | 🔄 |
| PB13 | Atualizar o Documento de Arquitetura — Seções 1 a 4 (versão atualizada, Sprint 2 / Semana 2) | M | 3 | 2 | David | 🔄 |
| PB14 | Manter as atas de reunião semanais e os relatórios de contribuição semanal (individual) ao longo do projeto | M | 3 | 1–8 | Todos | 🔄 |
| PB15 | Modelar a Visão Lógica: diagrama de classes, diagrama de componentes e modelo de dados (DER) | M | 8 | 3 | David | ❌ |
| PB16 | Produzir os wireframes das telas principais (protótipo interativo no Figma) | M | 8 | 3 | Arthur | ❌ |
| PB17 | Realizar a avaliação heurística de usabilidade sobre o protótipo | M | 3 | 3 | Arthur | ❌ |
| PB18 | Definir os cenários de qualidade e conduzir a avaliação da arquitetura pelo método ATAM | S | 5 | 8 | David | ❌ |
| PB19 | Preparar a apresentação final e o material de divulgação (slides e vídeo) | M | 5 | 8 | Bernardo | ❌ |
 
### 4.2. EP07 — Plataforma, Resiliência e Qualidade (habilitadores técnicos)
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB20 | Estruturar o monorepo (back, front, mobile) e o pacote de tipos compartilhados entre as camadas (RNF011) | M | 5 | 3 | David | ❌ |
| PB21 | Implementar o esqueleto do web service REST em TypeScript, com padronização de rotas, erros e documentação (RNF001) | M | 5 | 3 | David | ❌ |
| PB22 | Modelar e provisionar o banco PostgreSQL no Supabase (esquema de usuários, eventos, interesses, interações) | M | 5 | 3 | David | ❌ |
| PB23 | Configurar o cliente web (React) e o cliente móvel (React Native + Expo) consumindo o mesmo web service, com paridade das funcionalidades essenciais (RNF002, RNF003) | M | 5 | 3 | Bernardo / Arthur | ❌ |
| PB24 | Configurar o middleware de mensageria (Supabase Realtime) com filtros de canal, de modo que cada cliente receba apenas as atualizações do seu interesse (RNF004, RNF006) | M | 8 | 4 | David | ❌ |
| PB25 | Garantir o atendimento concorrente a múltiplos clientes sobre a mesma base de eventos, sem inconsistência de dados (RNF005) | M | 5 | 4 | David | ❌ |
| PB26 | Implementar no cliente as políticas de cache, retry automático e revalidação com TanStack Query (RNF007) | M | 3 | 4 | Bernardo | ❌ |
| PB27 | Implementar no servidor as políticas de retry, timeout e circuit breaker com Cockatiel (RNF007, RNF008) | M | 5 | 5 | David | ❌ |
| PB28 | Configurar a suíte de testes unitários e de integração (Vitest) no back-end e no front-end (RNF009) | M | 5 | 5 | Bernardo / Arthur | ❌ |
| PB29 | Configurar os testes ponta a ponta: Playwright (web, Bernardo) e Maestro (mobile, Arthur) para os fluxos essenciais (RNF009) | M | 5 | 7 | Bernardo / Arthur | ❌ |
| PB30 | Configurar o deploy contínuo a partir do Git: Vercel (front-end) e Render (back-end), em plano gratuito (RNF010) | M | 3 | 3 | Arthur | ❌ |
| PB31 | Endurecer a resiliência: testes de falha de rede, timeout e indisponibilidade de serviço, e ajuste das políticas | S | 5 | 7 | Arthur | ❌ |
 
### 4.3. EP01 — Cadastro e Perfil de Interesses
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB32 | Eu, como visitante, quero criar uma conta e autenticar-me para acessar as recomendações personalizadas (RF001) | M | 5 | 4 | David | ❌ |
| PB33 | Eu, como Mariana, quero cadastrar os artistas e gêneros musicais que acompanho para receber recomendações alinhadas ao meu gosto (RF002) | M | 5 | 4 | Bernardo | ❌ |
| PB34 | Eu, como Rafael, quero cadastrar o time para o qual torço para acompanhar os jogos sem procurar em vários sites (RF002) | M | 2 | 4 | Bernardo | ❌ |
| PB35 | Eu, como usuário, quero editar meu perfil de interesses (artistas, categorias, gêneros e times) a qualquer momento para manter as recomendações atualizadas (RF002) | M | 3 | 4 | Bernardo | ❌ |
| PB36 | Paridade da funcionalidade de cadastro e perfil no cliente móvel (RF001, RF002 / RNF002) | M | 3 | 4 | Arthur | ❌ |
 
### 4.4. EP02 — Descoberta de Eventos
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB37 | Eu, como usuário, quero listar os eventos disponíveis e buscá-los por nome, categoria ou data para explorar o catálogo (RF003) | M | 5 | 4 | Bernardo | ❌ |
| PB38 | Eu, como Camila, quero consultar eventos de categorias variadas em um único lugar para planejar saídas em grupo sem consultar múltiplas plataformas (RF003) | M | 3 | 4 | Bernardo | ❌ |
| PB39 | Eu, como usuário, quero visualizar os detalhes de um evento e ser direcionado ao canal oficial de compra para concluir a aquisição do ingresso (RF006) | M | 3 | 4 | Bernardo | ❌ |
| PB40 | Paridade da listagem, busca e detalhe de evento no cliente móvel (RF003, RF006 / RNF002) | M | 3 | 4 | Arthur | ❌ |
| PB41 | Rotina de ingestão / cadastro de eventos e ingressos que alimenta o catálogo e dispara os eventos de mensageria | M | 5 | 4 | David | ❌ |
 
### 4.5. EP03 — Recomendação Personalizada
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB42 | Eu, como usuário, quero receber recomendações de eventos compatíveis com o meu perfil de interesses para descobrir eventos relevantes sem busca ativa (RF004) | M | 8 | 4 | David | ❌ |
| PB43 | Eu, como usuário, quero curtir ou descurtir as recomendações recebidas para tornar as próximas sugestões mais aderentes ao meu perfil (RF009) | S | 5 | 5 | David | ❌ |
| PB44 | Realimentação do motor de recomendação com o feedback do usuário (curtir / não curtir) (RF009) | S | 5 | 5 | David | ❌ |
| PB45 | Paridade da exibição e avaliação de recomendações no cliente móvel (RF004, RF009 / RNF002) | M | 3 | 4 | Arthur | ❌ |
 
### 4.6. EP04 — Notificação em Tempo Real
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB46 | Eu, como Mariana, quero ser notificada em tempo real assim que os ingressos de um artista que sigo entrarem à venda para comprar antes que o lote se esgote (RF005) | M | 8 | 4 | David | ❌ |
| PB47 | Recebimento e exibição das notificações em tempo real no cliente web, sem recarregamento manual (RF005 / RNF004) | M | 5 | 4 | Bernardo | ❌ |
| PB48 | Recebimento e exibição das notificações em tempo real no cliente móvel (RF005 / RNF004, RNF002) | M | 5 | 4 | Arthur | ❌ |
| PB49 | Eu, como Rafael, quero receber alertas de queda de preço e de últimas unidades para aproveitar a melhor oportunidade de compra dentro da minha rotina (RF007) | S | 5 | 5 | David | ❌ |
| PB50 | Preferências de notificação: canais, tipos de alerta e frequência (RF007) | S | 3 | 5 | Bernardo | ❌ |
 
### 4.7. EP05 — Histórico e Engajamento
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB51 | Eu, como usuário, quero consultar o histórico de eventos que visualizei e curti para retomar um evento que me interessou anteriormente (RF008) | S | 5 | 5 | Bernardo | ❌ |
| PB52 | Registro automático das interações do usuário (visualização e curtida) que alimentam o histórico e a recomendação (RF008, RF009) | S | 3 | 5 | David | ❌ |
| PB53 | Paridade do histórico no cliente móvel (RF008 / RNF002) | S | 2 | 5 | Arthur | ❌ |
 
### 4.8. EP06 — Social e Integrações
 
| ID | Item / História | Prioridade | Estimativa | Sprint | Responsável | Status |
| --- | --- | --- | --- | --- | --- | --- |
| PB54 | Eu, como Camila, quero gerar recomendações para um grupo de amigos considerando os interesses combinados dos participantes para encontrar programas que agradem a todos (RF010) | C | 8 | 5 | David | ❌ |
| PB55 | Eu, como usuário do app móvel, quero integrar os eventos de interesse ao meu calendário para não esquecer as datas (RF011) | C | 5 | 5 | Arthur | ❌ |
| PB56 | Eu, como Camila, quero compartilhar um evento com meus amigos para combinar o programa com o grupo (RF012) | C | 3 | 5 | Bernardo | ❌ |
 
### 4.9. Fora de escopo nesta versão (registro)
 
| ID | Item | Prioridade | Motivo |
| --- | --- | --- | --- |
| PB57 | Venda, emissão, validação ou revenda de ingressos e processamento de pagamentos | W | Contra-escopo do TAP 001 — o usuário é direcionado ao canal oficial |
| PB58 | Reserva de ingressos e garantia de disponibilidade | W | Contra-escopo do TAP 001 |
| PB59 | Rede social de eventos (perfis públicos, feed, comentários, seguidores) | W | Contra-escopo do TAP 001 |
| PB60 | Aplicativos móveis nativos separados para Android e iOS | W | RNF003 — cliente móvel exclusivamente híbrido, base de código única |
| PB61 | Operação em ambiente produtivo com carga real | W | Implantação limitada a planos gratuitos, para demonstração acadêmica |
 
---
 
## 5. Roadmap por sprint (visão inicial)
 
Sprints de duas semanas, conforme o calendário da disciplina (início em 04/08/2026,
término previsto em 01/12/2026 pelo TAP 001). A distribuição dos requisitos funcionais
entre as Sprints 4 e 5 acompanha a tabela da Seção 3.1 do Documento de Arquitetura.
As Sprints 1 e 2 seguem o cronograma já divulgado; as Sprints 3 a 8 são **previsão** e
serão ajustadas conforme o cronograma detalhado da disciplina for publicado.
 
| Sprint | Período | Objetivo da sprint | Itens |
| --- | --- | --- | --- |
| **Sprint 1** | 04/08 – 17/08 | Definição inicial do trabalho: tema, Lean Inception – Visão de Produto e sequenciador MoSCoW | PB01–PB03, PB14 |
| **Sprint 2** | 18/08 – 31/08 | Iniciação do projeto e arquitetura: Documento de Arquitetura (Seções 1–4), decisões de arquitetura, TAP, ambiente GitHub Classroom, Product Backlog e Sprint Backlog | PB04–PB14 |
| **Sprint 3** | 01/09 – 14/09 | Modelagem, protótipo e fundação técnica: diagramas, wireframes, avaliação heurística, monorepo, web service, banco e deploy | PB15–PB17, PB20–PB23, PB30 |
| **Sprint 4** | 15/09 – 28/09 | MVP essencial (RF001–RF006): cadastro, perfil, descoberta, recomendação e notificação em tempo real | PB24–PB26, PB32–PB42, PB45–PB48 |
| **Sprint 5** | 29/09 – 12/10 | Funcionalidades desejáveis e opcionais (RF007–RF012): resiliência do servidor, alertas de preço, histórico, avaliação de recomendações e integrações | PB27, PB28, PB43, PB44, PB49–PB56 |
| **Sprint 6** | 13/10 – 26/10 | Estabilização das funcionalidades e fechamento de pendências das Sprints 4 e 5 | itens remanescentes |
| **Sprint 7** | 27/10 – 09/11 | Qualidade: testes ponta a ponta (Playwright e Maestro) e endurecimento da resiliência | PB29, PB31 |
| **Sprint 8** | 10/11 – 01/12 | Avaliação da arquitetura (ATAM), ajustes finais, apresentação e divulgação | PB18, PB19 |
 
---
 
## 6. Sprint Backlog atual — Sprint 2
 
Recorte da sprint em curso, atualizado a cada sprint nesta mesma seção (sem arquivo
separado), para manter uma única fonte de verdade sincronizada com o quadro Kanban do
GitHub Projects.
 
**Período:** 18/08/2026 – 01/09/2026 (Semana 1: 18/08–24/08 · Semana 2: 25/08–31/08 · Entrega 2: terça, 01/09)
 
**Meta da sprint (Sprint Goal):** encerrar a etapa de concepção e arquitetura do projeto —
publicar as Seções 1 a 4 do Documento de Arquitetura, formalizar o Termo de Abertura do
Projeto, consolidar o ambiente de trabalho no GitHub Classroom (repositório, Kanban e
Product Backlog) e realizar a reunião de *kickoff* que autoriza formalmente o início do
desenvolvimento na Sprint 3.
 
### 6.1. Itens da sprint
 
Status consolidado dos itens PB04–PB14 (descrições completas na Seção 4.1):
 
| ID | Responsável | Status |
| --- | --- | --- |
| PB04 | David | ✅ |
| PB05 | David / Bernardo | ✅ |
| PB06 | David | ✅ |
| PB07 | David | ✅ |
| PB08 | Arthur | ✅ |
| PB09 | Arthur | ✅ |
| PB10 | Arthur | ✅ |
| PB11 | Bernardo | ✅ |
| PB12 | Arthur | 🔄 |
| PB13 | David | 🔄 |
| PB14 | Todos | 🔄 |
 
### 6.2. Tarefas de fechamento da Entrega 2 (01/09)
 
Detalhamento de PB14 ligado ao fechamento da sprint, delegado a Arthur e Bernardo em
28/08/2026. Dependem de uma reunião real do grupo — não devem ser preenchidas com dados
fictícios.
 
| Tarefa | Responsável | Status |
| --- | --- | --- |
| Ata de reunião de *kickoff* (`assets/atas/`) | Arthur / Bernardo | ❌ |
| Fechamento da Sprint 2 | Arthur / Bernardo | ❌ |
| Planejamento da Sprint 3 | Arthur / Bernardo | ❌ |
| Relatório de Contribuição Semanal (individual) | David ✅ · Bernardo ✅ · Arthur ✅ |
 
### 6.3. Quadro Kanban (resumo desta sprint)
 
| Coluna | Itens |
| --- | --- |
| **Done** | PB04, PB05, PB06, PB07, PB08, PB09, PB10, PB11 |
| **Doing** | PB12, PB13, PB14 |
| **Sprint Backlog** | Ata de *kickoff*, Fechamento da Sprint 2, Planejamento da Sprint 3 |
| **Product Backlog** | Itens de PB15 em diante (Sprint 3 e seguintes) |
 
---
 
## 7. Histórico de versões
 
| Versão | Data | Descrição | Responsável |
| --- | --- | --- | --- |
| 1.0 | 18/08/2026 | Versão inicial do Product Backlog, derivada da Lean Inception, dos requisitos RF001–RF012 / RNF001–RNF011 e do TAP 001 | Bernardo Carvalho |
| 1.1 | 01/09/2026 | Incorporação da Seção 6, com o recorte da sprint em curso mantido neste mesmo documento | Arthur Modesto |