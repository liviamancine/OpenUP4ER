# Tarefa: Definir a Visão (Passos)

**Descrição:**  
Definir a visão da explicabilidade, em alto nível, e os problemas relacionados à compreensão das decisões do sistema de AM, os stakeholders afetados, os objetivos da explicabilidade e os limites iniciais que guiarão as iterações futuras.

Observação:
- o problema de explicabilidade já foi reconhecido fora do OpenUP4RE (escopo do projeto)
- o OpenUP4RE começa quando há a necessidade explícita de explicabilidade
- o foco inicial é alinhamento entre stakeholders, necessidades explicativas e contexto.

[Disciplina: Requisitos](requisitos.md)

**Objetivo**
A solução é proposta para abordar o problema de falta de confiança, transparência e compreensibilidade nas decisões produzidas pelo sistema de AM. Os Stakeholders colaboram com a equipe de desenvolvimento para expressar e documentar suas necessidades de explicação, seus critérios de confiança e os tipos de informações que precisam compreender. Esse alinhamento permite que a equipe do projeto obtenha uma visão clara sobre como a explicabilidade deve ser integrada ao sistema e quais mecanismos devem ser implementados para atendê-los.

## Relacionamentos

**Papéis**  
- **Responsável:** [Engenheiro de Requisitos](../papeis/engenheiro-requisitos.md)  
- **Executores Adicionais:** [Arquiteto de Software](../papeis/arquiteto-software.md), [Gerente de Projetos](../papeis/gerente-projeto.md), 
[Especialista Ética](../papeis/especialista-etica-regulacao) e [Stakeholders](../papeis/stakeholders)

**Entradas**  
- **Obrigatório:**  
  - Escopo do Projeto
  - Necessidade da Explicabilidade Reconhecida
- **Opcional:**  
  - [Lista de Item de Trabalho](#) 
  - [Visão Explicabilidade](../artefatos/TEMPLATE-definir.visao.md)
- **Saídas Intermediárias:**  
  - [Glossário](#)
  - [Lista de Item de Trabalhos](#)
  - [Visão Explicabilidade](../artefatos/TEMPLATE-definir.visao.md)
- **Saída Principal**
  - [Documento de Requisitos de Explicabilidade - DRE](../artefatos/DRE.md)
---
## Passos
***1. Identificar Stakeholders e Necessidades de Explicabilidade***

**O que fazer**

Formalizar e alinhar a necessidade de explicabilidade já reconhecida no projeto, identificando quais stakeholders precisam de explicações, por que precisam, e que tipo de explicação é necessária no contexto do sistema de Aprendizado de Máquina.

Nesta etapa, o objetivo não é descobrir o problema do projeto, mas:
- consolidar o problema de explicabilidade associado ao uso do sistema
- identificar os stakeholders que necessitam compreender, auditar ou validar as decisões do modelo
- caracterizar as necessidades explicativas iniciais, que irão orientar a Visão da Explicabilidade

**Quem**

- Engenheiro de Requisitos (líder), com apoio do Gerente de Projeto e validação dos stakholders-chave.

**Onde registrar**

[Documento de Visão de Explicabilidade](../artefatos/TEMPLATE-definir.visao.md):
- Seção 2.2 — Declaração de Posicionamento da Explicabilidade
- Seção 3.1 — Resumo dos Stakeholders

**Boas Práticas**

- Tratar esta atividade como ponto de partida do OpenUP4RE, assumindo que a necessidade de explicabilidade já existe.
- Evite propor solução antes de concordar sobre o problema.
- Trabalhe com exemplos reais do domínio para aumentar clareza.
- Garantir alinhamento terminológico com o glossário de explicabilidade ([relacionar ao glossário](TEMPLATE-glossario.md)).
- Revisar a declaração do problema ao final de cada iteração, se necessário.

  *Perguntas úteis*
- Quem precisa entender as decisões do sistema?
- Para qual finalidade (uso operacional, validação, auditoria, pesquisa, conformidade)?
- Em quais situações a falta de explicabilidade causa problemas?


***2. Adquirir consenso sobre o problema (não pule para soluções)***

**O que fazer**

- Conduzir workshops, entrevistas para definir qual é o problema de explicabilidade (p. ex. “não entendemos porque o modelo me fornece um resultado positivo”).
- Trabalhar o “problema por trás do problema” — identificar consequências (confiança, retrabalho, não conformidade).

**Quem**

- Engenheiro de Requisitos (facilitador), Stakeholders.

**Onde registrar**

- [Documento de Visão da Explicabilidade](../artefatos/TEMPLATE-definir.visao.md) → seção 4.1 Necessidades e Funcionalidades 
- [Itens gerados para Lista de Itens de Trabalho](Verificar)

**Boas Práticas**

-  [Guidaline: Técnica para obtenção de requisitos de explicabilidade](VERIFICAR)
---
***3. Capturar um vocabulário comum (glossário)***

**O que fazer**

Cada projeto envolvendo sistemas de Aprendizado de Máquina possui um conjunto de termos específicos relacionados à explicabilidade que precisam ser compreendidos por todos os stakeholders. Um glossário de explicabilidade garante uma comunicação clara ao longo do projeto e evita interpretações divergentes sobre conceitos técnicos, éticos e funcionais.

Trabalhe com os stakeholders para criar e manter um glossário que defina termos utilizados no contexto de explicabilidade, incluindo técnicas de interpretação, métricas, tipos de explicações, conceitos regulatórios e terminologia do domínio. Este glossário deve ser expandido e refinado continuamente durante todo o ciclo de vida do projeto, acompanhando a evolução do entendimento sobre o comportamento do modelo e das necessidades de explicação dos usuários.

- Construir um glossário com termos centrais: explicabilidade, interpretabilidade, local/global, saliência, confiança, rastreabilidade, mapa de calor, etc.
- Validar termos com stakeholders para evitar ambiguidade.

**Quem**

Engenheiro de Requisitos

**Onde registrar**

[Glossário](../artefatos/TEMPLATE-glossario.md) 

**Boas práticas**

O glossário é uma lista simples em ordem alfabética dos termos do domínio e suas definições. É importante cobrir três dimensões fundamentais:
- Terminologia técnica da área de explicabilidade - técnicas, métricas, tipos de explicação
- Terminologia de stakeholders e papéis explicáveis - quem recebe explicações e como usa
- Terminologia do domínio do problema: específica ao contexto de aplicação

---
***4. Obtenha as solicitações dos Stakeholders (elicitação focada em explicabilidade)***

**O que fazer**

- Planejar técnicas de elicitação: entrevistas, questionários, card-sorting para formatos de explicação, protótipos de baixa fidelidade. 
- Capturar requisitos funcionais e não funcionais de explicabilidade (quem, quando, como, nível de detalhe, tempo de resposta).

**Quem**

- Engenheiro de Requisitos (conduz), Stakeholders e UX Designer (para protótipos)

**Onde registrar**

- [Descrever os Requisitos](../tarefas/documento-requisito.md) → 4.1 Necessidades e Funcionalidades
- Lista de Itens de Trabalho [cada requisito vira item rastreável](VALIDAR)

**Boas práticas**

Se você puder se encontrar pessoalmente com os Stakeholders, então você poderá conduzir uma entrevista ou uma sessão de brainstorming. Esta colaboração face-a-face é extremamente valiosa e reduz as possibilidades da equipe de projeto não entender as necessidades dos Stakeholders. Alguns requisitos podem já ter sido documentados em uma [Lista de Itens de Trabalho existente](VERIFICAR). Isto pode normalmente ser usado como um sólido ponto de partida do qual um conjunto completo de requisitos de explicabilidade possa ser criado.

Qualquer requisito obtido durante esta etapa deve ser capturado na [Lista de Itens de Trabalho existente](VERIFICAR). Para mais informações, veja Tarefa: [Encontrar e Descrever os Requisitos](VERIFICAR).

*Perguntas/artefatos*

Que informação é necessária para você confiar numa decisão automática?

Exemplo: protótipo com explicação textual + visual para avaliar preferências.

---
***5. Definir os limites da Explicabilidade***

**O que fazer**

Especificar até onde a explicabilidade deve chegar: quais decisões, quais módulos, para quais stakeholders.
Identificar interfaces onde as explicações aparecem (UI, API, relatórios) e entradas/saídas relacionadas.
Essa delimitação estabelece o escopo da explicabilidade, distinguindo os elementos do sistema que exigem mecanismos explicativos daqueles que não fazem parte do requisito.

Devem ser identificadas:
- As decisões, recomendações ou previsões do sistema que requerem explicação
- Os perfis de stakeholders que receberão explicações (por exemplo, usuários finais, especialistas de domínio, auditores)
- Os tipos de explicação esperados (local, global, textual, visual, simbólica)
- Os pontos de interação onde a explicação será apresentada

As informações de entrada e saída envolvidas no processo explicativo, incluindo dados, atributos relevantes e resultados do modelo.

**Quem**

Engenheiro de Requisitos, Arquiteto de Software e Gerente de Projeto.

**Onde registrar**

- Veja Tarefa: [Checklist para delimitar explicabilidade](../tarefas/checklist-explicabilidade.md)

---

***6. Identificar as restrições no sistema (impactos para explicabilidade)***

**O que fazer**

Levantar restrições: regulatórias (LGPD, requisitos de auditoria), técnicas (modelo utilizados), qualidade (qualidade esperada para as explicações), econômicas (custo de geração de explicações), temporais (latência aceitável), compatibilidade (plataformas).

**Quem**

Engenheiro de Requisitos, Gerente de Projeto, Arquiteto e especialista em ética e regulação (se houver).

**Onde registrar**

[Documento de Visão da Explicabilidade](../tarefas/documento-requisito.md) → seção 4.1 Necessidades e Funcionalidade e 5. Outros Requisitos do Produto (Explicabilidade)


---
***7. Obter consenso (revisão da Visão)***

**O que fazer**

- Fazer revisão formal da Visão da Explicabilidade com stakeholders e time técnico; coletar aprovações, feedbacks e registrar decisões.
- Ajustar [Documento de Visão de Explicabilidade](../tarefas/documento-requisito.md), conforme consenso.

**Quem**

Engenheiro de Requisitos (facilitador), Stakeholders, Gerente de Projeto, Arquiteto.

**Onde registrar**

- [Documento de Visão de Explicabilidade](../tarefas/definir-visao.md) (versão aprovada)

**Boas Práticas**

- [VAMOS TER UM DOCUMENTO INDICANDO BOAS PRÁTICAS?](#)

---

## Informações Adicionais

**Listas de Verificação:**  
- [Documento de Visão de Explicabilidade](../tarefas/documento-requisito.md) 

**Conceitos:**  
- [Requisitos](#)

  **Diretrizes:**  
- [Revisão eficaz de Requisitos](#)
- [Técnicas Para Obtenção de Requisitos de Explicabilidade](#)
---
**Referências:**  
- [Link para o OpenUP Original](file:///C:/Users/Livia%20Mancine/Downloads/OpenUP/Publish/openup/tasks/define_vision_9D36CF2F.html)

