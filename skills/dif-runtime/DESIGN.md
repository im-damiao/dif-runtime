# DESIGN.md

## 1. Purpose

Este arquivo define o protocolo universal de contexto de design do DIF Runtime.

Seu objetivo é orientar agentes a descobrir, interpretar, aplicar e validar a linguagem de design existente no projeto atual.

Este arquivo não representa uma empresa, produto, marca ou Design System específico.

Não fixe valores, componentes, tokens, estilos, padrões ou decisões de uma organização como regra universal.

Sempre derive o contexto de design das fontes reais disponíveis no projeto.

## 2. Source of Truth

Antes de tomar decisões de UI ou Design System, identifique as fontes disponíveis.

Priorize evidências nesta ordem quando aplicável:

1. Design System publicado e atualmente utilizado pelo projeto.
2. Variables, tokens e styles publicados.
3. Componentes e component sets oficiais.
4. Documentação oficial do produto ou Design System.
5. Padrões recorrentes confirmados no produto.
6. Artefatos e decisões aprovadas do projeto.
7. Interface existente, somente quando não houver fonte mais confiável.

Não trate aparência visual isolada como fonte suficiente.

Quando fontes entrarem em conflito:
- registre o conflito;
- identifique qual fonte é oficial ou mais atual;
- não resolva por preferência estética;
- escale quando a decisão exigir Produto, Design System ou governança.

## 3. Design Context Discovery

Antes de criar, revisar ou alterar uma interface, identifique quando disponível:

- empresa ou organização;
- produto;
- feature ou módulo;
- plataforma;
- usuários;
- contexto de uso;
- objetivo da interface;
- Design System;
- bibliotecas;
- foundations;
- variables;
- tokens;
- styles;
- componentes;
- component sets;
- padrões;
- breakpoints;
- requisitos de acessibilidade;
- restrições técnicas;
- decisões previamente aprovadas.

Quando uma informação relevante não estiver disponível, registre como lacuna.

Não invente contexto ausente.

## 4. Product Design Principles

Identifique os princípios de design existentes no projeto.

Verifique:
- prioridades de UX;
- princípios de produto;
- critérios de consistência;
- necessidades dos usuários;
- objetivos de negócio;
- restrições relevantes;
- decisões explicitamente aprovadas.

Quando princípios formais não existirem:
- não invente uma filosofia de produto;
- use evidências do projeto para orientar recomendações;
- diferencie claramente regra existente de recomendação.

## 5. Visual Language

Descubra a linguagem visual existente.

Identifique:
- hierarquia visual;
- densidade;
- superfícies;
- profundidade;
- uso de bordas;
- uso de elevação;
- tratamento de containers;
- padrões de composição;
- linguagem de ícones;
- tratamento de imagens quando aplicável.

Preserve padrões oficiais existentes.

Não introduza uma nova direção visual sem solicitação ou necessidade comprovada.

## 6. Colors

Inspecione:
- brand colors;
- neutral colors;
- semantic colors;
- variables;
- styles;
- primitive tokens;
- semantic tokens;
- component tokens;
- regras de contraste.

Regras:
- priorize tokens existentes;
- prefira tokens semânticos quando disponíveis;
- não invente novas cores;
- não substitua cores semânticas por cores de marca sem evidência;
- não use valores arbitrários quando existir token correspondente;
- valide contraste conforme os requisitos de acessibilidade do projeto.

Quando não houver sistema de cores suficiente, registre a lacuna.

## 7. Typography

Identifique:
- font family;
- escala tipográfica;
- pesos;
- line-height;
- letter spacing;
- headings;
- body;
- labels;
- captions;
- styles ou variables tipográficas.

Regras:
- reutilize estilos existentes;
- preserve hierarquia tipográfica;
- não crie uma nova escala sem necessidade comprovada;
- não introduza fontes ou pesos inexistentes sem aprovação;
- diferencie inconsistência existente de nova recomendação.

## 8. Spacing

Identifique:
- escala oficial;
- variables ou tokens;
- gaps;
- padding;
- espaçamento entre componentes;
- espaçamento entre seções;
- ritmo vertical.

Regras:
- use valores existentes quando disponíveis;
- priorize variables e tokens;
- evite valores arbitrários;
- não crie uma nova escala de spacing sem necessidade comprovada.

## 9. Radius

Identifique:
- escala de radius;
- tokens ou variables;
- regras por componente;
- exceções existentes.

Regras:
- reutilize valores oficiais;
- preserve consistência entre componentes equivalentes;
- não introduza novos níveis de radius por preferência estética.

## 10. Borders

Identifique:
- espessuras;
- cores;
- tokens;
- divisores;
- estados;
- padrões de separação visual.

Determine quando o sistema utiliza:
- border;
- background;
- divider;
- elevation;
- combinação desses recursos.

Não introduza padrões novos sem evidência.

## 11. Shadows and Elevation

Identifique:
- níveis de shadow;
- elevation;
- tokens;
- componentes que utilizam profundidade;
- contextos permitidos.

Regras:
- reutilize níveis existentes;
- não crie sombras decorativas arbitrárias;
- preserve a lógica de elevação do sistema.

## 12. Grid and Layout

Identifique:
- grid;
- containers;
- breakpoints;
- colunas;
- gutters;
- gaps;
- larguras máximas;
- margens;
- comportamento responsivo.

Regras:
- preserve a estrutura existente;
- não invente breakpoints;
- valide comportamento em diferentes tamanhos quando fizer parte do escopo;
- diferencie regras do Design System de decisões específicas da tela.

## 13. Design Tokens

Identifique quando disponíveis:
- primitive tokens;
- semantic tokens;
- component tokens;
- variables;
- collections;
- modes;
- nomenclatura;
- aliases.

Regras:
- priorize tokens semânticos;
- preserve aliases existentes;
- não invente tokens;
- não renomeie tokens sem solicitação;
- não altere arquitetura de tokens sem aprovação;
- quando um valor existir sem token correspondente, registre como possível lacuna, não como autorização automática para criar um token.

## 14. Component Usage

Antes de criar qualquer elemento de UI:

1. Inspecione componentes e component sets existentes.
2. Identifique componente, variante, propriedades e estados.
3. Confirme adequação semântica e funcional.
4. Reutilize instâncias conectadas quando adequadas.
5. Preserve propriedades e estrutura oficial.

Para cada componente relevante, determine quando disponível:
- quando usar;
- quando não usar;
- variantes;
- propriedades;
- estados;
- comportamento;
- composição;
- restrições;
- acessibilidade.

Não force reutilização quando o componente não atender adequadamente ao caso.

Não crie componente novo sem comprovar a lacuna e obter aprovação quando exigida pelo Runtime.

## 15. Forms

Identifique padrões existentes para:
- labels;
- helper text;
- placeholder;
- required;
- optional;
- validation;
- error;
- success;
- disabled;
- read-only;
- loading;
- seleção;
- agrupamento de campos.

Preserve padrões existentes.

Não use placeholder como substituto de label quando isso comprometer compreensão ou acessibilidade.

Considere prevenção, identificação e recuperação de erros.

## 16. Navigation

Identifique padrões existentes para:
- sidebar;
- header;
- breadcrumb;
- tabs;
- menus;
- page titles;
- navegação contextual;
- hierarquia de informação.

Regras:
- preserve modelos de navegação existentes quando adequados;
- não introduza uma nova arquitetura de navegação por preferência visual;
- valide localização, hierarquia e estado atual do usuário.

## 17. Data-heavy Interfaces

Quando o produto possuir interfaces densas em dados, identifique padrões para:
- tables;
- filters;
- search;
- sorting;
- pagination;
- selection;
- bulk actions;
- empty states;
- loading;
- error;
- density;
- overflow;
- responsive behavior.

Priorize legibilidade, escaneabilidade, eficiência e consistência.

Não simplifique informação necessária apenas para reduzir densidade visual.

## 18. Interaction Patterns

Identifique comportamento existente para:
- default;
- hover;
- focus;
- active;
- pressed;
- selected;
- disabled;
- loading;
- error;
- success;
- confirmation.

Regras:
- não entregue somente o estado ideal;
- preserve feedback consistente;
- valide comportamento e não apenas aparência;
- não invente interações quando o comportamento existente puder ser identificado.

## 19. Feedback

Identifique padrões existentes para:
- toast;
- alert;
- inline feedback;
- modal;
- confirmation;
- destructive actions;
- progress;
- loading;
- success;
- error.

Escolha o padrão conforme severidade, contexto e necessidade de ação.

Preserve terminologia e comportamento existentes quando forem oficiais.

## 20. Accessibility

Identifique os requisitos de acessibilidade do projeto.

Na ausência de regra mais específica, avalie conformidade com WCAG 2.2 AA quando aplicável ao produto e plataforma.

Considere:
- contraste;
- teclado;
- foco;
- ordem de foco;
- nomes acessíveis;
- labels;
- touch targets;
- screen readers;
- motion;
- reduced motion;
- mensagens de erro;
- recuperação;
- semântica;
- responsividade;
- conteúdo inclusivo.

Não considere acessibilidade apenas como validação final.

## 21. Motion

Identifique quando disponível:
- duration;
- easing;
- transitions;
- motion tokens;
- padrões de entrada e saída;
- feedback animado;
- reduced motion.

Regras:
- use motion com propósito funcional;
- preserve padrões existentes;
- não introduza animação decorativa arbitrária;
- respeite preferências de redução de movimento.

## 22. UX Writing

Identifique:
- idioma;
- tom;
- terminologia oficial;
- capitalização;
- labels;
- títulos;
- CTAs;
- mensagens de erro;
- confirmações;
- instruções;
- nomenclaturas de produto.

Regras:
- preserve terminologia existente e aprovada;
- priorize clareza;
- evite termos diferentes para a mesma ação ou conceito;
- não invente nomenclatura de negócio quando ela não estiver definida;
- use conteúdo realista quando houver contexto suficiente.

## 23. Do / Don't

Quando houver documentação oficial de boas práticas:
- aplique os exemplos existentes;
- preserve seus critérios;
- não transforme preferência visual em regra universal.

Quando não houver Do / Don't documentado:
- não invente regras como se fossem oficiais;
- registre recomendações separadamente das regras existentes.

## 24. Design System Gaps

Considere uma possível lacuna quando:
- nenhum componente existente atende adequadamente;
- um padrão recorrente não possui definição;
- valores são repetidos sem token correspondente;
- estados necessários não estão cobertos;
- comportamento relevante não está documentado;
- acessibilidade depende de solução improvisada;
- reutilização exige overrides frágeis;
- existe inconsistência recorrente entre produtos ou telas.

Uma lacuna não autoriza automaticamente criação.

Registre:
- evidência;
- impacto;
- recorrência;
- risco;
- recomendação.

## 25. AI Decision Rules

Sempre:
- use evidência acima de preferência estética;
- inspecione antes de criar;
- reutilize antes de propor algo novo;
- preserve componentes conectados;
- respeite Design System, tokens e padrões oficiais;
- diferencie regra, evidência, hipótese e recomendação;
- registre lacunas e conflitos;
- valide o resultado.

Nunca:
- invente tokens;
- invente componentes;
- invente bibliotecas;
- invente padrões;
- invente regras de marca;
- invente decisões de produto;
- trate aparência isolada como evidência suficiente;
- assuma que um padrão recorrente é oficial sem confirmação;
- substitua padrão oficial por preferência estética.

## 26. Conflict Resolution

Quando houver conflito entre fontes:

1. Identifique as fontes conflitantes.
2. Verifique qual é oficial, publicada e atual.
3. Registre a evidência.
4. Preserve a fonte oficial quando a autoridade estiver clara.
5. Quando a autoridade não puder ser determinada, classifique como inconclusivo.
6. Não altere foundations, tokens, componentes ou padrões para resolver o conflito sem aprovação.

## 27. Output Expectations

Quando uma tarefa utilizar este contexto, registre quando relevante:
- fontes de design inspecionadas;
- Design System identificado;
- foundations aplicadas;
- tokens utilizados;
- componentes reutilizados;
- padrões utilizados;
- lacunas encontradas;
- conflitos encontrados;
- decisões que exigem aprovação;
- nível de confiança.

## 28. Success Criteria

Este protocolo é bem-sucedido quando o agente:
- adapta-se ao projeto atual sem carregar identidade de outra empresa;
- identifica a fonte de verdade;
- usa o Design System real;
- respeita foundations e tokens existentes;
- reutiliza componentes adequados;
- identifica lacunas sem inventar soluções;
- diferencia regras oficiais de recomendações;
- mantém consistência visual, funcional e comportamental;
- considera acessibilidade;
- produz decisões rastreáveis e baseadas em evidências.

