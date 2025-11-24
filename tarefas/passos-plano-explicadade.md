# Tarefa: Plano para Explicabilidade (Passos)

**Descrição:**  
Uma tarefa colaborativa que estabelece o acordo inicial sobre como o projeto irá incorporar, desenvolver e validar a explicabilidade ao longo do seu ciclo de vida.

O Plano de Explicabilidade resultante fornece uma visão geral resumida de como o requisito de explicabilidade será tratado.

**Objetivo**
Obter a aprovação dos Stakeholders para iniciar o tratamento da explicabilidade como um requisito não funcional essencial do projeto e garantir o compromisso da equipe para executá-lo ao longo de todas as fases do desenvolvimento.

O Plano de Explicabilidade descreve quando, como e por quem as atividades relacionadas à explicabilidade serão realizadas. Assim como no OpenUP original, este plano pode — e deve — ser atualizado continuamente conforme surgirem novas descobertas, feedback dos usuários, resultados de validações iterativas, ou mudanças no ambiente regulatório, técnico ou organizacional.

## Relacionamentos

**Papéis**  
- **Responsável:** [Gerente de Projetos](../papeis/gerente-projeto.md)  
- **Executores Adicionais:** [Engenheiro de Requisitos](engenheiro-requisito.md), [Arquiteto de Software](../papeis/arquiteto-software.md), [Desenvolvedor](../papeis/gerente-projeto.md), 
[Especialista Ética](../papeis/especialista-etica-regulacao) e [Stakeholders](../papeis/stakeholders)

**Entradas**  
- **Obrigatório:**  
  - Nenhum
- **Opcional:**  
  - [Lista de Item de Trabalho](#) 
  - [Visão Explicabilidade](../artefatos/visao-explicabilidade.md) 
- **Saída de:**  
  - [Glossário](#)
  - [Lista de Item de Trabalhos](#)
  - [Visão Explicabilidade](../artefatos/visao-explicabilidade.md)
---
## Passos
***1. Identificar os Stakeholders (foco: explicabilidade)***

**O que fazer**
- Mapear pessoas/grupos/perfis que precisam receber, entender ou auditar explicações (veja Papéis)[../papeis].
- Para cada stakeholder, registrar: objetivos, que tipo de explicação precisa (local/global, técnico/resumido), nível de detalhe e canais (UI, relatório, API).

**Quem**
- Engenheiro de Requisitos (líder) com apoio do Gerente de Projeto.

**Onde registrar**

[Documento de Visão de Explicabilidade](../tarefas/definir.visao.md) → seção 3.1 - Resumo dos stakeholders

**Boas Práticas**

*Perguntas úteis*
- Quem precisa entender as decisões do sistema? Por quê?
- Que formato de explicação cada perfil prefere (texto resumido, relatório técnico, visualização)?
- Com que frequência precisam das explicações?

***2. Adquirir consenso sobre o problema (não pule para soluções)***

**O que fazer**
- Conduzir workshops, entrevistas para definir qual é o problema de explicabilidade (p. ex. “não entendemos porque o modelo me fornece um resultado positivo”).
- Trabalhar o “problema por trás do problema” — identificar consequências (confiança, retrabalho, não conformidade).

**Quem**
- Engenheiro de Requisitos (facilitador), Stakeholders.

**Onde registrar**

- [Documento de Visão da Explicabilidade](../tarefas/definir.visao.md) → seção 4.1 Necessidades e Funcionalidades 
- [Itens gerados para Lista de Itens de Trabalho](Verificar)

**Boas Práticas**

-  [Guidaline: Técnica para obtenção de requisitos de explicabilidade](VERIFICAR)
---
***3. Capturar um vocabulário comum (glossário)***

**O que fazer**
- Construir um glossário com termos centrais: explicabilidade, interpretabilidade, local/global, saliência, confiança, rastreabilidade, etc.
- Validar termos com stakeholders para evitar ambiguidade.

**Quem**
Engenheiro de Requisitos

**Onde registrar**

[Glossário](../tarefas/#) e seção do [DRE](VERIFICAR).

**Boas práticas**
O glossário é uma lista simples em ordem alfabética dos termos do domínio e suas definições.

---
***4. Obter solicitações dos Stakeholders (elicitação focada em explicabilidade)***

**O que fazer**

- Planejar técnicas de elicitação: entrevistas, questionários, card-sorting para formatos de explicação, protótipos de baixa fidelidade.
- Capturar requisitos funcionais e não funcionais de explicabilidade (quem, quando, como, nível de detalhe, tempo de resposta).

**Quem**
- Engenheiro de Requisitos (conduz), Stakeholders, UX Designer (para protótipos)(VALIDAR)

**Onde registrar**

- [Descrever os Requisitos](../tarefas/documento-requisito.md) → Documento de Requisitos de Explicabilidade
- Lista de Itens de Trabalho (cada requisito vira item rastreável)(VALIDAR)

**Boas práticas**
Se você puder se encontrar pessoalmente com os Stakeholders, então você poderá conduzir uma entrevista ou uma sessão de brainstorming. Esta colaboração face-a-face é extremamente valiosa e reduz as possibilidades da equipe de projeto não entender as necessidades dos Stakeholders. Alguns requisitos podem já ter sido documentados em uma [Lista de Itens de Trabalho existente](VERIFICAR). Isto pode normalmente ser usado como um sólido ponto de partida do qual um conjunto completo de requisitos de explicabilidade possa ser criado.

Qualquer requisito obtido durante esta etapa deve ser capturado na [Lista de Itens de Trabalho existente](VERIFICAR). Para mais informações, veja Tarefa: [Encontrar e Descrever os Requisitos](VERIFICAR).

*Perguntas/artefatos*

Que informação é necessário para você confiar numa decisão automática?

Exemplo: protótipo com explicação textual + visual para avaliar preferências.

---
***5. Definir os limites da Explicabilidade***

**O que fazer**

Especificar até onde a explicabilidade deve chegar: quais decisões, quais módulos, para quais stakeholders.
Identificar interfaces onde as explicações aparecem (UI, API, relatórios) e entradas/saídas relacionadas.

**Quem**

Engenheiro de Requisitos + Arquiteto de Software + Gerente de Projeto.

**Onde registrar**

- Veja Tarefa: [Encontrar e Descrever os Requisitos](VERIFICAR).
- [História de Usuários](#) é uma técnica que pode ser útil na definição do limite da Explicabilidade.
---

***6. Identificar as restrições no sistema (impactos para explicabilidade)***

**O que fazer**

Levantar restrições: regulatórias (LGPD, requisitos de auditoria), econômicas (custo de geração de explicações), técnicas (modelo utilizados), temporais (latência aceitável), compatibilidade (plataformas).

**Quem**

Engenheiro de Requisitos + Gerente de Projeto + Arquiteto + especialista em ética e regulação (se houver).

Onde registrar

[Documento de Visão da Explicabilidade](../tarefas/definir.visao.md): seção 4.1 Necessidades e Funcionalidade e 5. Outros Requisitos do Produto (Explicabilidade)


---
***7. Obter consenso (revisão da Visão)***

**O que fazer**

- Fazer revisão formal da Visão da Explicabilidade com stakeholders e time técnico; coletar aprovações, feedbacks e registrar decisões.
- Ajustar [Documento de Visão de Explicabilidade](../tarefas/definir-visao.md) e [Lista de Itens](VALIDAR) conforme consenso.

**Quem**

Engenheiro de Requisitos (facilitador), Stakeholders, Gerente de Projeto, Arquiteto.

**Onde registrar**

- [Documento de Visão de Explicabilidade](../tarefas/definir-visao.md) (versão aprovada)

**Boas Práticas**

- [VAMOS TER UM DOCUMENTO INDICANDO BOAS PRÁTICAS?](#)

---

## Informações Adicionais

**Listas de Verificação:**  
- [Documento de Visão de Explicabilidade](../tarefas/definir-visao.md)

**Conceitos:**  
- [Requisitos](#)

  **Diretrizes:**  
- [Guidaline: Técnica para obtenção de requisitos de explicabilidade](VERIFICAR)
- [Glossário](glossario-explicabilidade.md)
- [Encontrar e Descrever os Requisitos](VERIFICAR)
---
**Referências:**  
- [Link para o OpenUP Original](file:///C:/Users/Livia%20Mancine/Downloads/OpenUP/Publish/openup/tasks/plan_the_project_A4A80C96.html)

