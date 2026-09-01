<!-- [![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=99999999&assignment_repo_type=AssignmentRepo) [![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=99999999)
-->
 
<a href="https://classroom.github.com/online_ide?assignment_repo_id=99999999&assignment_repo_type=AssignmentRepo"><img src="https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg" width="200"/></a> <a href="https://classroom.github.com/open-in-codespaces?assignment_repo_id=99999999"><img src="https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg" width="250"/></a>
 
---
 
# 🎫 TICKET MIND — Plataforma de Recomendação e Notificação em Tempo Real 🔔
 
> [!NOTE]
> Plataforma distribuída que aprende as preferências de cada usuário — **artistas, categorias, gêneros e times** — e o **notifica em tempo real** assim que surge um evento ou ingresso compatível com o seu perfil. **Nunca mais perca um show, jogo ou evento por descobrir tarde demais.**
 
<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O mercado de eventos e ingressos é marcado pela <b>alta rotatividade de ofertas</b> e pela <b>rápida exaustão de lotes</b>, o que faz com que muitos consumidores percam eventos de seu interesse por não tomarem conhecimento deles a tempo. O <b>Ticket Mind</b> ataca esse problema em suas duas frentes: a <i>falha de descoberta</i> (o usuário desconhece o evento) e a <i>falha de tempestividade</i> (o usuário toma ciência da oferta tarde demais). A plataforma aprende o perfil do usuário, recomenda eventos compatíveis e entrega <b>notificações em tempo real</b> sobre novos lançamentos, quedas de preço e últimas unidades. A solução contempla <b>aplicação web</b>, <b>aplicação móvel híbrida</b>, comunicação via <b>web service REST</b> e <b>middleware de mensageria</b> para processamento em tempo real. Desenvolvida como projeto acadêmico da disciplina <b>Trabalho Interdisciplinar TIS V — Aplicações Distribuídas</b> do curso de <b>Engenharia de Software</b> da <b>PUC Minas</b>.
      </div>
    </td>
    <td>
      <div>
        <img src="https://joaopauloaramuni.github.io/image/logo_ES_vertical.png" alt="Logo Ticket Mind" width="120px"/>
      </div>
    </td>
  </tr>
</table>
---
 
## 🚧 Status do Projeto
 
[![Versão](https://img.shields.io/badge/Versão-em%20desenvolvimento-orange?style=for-the-badge)](https://github.com/DavidOlinda/TI5-Ticket-Mind) ![Sprint](https://img.shields.io/badge/Sprint-2%20(Arquitetura)-orange?style=for-the-badge) ![React](https://img.shields.io/badge/React-planejado-lightgrey?style=for-the-badge&logo=react&logoColor=white) ![React Native](https://img.shields.io/badge/React_Native%20%2B%20Expo-planejado-lightgrey?style=for-the-badge&logo=expo&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-planejado-lightgrey?style=for-the-badge&logo=typescript&logoColor=white) ![Supabase](https://img.shields.io/badge/Supabase-planejado-lightgrey?style=for-the-badge&logo=supabase&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-planejado-lightgrey?style=for-the-badge&logo=postgresql&logoColor=white)
 
> [!WARNING]
> O projeto está em fase de **arquitetura e planejamento** (Sprint 2). O código-fonte começa a ser produzido na **Sprint 4** (entrega parcial das funcionalidades prioritárias, RF001–RF006). Seções relacionadas a implementação, execução e telas estão marcadas como **a preencher** até lá.
 
---
 
## 📚 Índice
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
- [Instalação e Execução](#-instalação-e-execução)
  - [Pré-requisitos](#pré-requisitos)
  - [Variáveis de Ambiente](#-variáveis-de-ambiente)
  - [Instalação de Dependências](#-instalação-de-dependências)
  - [Como Executar a Aplicação](#-como-executar-a-aplicação)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Demonstração](#-demonstração)
- [Testes](#-testes)
- [Documentações Utilizadas](#-documentações-utilizadas)
- [Autores](#-autores)
- [Contribuição](#-contribuição)
- [Agradecimentos](#-agradecimentos)
---
 
## 📝 Sobre o Projeto
 
Pessoas perdem shows, jogos e eventos de seu interesse porque não ficam sabendo a tempo. O **Ticket Mind** resolve isso atacando dois problemas complementares:
 
- **Falha de descoberta** — O usuário simplesmente não descobre que o evento existe.
- **Falha de tempestividade** — Os ingressos esgotam antes que o usuário perceba a oportunidade.
Para isso, o sistema aprende as preferências do usuário (artistas, categorias, times, gêneros), recomenda eventos compatíveis com o perfil e envia **notificações em tempo real** assim que surge um evento ou ingresso relevante — incluindo alertas de novo lançamento, queda de preço e últimas unidades. O ciclo é contínuo: as curtidas e descurtidas do usuário realimentam o motor de recomendação, refinando as sugestões futuras.
 
O projeto foi desenvolvido como parte do **Trabalho Interdisciplinar TIS V — Aplicações Distribuídas** do curso de **Engenharia de Software** da **PUC Minas** (Campus Coração Eucarístico), sob orientação dos professores Artur Martins Mol, João Paulo Carneiro Aramuni e Leonardo Vilela Cardoso.
 
> [!NOTE]
> O desenvolvimento segue uma abordagem **iterativa e incremental**, organizada em sprints (Scrum), com Lean Inception para a visão de produto, documento de arquitetura, prototipação no Figma e entregas parciais antes da versão final.
 
---
 
## ✨ Funcionalidades Principais
 
> [!NOTE]
> Funcionalidades organizadas pelo método **MoSCoW**, conforme o Termo de Abertura e o documento de requisitos.
 
### 🟢 Essenciais — MVP (RF001–RF006) · *Sprint 4*
- 🔐 **Cadastro e Login:** Autenticação de usuários na plataforma.
- 🎯 **Definição de Interesses:** Escolha de artistas, categorias, times e gêneros que compõem o perfil.
- 🔎 **Listagem e Busca de Eventos:** Consulta ao catálogo de eventos disponíveis.
- 🤖 **Motor de Recomendação:** Sugestão de eventos compatíveis com o perfil do usuário.
- 🔔 **Notificações em Tempo Real:** Alertas imediatos quando surge um evento ou ingresso relevante.
- 🛒 **Detalhes do Evento e Direcionamento à Compra:** Visualização de detalhes e encaminhamento para a compra.
### 🟡 Desejáveis (RF007–RF009) · *Sprint 5*
- 💸 **Queda de Preço / Últimas Unidades:** Alertas de oportunidade e escassez.
- 🕘 **Histórico de Visualizados e Curtidos:** Registro da navegação do usuário.
- 👍 **Feedback nas Recomendações:** Curtir/descurtir para refinar sugestões futuras.
### ⚪ Opcionais (RF010–RF012) · *Sprint 5, se houver folga*
- 👥 **Recomendação para Grupos**
- 📅 **Integração com Calendário**
- 📲 **Compartilhamento Social**
> [!NOTE]
> As funcionalidades opcionais (RF010–RF012) estão explicitamente fora do escopo garantido no Termo de Abertura, condicionadas a eventual folga de prazo.
 
---
 
## 🛠 Tecnologias Utilizadas
 
> [!NOTE]
> Stack **definida na fase de arquitetura**; a implementação inicia na Sprint 4. As versões serão fixadas conforme o desenvolvimento avança.
 
### 💻 Front-end Web
 
* **Biblioteca:** React
* **Linguagem:** TypeScript
* **Requisições / cache / retry:** TanStack Query
* **Build & Deploy:** Vercel *(a configurar)*
### 📱 Mobile / Híbrido
 
* **Framework:** React Native + [Expo](https://expo.dev/)
* **Linguagem:** TypeScript
* **Requisições / cache / retry:** TanStack Query
### 🖥️ Back-end
 
* **Runtime:** Node.js
* **Linguagem:** TypeScript
* **Modelo de Web Service:** REST
* **Resiliência (retry / timeout / circuit breaker):** Cockatiel
* **Hospedagem:** Render *(a configurar)*
### 🗄️ Dados & Tempo Real
 
* **Banco de Dados:** PostgreSQL
* **Mensageria em Tempo Real:** [Supabase](https://supabase.com/) (Realtime), com estratégia de **Filtros de Canal** (*Channel Filtering*)
### 🧪 Testes
 
* **Unitário / Integração:** [Vitest](https://vitest.dev/)
* **E2E Web:** Playwright
* **E2E Mobile:** Maestro
### ⚙️ Infraestrutura & DevOps
 
* **Versionamento:** Git + GitHub (GitHub Classroom)
* **Gestão (Kanban):** GitHub Projects *(a criar)*
* **Prototipação:** Figma *(a criar)*
---
 
## 🏗 Arquitetura
 
O Ticket Mind adota uma arquitetura **distribuída cliente-servidor** com múltiplos clientes (web e móvel) consumindo um mesmo **web service REST**, apoiada por um **middleware de mensageria em tempo real**.
 
- **Clientes (Web e Mobile):** Aplicação React (web) e React Native + Expo (mobile), compartilhando tipos em TypeScript e a mesma API REST.
- **Back-end (API REST):** Serviço em Node.js/TypeScript que expõe os recursos de eventos, perfis, recomendações e notificações, com políticas de retry, timeout e circuit breaker (Cockatiel).
- **Mensageria em Tempo Real:** Supabase Realtime entrega atualizações simultâneas a múltiplos clientes conectados; cada cliente assina apenas os canais do seu interesse (Filtros de Canal), reduzindo tráfego e evitando conflito de concorrência.
- **Banco de Dados:** PostgreSQL, integrado nativamente ao Supabase (dados + realtime no mesmo ambiente).
### Decisões de Arquitetura (resumo)
 
| Requisito | Decisão | Motivação resumida |
|-----------|---------|--------------------|
| Modelo de Web Service | REST | Padrão simples, conhecido e fácil de documentar/testar |
| Stack Back-end | TypeScript | Tipagem estática e compartilhamento de tipos com o front |
| Front-end Web | React | Ecossistema consolidado e componentização |
| Mobile/Híbrido | React Native + Expo | Reaproveita conhecimento de React; build ágil |
| Mensageria (tempo real) | Supabase Realtime | Canais prontos sobre o PostgreSQL, sem broker separado |
| Concorrência | Filtros de Canal | Cada cliente assina só o que interessa |
| Resiliência | TanStack Query (cliente) + Cockatiel (servidor) | Cache/retry no cliente; retry/timeout/circuit breaker no servidor |
| Testes | Vitest · Playwright · Maestro | Unit/integração, E2E web e E2E mobile |
| Hospedagem | Vercel (front) · Render (back) | Planos gratuitos com deploy automático via Git |
| Banco de Dados | PostgreSQL | Relacional robusto, gratuito e integrado ao Supabase |
 
### Modelo de Dados (Entidades Principais)
 
> [!WARNING]
> **A preencher** — O Diagrama Entidade-Relacionamento (DER) e o modelo lógico de dados serão elaborados na **Sprint 3** e documentados em `docs/4.modelagem.md` (seções 4.2 e 4.3).
 
### Diagramas
 
> [!WARNING]
> **A preencher** — Diagramas de classes, de componentes e DER previstos para a **Sprint 3**.
 
---
 
## 🔧 Instalação e Execução
 
> [!WARNING]
> **A preencher** — Assim que a primeira versão do sistema estiver disponível (a partir da **Sprint 4**), esta seção será complementada com as instruções completas de instalação de dependências e execução da aplicação (web, mobile e back-end).
 
### Pré-requisitos
 
* **Node.js:** Versão LTS (v18.x ou superior)
* **npm:** Incluído com o Node.js
* **Expo CLI:** Para execução do cliente mobile *(a confirmar na Sprint 4)*
* **PostgreSQL** *(ou conta no Supabase)*
---
 
### 🔑 Variáveis de Ambiente
 
> [!WARNING]
> **A preencher** — As variáveis de ambiente (URL do banco, chaves do Supabase, segredo de JWT, etc.) serão definidas quando o back-end começar a ser implementado.
 
| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `DATABASE_URL` | URL de conexão PostgreSQL. | _a preencher_ |
| `SUPABASE_URL` | URL do projeto Supabase. | _a preencher_ |
| `SUPABASE_ANON_KEY` | Chave pública (anon) do Supabase. | _a preencher_ |
| _..._ | _demais variáveis a definir_ | _a preencher_ |
 
---
 
### 📦 Instalação de Dependências
 
```bash
git clone https://github.com/DavidOlinda/TI5-Ticket-Mind.git
cd TI5-Ticket-Mind
```
 
> [!WARNING]
> **A preencher** — Passos de instalação por módulo (`code/back`, `code/front`, `code/mobile`) serão adicionados na Sprint 4.
 
---
 
### ⚡ Como Executar a Aplicação
 
> [!WARNING]
> **A preencher** — Comandos de execução (back-end, front-end web e app mobile via Expo) serão adicionados na Sprint 4.
 
---
 
## 📂 Estrutura de Pastas
 
```
.
├── README.md                          # 📘 Documentação principal do projeto
├── CITATION.cff                       # 📄 Metadados de citação acadêmica (campos a preencher)
│
├── /docs                              # 📚 Documento de Arquitetura (template PUC Minas)
│   ├── README.md                      # 🗂️ Capa e sumário do documento
│   ├── 1.apresentacao.md              # ✅ Apresentação, problema, objetivos, glossário
│   ├── 2.nosso_produto.md             # ✅ Visão do produto, MVP, personas
│   ├── 3.requisitos.md                # ✅ Requisitos (RF/RNF), restrições, mecanismos
│   ├── 4.modelagem.md                 # 🟡 Jornada e histórias (4.1); diagramas/DER (Sprint 3)
│   ├── 5.wireframe.md                 # ⬜ Wireframes (Sprint 3)
│   ├── 6.avaliacao_heuristica.md      # ⬜ Avaliação heurística (sprint futura)
│   ├── 7.solucao.md                   # ⬜ Projeto da solução / telas (sprint futura)
│   └── 8.avaliacao_arquitetura.md     # ⬜ Avaliação da arquitetura / ATAM (Sprint 6)
│
├── /assets                            # 📂 Artefatos de gerência do projeto
│   ├── /atas                          # 📋 Atas de reunião
│   ├── /contribuicao_semanal          # 🧾 Relatórios de contribuição individuais
│   └── /gerencia                      # 📑 Termo de Abertura, Product Backlog
│
├── /code                              # 📁 Código-fonte (a partir da Sprint 4)
│   ├── /back                          # 🖥️ Back-end (Node.js + TypeScript, REST)
│   ├── /front                         # 💻 Front-end Web (React + TypeScript)
│   └── /mobile                        # 📱 Mobile (React Native + Expo)
│
└── /divulge                           # 📣 Material de divulgação
    ├── /presentation                  # 🎤 Slides de apresentação
    └── /video                         # 🎥 Vídeos de demonstração
```
 
---
 
## 🎥 Demonstração
 
> [!WARNING]
> **A preencher** — As capturas de tela, GIFs e o protótipo interativo (Figma) serão adicionados conforme o desenvolvimento avança. Telas previstas para a Sprint 3 (wireframes) e Sprints seguintes (implementação).
 
### Principais Telas *(planejadas)*
 
| Tela | Descrição |
| :---: | :--- |
| **Cadastro / Login** | Autenticação do usuário na plataforma |
| **Definição de Interesses** | Seleção de artistas, categorias, times e gêneros |
| **Feed de Recomendações** | Eventos sugeridos com base no perfil |
| **Busca de Eventos** | Listagem e filtro do catálogo de eventos |
| **Detalhes do Evento** | Informações e direcionamento à compra |
| **Notificações** | Alertas em tempo real (lançamento, preço, últimas unidades) |
| **Perfil** | Gerenciamento de preferências e histórico |
 
---
 
## 🧪 Testes
 
> [!WARNING]
> **A preencher** — A suíte de testes será implementada junto ao código, a partir da Sprint 4.
 
Estratégia definida na arquitetura:
 
* **Unitário / Integração:** Vitest
* **E2E Web:** Playwright
* **E2E Mobile:** Maestro
---
 
## 🔗 Documentações Utilizadas
 
* 📖 **React:** [Documentação Oficial do React](https://react.dev/reference/react)
* 📖 **React Native:** [Documentação Oficial](https://reactnative.dev/docs/getting-started)
* 📖 **Expo:** [Documentação do Expo](https://docs.expo.dev/)
* 📖 **TypeScript:** [Documentação do TypeScript](https://www.typescriptlang.org/docs/)
* 📖 **Supabase:** [Documentação do Supabase](https://supabase.com/docs)
* 📖 **PostgreSQL:** [Documentação do PostgreSQL](https://www.postgresql.org/docs/)
* 📖 **TanStack Query:** [Documentação do TanStack Query](https://tanstack.com/query/latest)
* 📖 **Vitest:** [Documentação do Vitest](https://vitest.dev/)
* 📖 **Playwright:** [Documentação do Playwright](https://playwright.dev/docs/intro)
* 📖 **Maestro:** [Documentação do Maestro](https://maestro.mobile.dev/)
---
 
## 👥 Autores
 
| 👤 Nome | Papel | :octocat: GitHub |
|---------|-------|-----------------|
| David Olinda Pomine | Líder (Scrum Master / Gerente de Projeto) | [@DavidOlinda](https://github.com/DavidOlinda) |
| Arthur Modesto | Desenvolvedor | [@ArthurModesto1](https://github.com/ArthurModesto1) |
| Bernardo Carvalho | Desenvolvedor | [@bernardocdm](https://github.com/bernardocdm) |
 
**Professores Orientadores:**
- **Prof. Artur Martins Mol** — PUC Minas
- **Prof. João Paulo Carneiro Aramuni** — PUC Minas
- **Prof. Leonardo Vilela Cardoso** — PUC Minas
---
 
## 🤝 Contribuição
 
1.  Faça um `fork` do projeto (ou crie uma branch, se for colaborador).
2.  Crie uma branch para sua feature (`git checkout -b feature/minha-feature`).
3.  Commit suas mudanças (`git commit -m 'feat: Adiciona nova funcionalidade X'`). **(Utilize [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/))**
4.  Faça o `push` para a branch (`git push origin feature/minha-feature`).
5.  Abra um **Pull Request (PR)**.
> [!IMPORTANT]
> A avaliação da disciplina é **individualizada por contribuição no GitHub**. Cada integrante deve configurar sua identidade Git e commitar em nome próprio:
> ```
> git config --global user.name "Seu Nome Completo"
> git config --global user.email "SEU_ID+SEU_USUARIO@users.noreply.github.com"
> ```
 
---
 
## 🙏 Agradecimentos
 
* [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo apoio institucional, estrutura acadêmica e fomento à inovação e boas práticas de engenharia.
* **Prof. Artur Martins Mol** — Pela orientação e acompanhamento do projeto ao longo das sprints.
* **Prof. João Paulo Carneiro Aramuni** — Pela orientação técnica e suporte metodológico.
* **Prof. Leonardo Vilela Cardoso** — Pela orientação e acompanhamento do projeto ao longo das sprints.
---
