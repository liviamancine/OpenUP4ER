# Tarefa: Definir a Visão (Passos)

**Descrição:**  
Definir a visão da explicabilidade para o sistema, identificando o problema relacionado à ausência ou insuficiência de explicações e descrevendo os aspectos de confiança e transparência e compreensão esperados, com base nas necessidades e solicitações dos Stakeholders que dependem da compreensão das decisões do modelo.

**Objetivo**
A solução é proposta para abordar o problema de falta de confiança, transparência e compreensibilidade nas decisões produzidas pelo sistema de AM. Os Stakeholders colaboram com a equipe de desenvolvimento para expressar e documentar suas necessidades de explicação, seus critérios de confiança e os tipos de informações que precisam compreender. Esse alinhamento permite que a equipe do projeto obtenha uma visão clara sobre como a explicabilidade deve ser integrada ao sistema e quais mecanismos devem ser implementados para atendê-los.

## Relacionamentos

**Papéis**  
- **Responsável:** [Engenheiro de Requisitos](../papeis/engenheiro-requisitos.md)  
- **Executores Adicionais:** [Arquiteto de Software](../papeis/arquiteto-software.md), [Gerente de Projetos](../papeis/gerente-projeto.md), 
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
1. Identificar os Stakeholders (foco: explicabilidade)

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

2. Adquirir consenso sobre o problema (não pule para soluções)

**O que fazer**
- Conduzir workshops, entrevistas para definir qual é o problema de explicabilidade (p. ex. “não entendemos porque o modelo me fornece um resultado positivo”).
- Trabalhar o “problema por trás do problema” — identificar consequências (confiança, retrabalho, não conformidade).

**Quem**
- Engenheiro de Requisitos (facilitador), Stakeholders.

**Onde registrar**
- [Documento de Visão da Explicabilidade](../tarefas/definir.visao.md) → seção 4.1 Necessidades e Funcionalidades 
- [Itens gerados para Lista de Itens de Trabalho](Verificar)

**Técnicas**
-  [Guidaline: Técnica para obtenção de requisitos de explicabilidade](VERIFICAR)

##3. Capturar um vocabulário comum (glossário)

**O que fazer**
- Construir um glossário com termos centrais: explicabilidade, interpretabilidade, local/global, saliência, confiança, rastreabilidade, etc.
- Validar termos com stakeholders para evitar ambiguidade.

**Quem**
Engenheiro de Requisitos

**Onde registrar**
glossario-explicabilidade.md (artefato) e seção do DRE.

**Boas práticas**
Se você puder se encontrar pessoalmente com os Stakeholders, então você poderá conduzir uma entrevista ou uma sessão de brainstorming. Esta colaboração face-a-face é extremamente valiosa e reduz as possibilidades da equipe de projeto não entender as necessidades dos Stakeholders. Alguns requisitos podem já ter sido documentados em uma [Lista de Itens de Trabalho existente](verificar). Isto pode normalmente ser usado como um sólido ponto de partida do qual um conjunto completo de requisitos de explicabilidade possa ser criado.

Qualquer requisito obtido durante esta etapa deve ser capturado na [Lista de Itens de Trabalho existente](verificar). Para mais informações, veja Task: {Encontrar e Descrever os Requisitos](VERIFICAR).
---

## Ilustrações / Templates
- [Nome do Template](../templates/template-nome.md)
- [Exemplo de Preenchimento](../examples/exemplo-nome.md)

---

## Adaptação

**Impacto de não ter:**  
[Ex: “A ausência deste artefato aumenta o risco de desalinhamento entre stakeholders e equipe de desenvolvimento.”]

**Opções de Representação:**  
[Ex: “Customize este artefato conforme o contexto do projeto. Recomenda-se mantê-lo resumido e fácil de ler.”]

---

## Informações Adicionais

**Listas de Verificação:**  
- [Qualidades de Bons Requisitos](../checklists/qualidades-bons-requisitos.md)

**Referências:**  
- [Link para o OpenUP Original](file:///C:/Users/Livia%20Mancine/Downloads/OpenUP/Publish/openup/tasks/define_vision_9D36CF2F.html)

