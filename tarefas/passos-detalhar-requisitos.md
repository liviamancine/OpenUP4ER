# Tarefa: Detalhar os Requisitos (Passos)

[Disciplina: Requisitos](requisitos.md)


**Descrição:**  
Descrever como detalhar os requisitos de explicabilidade associados a sistemas baseados em Aprendizado de Máquina. Essa tarefa envolve a especificação clara e estruturada do que deve ser explicado, para quem, em quais situações e por meio de quais mecanismos, garantindo que os pontos de decisão relevantes do sistema sejam explicáveis de acordo com as necessidades e expectativas específicas dos stakeholders.

**Objetivo**
A finalidade desta tarefa é descrever um ou mais requisitos de explicabilidade com nível de detalhe suficiente para: validar a compreensão sobre o que deve ser explicado pelo sistema, assegurar o alinhamento com as expectativas dos stakeholders, e permitir o início do desenvolvimento e da integração dos mecanismos de explicação ao sistema baseado em AM.

Os requisitos de explicabilidade devem definir claramente os pontos de decisão que requerem explicação, os públicos-alvo das explicações, os níveis de detalhe esperados e as condições sob as quais as explicações devem ser disponibilizadas, apoiando o uso adequado, a confiança no sistema e a responsabilização sobre seu comportamento.

## Relacionamentos

**Papéis**  
- **Executor Principal:** [Engenheiro de Requisitos](../papeis/engenheiro-requisitos.md)  
- **Executores Adicionais:** [Arquiteto de Software](../papeis/arquiteto-software.md), [Desenvolvedor](../papeis/desenvolvedor.md), [Stakeholders](../papeis/stakeholders) e [Testador](testador.md)

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

Que informação é necessária para o usuário confiar numa decisão automática?

Quais informações são necessárias para que o usuário entenda os fatores mais relevantes envolvidos na decisão?


---
***5. Identificar as restrições no sistema (impactos para explicabilidade)***

**O que fazer**

Levantar restrições: regulatórias (LGPD, requisitos de auditoria), técnicas (modelo utilizados), qualidade (qualidade esperada para as explicações), econômicas (custo de geração de explicações), temporais (latência aceitável), compatibilidade (plataformas).

**Quem**

Engenheiro de Requisitos, Gerente de Projeto, Arquiteto e especialista em ética e regulação (se houver).

**Onde registrar**

[Documento de Visão da Explicabilidade](../tarefas/documento-requisito.md) → seção 4.1 Necessidades e Funcionalidade e 5. Outros Requisitos do Produto (Explicabilidade)

---
***6. Definir os limites da Explicabilidade***

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
