# Relatório de Contribuição Semanal — David Olinda Pomine

**Projeto:** Ticket Mind
**Papel:** Líder do projeto (Scrum Master / Gerente de Projeto) e desenvolvedor
**GitHub:** [@DavidOlinda](https://github.com/DavidOlinda)

---

# Sprint 1

### Semana 1 (04/08 - 10/08)

- Participação na definição do tema do projeto, com a escolha da plataforma de recomendação e notificação em tempo real aplicada ao mercado de eventos e ingressos.
- Delimitação do problema a ser resolvido, separando as duas frentes que o compõem: a falha de descoberta (o usuário desconhece o evento) e a falha de tempestividade (o usuário toma ciência da oferta tarde demais).

### Semana 2 (11/08 - 17/08)

- Elaboração da Lean Inception — Visão de Produto: definição do produto Ticket Mind, das três personas (Mariana, Rafael e Camila), da jornada do usuário em cinco etapas e do MVP.
- Construção do sequenciador de funcionalidades pelo método MoSCoW, com a classificação das funcionalidades em prioritárias, desejáveis e opcionais.

---

# Sprint 2

### Semana 1 (18/08 - 24/08)

- Consolidação do documento de planejamento do projeto, reunindo tema, visão de produto, personas, jornada, sequenciador MoSCoW e requisitos obrigatórios da disciplina.
- Definição da stack tecnológica e das decisões de arquitetura que atendem a cada requisito obrigatório, com a justificativa técnica de cada escolha: REST como modelo de web service; TypeScript no back-end; React no front-end web; React Native com Expo no cliente móvel híbrido; Supabase Realtime como middleware de mensageria; filtros de canal como estratégia de concorrência; TanStack Query e Cockatiel para tratamento de erros; Vitest, Playwright e Maestro para testes; Vercel e Render para hospedagem; PostgreSQL como banco de dados.
- Criação de uma estrutura inicial de repositório em ambiente próprio, posteriormente consolidada no repositório oficial em 28/08.

### Semana 2 (25/08 - 31/08)

**Lean Inception e decisões de arquitetura iniciais** 

- `docs/1.apresentacao.md` — apresentação e contexto do projeto, delimitação do problema em suas duas frentes, objetivo geral e seis objetivos específicos da descrição arquitetural, e glossário com 15 termos e abreviaturas.
- `docs/2.nosso_produto.md` — visão do produto, quadros “É / Não é” e “Faz / Não faz”, definição do MVP e detalhamento das três personas.
- `docs/3.requisitos.md` — doze requisitos funcionais (RF001 a RF012) priorizados a partir do sequenciador MoSCoW e distribuídos entre as sprints; onze requisitos não-funcionais (RNF001 a RNF011); sete restrições arquiteturais; e a tabela de mecanismos arquiteturais nos três estados de análise, design e implementação, acompanhada das justificativas de cada decisão.
- `docs/4.modelagem.md` — jornada do usuário em cinco etapas e nove histórias de usuário associadas às personas.
- `README.md` e `docs/README.md` — identificação do projeto, resumo, integrantes e tabela de ferramentas e ambientes.

 **Orientadores e restauração do template nas seções 4.2 e 4.3** 

- Inclusão dos três orientadores no `README.md` e no sumário de `docs/README.md`.
- Restauração do conteúdo original do template nas seções 4.2 (Visão Lógica) e 4.3 (Modelo de dados), cujos diagramas foram programados para a Sprint 3.

**Termo de Abertura do Projeto (TAP 001)** 

- Identificação do projeto, gerência, cliente, objetivo, benefícios e requisitos de qualidade ancorados nos RNF001 a RNF011.
- Escopo preliminar a partir do MoSCoW, contra-escopo, oito entregas previstas e condições para início do projeto.
- Estimativa de prazo de 306 horas, correspondente a 17 semanas de projeto por 6 horas semanais por integrante, com início em 04/08/2026 e término em 01/12/2026.
- Estimativa de custo de R$ 0,00, justificada pela mão de obra acadêmica não remunerada e pela utilização integral de serviços em plano gratuito.
- Registro das partes interessadas, com os três integrantes e os três orientadores.

**Decisões de gerência tomadas na semana**

- A Seção 1 não incluiria estatísticas de mercado sem fonte citável.
- O projeto seria registrado como acadêmico sem parceiro externo, com os professores no papel de cliente e avaliador.

---

# Sprint 3

### Semana 1 (01/09 - 08/09)

**Visão Lógica e modelo de dados (PB15)**

- `docs/4.modelagem.md` — elaboração dos quatro diagramas do documento de arquitetura, em Mermaid, versionados junto ao próprio Markdown:
  - Figura 1, visão geral da solução, do interesse declarado pelo usuário até o direcionamento ao canal oficial de compra;
  - Figura 2, diagrama de classes, com oito classes de domínio, seus atributos, métodos e cardinalidades;
  - Figura 3, diagrama de componentes, com a distinção entre os componentes reutilizados e os que serão desenvolvidos, e o mapeamento de cada um aos requisitos não-funcionais correspondentes;
  - Figura 4, diagrama de entidade e relacionamento, com sete entidades, chaves primárias e estrangeiras, e a justificativa de duas decisões de modelagem.
- Substituição das imagens de exemplo herdadas do template e remoção das legendas que atribuíam ao grupo a autoria de figuras que não eram do grupo.

**Correção da Visão do Produto**

- `docs/2.nosso_produto.md` — ajuste da subseção 2.1 para as sete lacunas do template de Visão do Produto da Lean Inception, que estavam reduzidas a seis por fusão dos campos "O [nome do produto]" e "é um [categoria do produto]".

**Substituição do middleware de mensageria**

- Revisão da decisão arquitetural de mensageria após o veto da disciplina ao uso do Supabase, por abstrair o trabalho arquitetural que o projeto deve demonstrar. A camada passou a ser explícita e dividida em três responsabilidades: RabbitMQ, hospedado no CloudAMQP, como middleware de mensageria, com *topic exchange* roteando cada notificação por chave de interesse e filas duráveis com *ack* e *dead letter queue*; gateway Socket.IO no back-end, consumindo as filas e mantendo conexão persistente com cada cliente; e PostgreSQL gerenciado no Neon, desacoplado da mensageria.
- Atualização dos mecanismos arquiteturais e das justificativas em `docs/3.requisitos.md`, da tabela de ferramentas em `docs/README.md`, da lista de tecnologias e das variáveis de ambiente no `README.md`, da linha de custo do Termo de Abertura e dos itens PB10, PB22 e PB24 do Product Backlog.

**Apresentação da Visão do Produto**

- Preparação dos slides de problema, público-alvo e proposta de valor, seguindo a abordagem de Lean Inception, incluindo o levantamento e a verificação das evidências utilizadas.

**Decisões de gerência tomadas na semana**

- Os relatórios de contribuição das sprints anteriores não seriam reescritos após a troca do middleware, por serem registros datados das decisões vigentes à época.
- O caso utilizado como evidência do problema seria aquele em que havia ingresso disponível e faltou aviso, e não o de escassez de estoque, por ser o que corresponde ao problema que o produto resolve.

---

# Sprint 4

### Semana 1 (15/09 - 21/09)

**Cliente web — cadastro, login e sessão autenticada (PB23, PB32, RF001)** (`code/front`)

- Criação do cliente web em React + TypeScript + Vite, consumindo a API real desde o primeiro commit.
- Cliente HTTP centralizado (`src/lib/api.ts`), que repassa à tela as mensagens de erro produzidas pelo back-end, e sessão do usuário via Context API (`src/lib/auth-context.tsx`), com o token persistido no navegador.
- Telas de início, cadastro, login e área autenticada, com a proteção das rotas privadas (`ProtectedRoute.tsx`).

**Avaliação heurística (PB17)** (`docs/6.avaliacao_heuristica.md`)

- Avaliação heurística de usabilidade sobre o protótipo de referência de UX (Lovable), com os problemas encontrados e as evidências, e registro de que ela deve ser revisitada quando o protótipo em Figma (PB16) existir.
- Atualização do status dos itens da Sprint 3 no Product Backlog, com a nota sobre o estágio real de PB20–PB23.

**Revisão e integração**

- Revisão e merge das Pull Requests #47 (back-end de autenticação) e #48 (front-end de autenticação).

### Semana 2 (22/09 - 28/09)

**Catálogo de eventos — back-end (PB37–PB39, PB41, RF003, RF006)** (`code/back`)

- Tabelas `eventos` e `ofertas` no schema, com índices para a busca por categoria e data.
- Rotas públicas `GET /api/eventos` (busca por nome, categoria e data) e `GET /api/eventos/:id` (detalhe do evento com suas ofertas), com validação das entradas e 404 para evento inexistente.
- Script de ingestão manual do catálogo (`scripts/seed-eventos.ts`, `npm run db:seed`), com eventos de exemplo e links para plataformas reais de venda de ingresso.
- Testes automatizados do módulo de eventos (`test/eventos.schemas.test.ts`, `test/eventos.service.test.ts`).

**Catálogo de eventos e layout do protótipo — front-end** (`code/front`)

- Telas "Descobrir" (`Eventos.tsx`), com busca e filtros por categoria e data, e de detalhe do evento (`EventoDetalhe.tsx`), com as ofertas e o botão que leva ao canal oficial de compra.
- Aplicação do layout do protótipo de referência em todo o cliente web: cabeçalho, card de evento, estados de carregamento, ícones e reestilização das telas de início, feed, interesses, login e cadastro.
