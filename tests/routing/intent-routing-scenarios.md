# DIF Runtime Routing Scenarios

These conceptual scenarios validate operational routing without adding a new workflow.

| ID | Input | Expected Primary Mode | Required routing outcome |
| --- | --- | --- | --- |
| 01 | Recebi esse briefing do Product Manager. Analise antes de começarmos o Design. | Analyze Brief | Do not start UI Design. |
| 02 | Precisamos entender por que os usuários abandonam essa etapa antes de redesenhar. | Discovery | Do not start a visual solution. |
| 03 | Crie o fluxo de recuperação de senha. | User Flow | Do not produce complete UI. |
| 04 | Transforme esse fluxo aprovado em wireframes. | Wireframe | Verify the required flow is available. |
| 05 | Agora transforme esses wireframes aprovados em interface final. | UI Design | Inspect Design System context when needed. |
| 06 | Avalie essa interface e identifique problemas antes de enviarmos para desenvolvimento. | Design Review | Determine supporting reviews from scope and gates; do not load all reviews by default. |
| 07 | Verifique se essa interface atende aos requisitos de acessibilidade. | Accessibility Review | Do not execute Discovery or Wireframe. |
| 08 | Confira se essa tela está usando corretamente nosso Design System. | Design System Review | Treat unknown Design System identity as a potential blocking context gate. |
| 09 | Não encontramos componente para esse padrão. Crie um novo componente reutilizável. | Component Creation | Confirm gap and apply component governance before authoring. |
| 10 | Essas telas foram aprovadas. Prepare o material para desenvolvimento. | Handoff | Verify handoff prerequisites. |
| 11 | Faça a validação final antes de liberar isso para implementação. | Final Validation | Run only checks required by the gate. |
| 12 | Transforme essas decisões de produto em um PRD. | PRD Generator | Do not start UI Design. |
| 13 | Faça uma crítica estruturada dessa solução. | Design Critique | Keep distinct from Design Review. |
| 14 | O projeto terminou. Quero registrar aprendizados e melhorias para o próximo ciclo. | Retrospective | Route to retrospective. |
| 15 | Melhore essa tela. | Ambiguous | Inspect context; ask only if material interpretations remain. |
| 16 | Analise este fluxo de usuário. Workspace inexistente. | User Flow analysis | Do not block solely for absent Workspace. |
| 17 | Crie a interface final. Nenhum Design System identificável. | UI Design | Do not invent a Design System; determine whether evidence is blocking. |
| 18 | Analise o briefing, crie o fluxo e depois faça os wireframes. | Sequential | Analyze Brief → User Flow → Wireframe only. |
| 19 | Usando o Design System identificado neste projeto, revise esta tela apenas quanto à consistência dos componentes. | Design System Review | Use the identified library without unnecessary confirmation. |
| 20 | Revise apenas acessibilidade. Não altere o layout. | Accessibility Review | Respect the scope limit; do not redesign. |
