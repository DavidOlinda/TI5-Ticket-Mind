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
