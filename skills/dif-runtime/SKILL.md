---
name: dif-runtime
description: Runtime operacional para Product Design, UX, UI, Design System, documentação e validação. Use esta Skill quando a tarefa envolver análise de brief, discovery, user flow, wireframe, UI design, design review, acessibilidade, auditoria de Design System, criação de componentes, handoff, documentação, workshops, PRDs, crítica de design ou retrospectiva. Quando houver link do Figma, use o Figma MCP para inspecionar o arquivo ou frame.
compatibility: Requires Figma MCP for Figma-related tasks.
---

# DIF Runtime

## Objetivo

Executar tarefas de Product Design usando os módulos localizados na pasta `agents/`.

Esta Skill funciona como ponto de entrada e orquestrador. Não deve executar todos os módulos em todas as tarefas. Deve selecionar apenas os módulos necessários conforme a solicitação.

## Hierarquia de autoridade

Quando houver conflito entre instruções do Runtime, aplique esta ordem:

1. solicitação explícita do usuário;
2. `SKILL.md`;
3. fonte oficial do projeto e Design System publicado;
4. `DESIGN.md`;
5. regras permanentes `agents/00-system.md` a `agents/04-workspace-context.md`;
6. módulo de execução aplicável `agents/10-*.md` a `agents/25-*.md`.

Regras de nível inferior não podem autorizar automaticamente uma ação bloqueada por nível superior.

Quando a autoridade entre fontes do projeto não puder ser determinada, registre como inconclusiva e não invente uma resolução.

## Uso do Figma MCP

Quando o usuário fornecer um link do Figma:

1. Use o servidor MCP `figma`.
2. Faça inicialmente uma inspeção somente leitura.
3. Identifique arquivo, página, frame e node selecionado.
4. Leia componentes, component sets, variables, styles, Auto Layout e hierarquia quando forem relevantes.
5. Não altere o arquivo sem solicitação explícita.
6. Não classifique componentes por aparência ou nomenclatura apenas.
7. Priorize component key, component set key, origem local ou remota e biblioteca de origem.
8. Quando a origem não puder ser confirmada, classifique como inconclusiva.

## Seleção de módulos

Consulte os arquivos abaixo conforme a intenção da tarefa.

### Regras permanentes

Sempre consulte:

- `agents/00-system.md`
- `agents/01-runtime-rules.md`
- `agents/02-decision-tree.md`
- `agents/03-component-policy.md`
- `agents/04-workspace-context.md`

### Módulos de execução

Use somente quando aplicável:

- Análise de brief: `agents/10-analyze-brief.md`
- Discovery: `agents/11-discovery.md`
- User flow: `agents/12-user-flow.md`
- Wireframe: `agents/13-wireframe.md`
- UI design: `agents/14-ui-design.md`
- Design review: `agents/15-design-review.md`
- Accessibility review: `agents/16-accessibility-review.md`
- Design System review: `agents/17-design-system-review.md`
- Criação de componente: `agents/18-component-creator.md`
- Handoff: `agents/19-handoff.md`
- Documentação: `agents/20-documentation.md`
- Workshop: `agents/21-workshop.md`
- Validação final: `agents/22-final-validation.md`
- PRD: `agents/23-prd-generator.md`
- Crítica de design: `agents/24-design-critique.md`
- Retrospectiva: `agents/25-retrospective.md`

## Regras de roteamento

### Quando o usuário pedir análise de uma tela

Use:

1. `15-design-review.md`
2. `16-accessibility-review.md`, quando acessibilidade fizer parte do escopo
3. `17-design-system-review.md`
4. `22-final-validation.md`, quando houver avaliação conclusiva

### Quando o usuário pedir auditoria de Design System

Use:

1. `11-discovery.md`
2. `17-design-system-review.md`
3. `15-design-review.md`
4. `22-final-validation.md`

### Quando o usuário pedir criação ou melhoria de interface

Use conforme necessário:

1. `10-analyze-brief.md`
2. `11-discovery.md`
3. `12-user-flow.md`
4. `13-wireframe.md`
5. `14-ui-design.md`
6. `15-design-review.md`
7. `22-final-validation.md`

Não execute fases desnecessárias para tarefas pequenas.

### Quando o usuário pedir criação de componente

Use:

1. `03-component-policy.md`
2. `17-design-system-review.md`
3. `18-component-creator.md`
4. `20-documentation.md`
5. `22-final-validation.md`

Não crie componentes, variables, tokens, foundations ou padrões novos sem aprovação explícita.

## Política de continuidade

Problemas não críticos não devem interromper uma tarefa aprovada.

Continue normalmente ao encontrar:

- ausência de Auto Layout;
- componentes manuais;
- inconsistências visuais não críticas;
- nomenclaturas inadequadas;
- oportunidades de padronização;
- espaços vazios;
- melhorias que não alterem a arquitetura.

Registre esses itens como observações ou riscos.

Interrompa apenas quando a tarefa exigir:

- criação de novo componente;
- alteração de variables ou tokens;
- alteração de foundations;
- mudança na arquitetura do Design System;
- criação de novo padrão;
- alteração de fluxo principal;
- decisão de Produto, negócio ou arquitetura.

Nesse caso, use:

`STATUS: Escalar para o Coordenador`

## Classificação de componentes

Use esta taxonomia universal:

- Design System confirmado
- Design System provável
- Versão divergente
- Remoto não identificado
- Local específico da tela
- Desconectado
- Origem inconclusiva

Nunca associe automaticamente origem local ou remota a uma biblioteca específica.

A ordem de evidência deve ser:

1. component key ou component set key;
2. biblioteca ou arquivo de origem;
3. main component;
4. origem local ou remota;
5. nomenclatura;
6. aparência visual.

## Escrita no Figma

Antes de alterar o Figma:

1. Confirme que o usuário solicitou explicitamente uma mudança.
2. Delimite o frame, página ou conjunto de nós afetados.
3. Evite mudanças fora do escopo.
4. Não substitua componente remoto com origem inconclusiva.
5. Não altere variables, tokens ou foundations sem aprovação.
6. Após a execução, valide o resultado.

## Formato de saída

Quando aplicável, entregue:

- status;
- resumo;
- evidências;
- achados;
- riscos;
- decisões necessárias;
- ações executadas;
- validação final.

Status permitidos:

- Ready
- Ready with Adjustments
- Proceed with Caution
- Escalar para o Coordenador
- Blocked

## Design Context

Para qualquer tarefa que envolva UI, Design System, componentes,
foundations, revisão visual, acessibilidade ou criação no Figma:

1. Consulte `DESIGN.md`.
2. Trate suas regras como contexto persistente de design.
3. Não invente regras ausentes.
4. Quando houver conflito entre `DESIGN.md` e o Design System publicado,
   registre o conflito e priorize a fonte oficial definida pelo projeto.

