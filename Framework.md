<?xml version="1.0" encoding="UTF-8"?>
<!-- BPMN 2.0 XML -->
<definitions xmlns="http://www.omg.org/spec/BPMN/20100524/MODEL"
             xmlns:bpmndi="http://www.omg.org/spec/BPMN/20100524/DI"
             xmlns:omgdc="http://www.omg.org/spec/DD/20100524/DC"
             xmlns:omgdi="http://www.omg.org/spec/DD/20100524/DI"
             id="Definitions_Explicabilidade"
             targetNamespace="http://example.com/bpmn">
  <process id="Processo_Explicabilidade" isExecutable="true">
    <!-- Start -->
    <startEvent id="StartEvent_1" name="Iniciar Processo"/>

    <!-- Lane set: Pool com duas lanes -->
    <laneSet id="LaneSet_1">
      <lane id="Lane_Visao" name="Visão da Explicabilidade">
        <!-- flowNodeRefs preenchidos abaixo -->
      </lane>
      <lane id="Lane_Consolidacao" name="Consolidação DER">
        <!-- flowNodeRefs preenchidos abaixo -->
      </lane>
    </laneSet>

    <!-- Atividades da Lane 1 -->
    <task id="Task_DefinirExplicabilidade" name="Definir Explicabilidade"/>
    <exclusiveGateway id="Gateway_Capturar_1" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_1" name="Capturar Termos para Glossário 1"/>
    <exclusiveGateway id="Gateway_Merge_1"/>

    <task id="Task_IdentificarStakeholders" name="Identificar Stakeholders"/>
    <exclusiveGateway id="Gateway_Capturar_2" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_2" name="Capturar Termos para Glossário 2"/>
    <exclusiveGateway id="Gateway_Merge_2"/>

    <task id="Task_ObterSolicitacoes" name="Obter Solicitações"/>
    <exclusiveGateway id="Gateway_Capturar_3" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_3" name="Capturar Termos para Glossário 3"/>
    <exclusiveGateway id="Gateway_Merge_3"/>

    <task id="Task_IdentificarRestricoes" name="Identificar Restrições"/>
    <exclusiveGateway id="Gateway_Capturar_4" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_4" name="Capturar Termos para Glossário 4"/>
    <exclusiveGateway id="Gateway_Merge_4"/>

    <task id="Task_DefinirLimites" name="Definir Limites"/>
    <exclusiveGateway id="Gateway_Capturar_5" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_5" name="Capturar Termos para Glossário 5"/>
    <exclusiveGateway id="Gateway_Merge_5"/>

    <!-- Paralelo para gerar artefatos -->
    <parallelGateway id="Gateway_Parallel_Split" name="Gerar artefatos em paralelo"/>
    <task id="Task_GerarDocumentoVisao" name="Gerar Documento de Visão de Explicabilidade"/>
    <task id="Task_ConsolidarGlossario" name="Consolidar Glossário"/>
    <parallelGateway id="Gateway_Parallel_Join"/>

    <!-- Lane 2: Consolidação do DER -->
    <task id="Task_GerarDER" name="Gerar Documento de Requisitos de Explicabilidade"/>
    <endEvent id="EndEvent_1" name="Fim"/>

    <!-- Fluxos de sequência -->
    <sequenceFlow id="flow_1" sourceRef="StartEvent_1" targetRef="Task_DefinirExplicabilidade"/>
    <sequenceFlow id="flow_2" sourceRef="Task_DefinirExplicabilidade" targetRef="Gateway_Capturar_1"/>
    <sequenceFlow id="flow_3" sourceRef="Gateway_Capturar_1" targetRef="Task_Capturar_1" name="sim"/>
    <sequenceFlow id="flow_4" sourceRef="Gateway_Capturar_1" targetRef="Gateway_Merge_1" name="não"/>
    <sequenceFlow id="flow_5" sourceRef="Task_Capturar_1" targetRef="Gateway_Merge_1"/>
    <sequenceFlow id="flow_6" sourceRef="Gateway_Merge_1" targetRef="Task_IdentificarStakeholders"/>

    <sequenceFlow id="flow_7" sourceRef="Task_IdentificarStakeholders" targetRef="Gateway_Capturar_2"/>
    <sequenceFlow id="flow_8" sourceRef="Gateway_Capturar_2" targetRef="Task_Capturar_2" name="sim"/>
    <sequenceFlow id="flow_9" sourceRef="Gateway_Capturar_2" targetRef="Gateway_Merge_2" name="não"/>
    <sequenceFlow id="flow_10" sourceRef="Task_Capturar_2" targetRef="Gateway_Merge_2"/>
    <sequenceFlow id="flow_11" sourceRef="Gateway_Merge_2" targetRef="Task_ObterSolicitacoes"/>

    <sequenceFlow id="flow_12" sourceRef="Task_ObterSolicitacoes" targetRef="Gateway_Capturar_3"/>
    <sequenceFlow id="flow_13" sourceRef="Gateway_Capturar_3" targetRef="Task_Capturar_3" name="sim"/>
    <sequenceFlow id="flow_14" sourceRef="Gateway_Capturar_3" targetRef="Gateway_Merge_3" name="não"/>
    <sequenceFlow id="flow_15" sourceRef="Task_Capturar_3" targetRef="Gateway_Merge_3"/>
    <sequenceFlow id="flow_16" sourceRef="Gateway_Merge_3" targetRef="Task_IdentificarRestricoes"/>

    <sequenceFlow id="flow_17" sourceRef="Task_IdentificarRestricoes" targetRef="Gateway_Capturar_4"/>
    <sequenceFlow id="flow_18" sourceRef="Gateway_Capturar_4" targetRef="Task_Capturar_4" name="sim"/>
    <sequenceFlow id="flow_19" sourceRef="Gateway_Capturar_4" targetRef="Gateway_Merge_4" name="não"/>
    <sequenceFlow id="flow_20" sourceRef="Task_Capturar_4" targetRef="Gateway_Merge_4"/>
    <sequenceFlow id="flow_21" sourceRef="Gateway_Merge_4" targetRef="Task_DefinirLimites"/>

    <sequenceFlow id="flow_22" sourceRef="Task_DefinirLimites" targetRef="Gateway_Capturar_5"/>
    <sequenceFlow id="flow_23" sourceRef="Gateway_Capturar_5" targetRef="Task_Capturar_5" name="sim"/>
    <sequenceFlow id="flow_24" sourceRef="Gateway_Capturar_5" targetRef="Gateway_Merge_5" name="não"/>
    <sequenceFlow id="flow_25" sourceRef="Task_Capturar_5" targetRef="Gateway_Merge_5"/>
    <sequenceFlow id="flow_26" sourceRef="Gateway_Merge_5" targetRef="Gateway_Parallel_Split"/>

    <sequenceFlow id="flow_27" sourceRef="Gateway_Parallel_Split" targetRef="Task_GerarDocumentoVisao"/>
    <sequenceFlow id="flow_28" sourceRef="Gateway_Parallel_Split" targetRef="Task_ConsolidarGlossario"/>
    <sequenceFlow id="flow_29" sourceRef="Task_GerarDocumentoVisao" targetRef="Gateway_Parallel_Join"/>
    <sequenceFlow id="flow_30" sourceRef="Task_ConsolidarGlossario" targetRef="Gateway_Parallel_Join"/>

    <sequenceFlow id="flow_31" sourceRef="Gateway_Parallel_Join" targetRef="Task_GerarDER"/>
    <sequenceFlow id="flow_32" sourceRef="Task_GerarDER" targetRef="EndEvent_1"/>

  </process>

  <!-- Participant / Pool -->
  <participant id="Participant_Analista" name="Analista de Requisitos" processRef="Processo_Explicabilidade"/>

  <!-- Mapar flow nodes para lanes -->
  <process id="LaneMappingHelper" isExecutable="false">
    <!-- apenas referências de nodes para lanes (não executável) -->
  </process>
  <bpmndi:BPMNDiagram id="BPMNDiagram_1">
    <bpmndi:BPMNPlane id="BPMNPlane_1" bpmnElement="Processo_Explicabilidade"/>
    <!-- Diagrama simplificado (posicionamento omitido para brevidade) -->
  </bpmndi:BPMNDiagram>
</definitions>
```<?xml version="1.0" encoding="UTF-8"?>
<!-- BPMN 2.0 XML -->
<definitions xmlns="http://www.omg.org/spec/BPMN/20100524/MODEL"
             xmlns:bpmndi="http://www.omg.org/spec/BPMN/20100524/DI"
             xmlns:omgdc="http://www.omg.org/spec/DD/20100524/DC"
             xmlns:omgdi="http://www.omg.org/spec/DD/20100524/DI"
             id="Definitions_Explicabilidade"
             targetNamespace="http://example.com/bpmn">
  <process id="Processo_Explicabilidade" isExecutable="true">
    <!-- Start -->
    <startEvent id="StartEvent_1" name="Iniciar Processo"/>

    <!-- Lane set: Pool com duas lanes -->
    <laneSet id="LaneSet_1">
      <lane id="Lane_Visao" name="Visão da Explicabilidade">
        <!-- flowNodeRefs preenchidos abaixo -->
      </lane>
      <lane id="Lane_Consolidacao" name="Consolidação DER">
        <!-- flowNodeRefs preenchidos abaixo -->
      </lane>
    </laneSet>

    <!-- Atividades da Lane 1 -->
    <task id="Task_DefinirExplicabilidade" name="Definir Explicabilidade"/>
    <exclusiveGateway id="Gateway_Capturar_1" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_1" name="Capturar Termos para Glossário 1"/>
    <exclusiveGateway id="Gateway_Merge_1"/>

    <task id="Task_IdentificarStakeholders" name="Identificar Stakeholders"/>
    <exclusiveGateway id="Gateway_Capturar_2" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_2" name="Capturar Termos para Glossário 2"/>
    <exclusiveGateway id="Gateway_Merge_2"/>

    <task id="Task_ObterSolicitacoes" name="Obter Solicitações"/>
    <exclusiveGateway id="Gateway_Capturar_3" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_3" name="Capturar Termos para Glossário 3"/>
    <exclusiveGateway id="Gateway_Merge_3"/>

    <task id="Task_IdentificarRestricoes" name="Identificar Restrições"/>
    <exclusiveGateway id="Gateway_Capturar_4" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_4" name="Capturar Termos para Glossário 4"/>
    <exclusiveGateway id="Gateway_Merge_4"/>

    <task id="Task_DefinirLimites" name="Definir Limites"/>
    <exclusiveGateway id="Gateway_Capturar_5" name="Decidir capturar termos?"/>
    <task id="Task_Capturar_5" name="Capturar Termos para Glossário 5"/>
    <exclusiveGateway id="Gateway_Merge_5"/>

    <!-- Paralelo para gerar artefatos -->
    <parallelGateway id="Gateway_Parallel_Split" name="Gerar artefatos em paralelo"/>
    <task id="Task_GerarDocumentoVisao" name="Gerar Documento de Visão de Explicabilidade"/>
    <task id="Task_ConsolidarGlossario" name="Consolidar Glossário"/>
    <parallelGateway id="Gateway_Parallel_Join"/>

    <!-- Lane 2: Consolidação do DER -->
    <task id="Task_GerarDER" name="Gerar Documento de Requisitos de Explicabilidade"/>
    <endEvent id="EndEvent_1" name="Fim"/>

    <!-- Fluxos de sequência -->
    <sequenceFlow id="flow_1" sourceRef="StartEvent_1" targetRef="Task_DefinirExplicabilidade"/>
    <sequenceFlow id="flow_2" sourceRef="Task_DefinirExplicabilidade" targetRef="Gateway_Capturar_1"/>
    <sequenceFlow id="flow_3" sourceRef="Gateway_Capturar_1" targetRef="Task_Capturar_1" name="sim"/>
    <sequenceFlow id="flow_4" sourceRef="Gateway_Capturar_1" targetRef="Gateway_Merge_1" name="não"/>
    <sequenceFlow id="flow_5" sourceRef="Task_Capturar_1" targetRef="Gateway_Merge_1"/>
    <sequenceFlow id="flow_6" sourceRef="Gateway_Merge_1" targetRef="Task_IdentificarStakeholders"/>

    <sequenceFlow id="flow_7" sourceRef="Task_IdentificarStakeholders" targetRef="Gateway_Capturar_2"/>
    <sequenceFlow id="flow_8" sourceRef="Gateway_Capturar_2" targetRef="Task_Capturar_2" name="sim"/>
    <sequenceFlow id="flow_9" sourceRef="Gateway_Capturar_2" targetRef="Gateway_Merge_2" name="não"/>
    <sequenceFlow id="flow_10" sourceRef="Task_Capturar_2" targetRef="Gateway_Merge_2"/>
    <sequenceFlow id="flow_11" sourceRef="Gateway_Merge_2" targetRef="Task_ObterSolicitacoes"/>

    <sequenceFlow id="flow_12" sourceRef="Task_ObterSolicitacoes" targetRef="Gateway_Capturar_3"/>
    <sequenceFlow id="flow_13" sourceRef="Gateway_Capturar_3" targetRef="Task_Capturar_3" name="sim"/>
    <sequenceFlow id="flow_14" sourceRef="Gateway_Capturar_3" targetRef="Gateway_Merge_3" name="não"/>
    <sequenceFlow id="flow_15" sourceRef="Task_Capturar_3" targetRef="Gateway_Merge_3"/>
    <sequenceFlow id="flow_16" sourceRef="Gateway_Merge_3" targetRef="Task_IdentificarRestricoes"/>

    <sequenceFlow id="flow_17" sourceRef="Task_IdentificarRestricoes" targetRef="Gateway_Capturar_4"/>
    <sequenceFlow id="flow_18" sourceRef="Gateway_Capturar_4" targetRef="Task_Capturar_4" name="sim"/>
    <sequenceFlow id="flow_19" sourceRef="Gateway_Capturar_4" targetRef="Gateway_Merge_4" name="não"/>
    <sequenceFlow id="flow_20" sourceRef="Task_Capturar_4" targetRef="Gateway_Merge_4"/>
    <sequenceFlow id="flow_21" sourceRef="Gateway_Merge_4" targetRef="Task_DefinirLimites"/>

    <sequenceFlow id="flow_22" sourceRef="Task_DefinirLimites" targetRef="Gateway_Capturar_5"/>
    <sequenceFlow id="flow_23" sourceRef="Gateway_Capturar_5" targetRef="Task_Capturar_5" name="sim"/>
    <sequenceFlow id="flow_24" sourceRef="Gateway_Capturar_5" targetRef="Gateway_Merge_5" name="não"/>
    <sequenceFlow id="flow_25" sourceRef="Task_Capturar_5" targetRef="Gateway_Merge_5"/>
    <sequenceFlow id="flow_26" sourceRef="Gateway_Merge_5" targetRef="Gateway_Parallel_Split"/>

    <sequenceFlow id="flow_27" sourceRef="Gateway_Parallel_Split" targetRef="Task_GerarDocumentoVisao"/>
    <sequenceFlow id="flow_28" sourceRef="Gateway_Parallel_Split" targetRef="Task_ConsolidarGlossario"/>
    <sequenceFlow id="flow_29" sourceRef="Task_GerarDocumentoVisao" targetRef="Gateway_Parallel_Join"/>
    <sequenceFlow id="flow_30" sourceRef="Task_ConsolidarGlossario" targetRef="Gateway_Parallel_Join"/>

    <sequenceFlow id="flow_31" sourceRef="Gateway_Parallel_Join" targetRef="Task_GerarDER"/>
    <sequenceFlow id="flow_32" sourceRef="Task_GerarDER" targetRef="EndEvent_1"/>

  </process>

  <!-- Participant / Pool -->
  <participant id="Participant_Analista" name="Analista de Requisitos" processRef="Processo_Explicabilidade"/>

  <!-- Mapar flow nodes para lanes -->
  <process id="LaneMappingHelper" isExecutable="false">
    <!-- apenas referências de nodes para lanes (não executável) -->
  </process>
  <bpmndi:BPMNDiagram id="BPMNDiagram_1">
    <bpmndi:BPMNPlane id="BPMNPlane_1" bpmnElement="Processo_Explicabilidade"/>
    <!-- Diagrama simplificado (posicionamento omitido para brevidade) -->
  </bpmndi:BPMNDiagram>
</definitions>
