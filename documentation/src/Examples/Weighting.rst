Weighting
=========

.. code-block:: XML

  <?xml version="1.0" encoding="UTF-8"?>
  <!--

    Example - Weighting
    
  -->
    
    <g:ResourcePackage xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN>urn:ddi:us.mpc:RP_weight:1</r:URN>
      <d:DataCollection isMaintainable="true" scopeOfUniqueness="Agency">
        <r:URN>urn:ddi:us.mpc:DColl:1</r:URN>
        <d:Methodology isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:Meth_1:1</r:URN>
          <d:WeightingMethodology isIdentifiable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:WgtMeth_1:1</r:URN>
            <d:TypeOfWeightingMethodology>Standard Weight</d:TypeOfWeightingMethodology>
            <r:Description><r:Content>Sample is taken using a simple probability resulting in each case being of equal weight in the resulting data.</r:Content></r:Description>
          </d:WeightingMethodology>
          <d:WeightingMethodology isIdentifiable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:WgtMeth_2:1</r:URN>
            <d:TypeOfWeightingMethodology>Inverse Probability Weighting</d:TypeOfWeightingMethodology>
            <r:Description><r:Content>The estimation procedure involves weighting the data from each sample person by the inverse of the probability of the person being in the sample. This gives a rough measure of the number of actual persons that the sample person represents.</r:Content></r:Description>
          </d:WeightingMethodology>
        </d:Methodology>
        <d:ProcessingEventScheme isMaintainable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:ProcEventScheme:1</r:URN>
          <d:ProcessingEvent isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:ProcEvent_l:1</r:URN>
            <d:Weighting isVersionable="true" scopeOfUniqueness="Agency">
              <r:URN>urn:ddi:us.mpc:WgtEvent_l:1</r:URN>
            </d:Weighting>
            <d:DataAppraisalInformation>
              <d:ResponseRate>
                <d:SampleSize>45027</d:SampleSize>
                <d:NumberOfResponses>35793</d:NumberOfResponses>
                <d:SpecificResponseRate>79.3</d:SpecificResponseRate>
              </d:ResponseRate>
              <d:SamplingError><r:Content>2% margin of error</r:Content></d:SamplingError>
            </d:DataAppraisalInformation>
          </d:ProcessingEvent>
          <d:ProcessingEvent isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:ProcEvent_l:1</r:URN>
            <d:Weighting isVersionable="true" scopeOfUniqueness="Agency">
              <r:URN>urn:ddi:us.mpc:WgtEvent_2:1</r:URN>
              <d:WeightingMethodologyReference>
                <r:URN>urn:ddi:us.mpc:WgtMeth_1:1</r:URN>
                <r:TypeOfObject>WeightingMethodology</r:TypeOfObject>
              </d:WeightingMethodologyReference>
              <r:AnalysisUnit>Person</r:AnalysisUnit>
              <d:UsageGuide>
                <d:UsageExample><r:Content>Weight all variables x10</r:Content></d:UsageExample>
                <d:UsageRestrictions><r:Content>None</r:Content></d:UsageRestrictions>
                <d:UsageRecommendations><r:Content>All cases represent 10 units in the population.</r:Content></d:UsageRecommendations>
              </d:UsageGuide>
              <d:StandardWeight>
                <r:URN>urn:ddi:us.mpc:SW:1</r:URN>
                <d:StandardWeightValue>10</d:StandardWeightValue>
              </d:StandardWeight>
            </d:Weighting>
          </d:ProcessingEvent>
          <d:ProcessingEvent isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:ProcEvent_l:1</r:URN>
            <d:Weighting isVersionable="true" scopeOfUniqueness="Agency">
              <r:URN>urn:ddi:us.mpc:WgtEvent_3:1</r:URN>
              <d:WeightingMethodologyReference>
                <r:URN>urn:ddi:us.mpc:WgtMeth_2:1</r:URN>
                <r:TypeOfObject>WeightingMethodology</r:TypeOfObject>
              </d:WeightingMethodologyReference>
              <r:AnalysisUnit>Person</r:AnalysisUnit>
              <d:UsageGuide>
                <d:UsageExample><r:Content>Weight all variables by the case specific weight.</r:Content></d:UsageExample>
                <d:UsageRestrictions><r:Content>None</r:Content></d:UsageRestrictions>
                <d:UsageRecommendations><r:Content>All variables within a case should indicate the appropriate specific weight variable to use in analysing the data.</r:Content></d:UsageRecommendations>
              </d:UsageGuide>
              <d:StandardWeight>
                <r:URN>urn:ddi:us.mpc:SW:1</r:URN>
                <d:StandardWeightValue>10</d:StandardWeightValue>
              </d:StandardWeight>
            </d:Weighting>
          </d:ProcessingEvent>
        </d:ProcessingEventScheme>
      </d:DataCollection>
      <l:LogicalProduct isMaintainable="true" scopeOfUniqueness="Agency">
        <r:URN>urn:ddi:us.mpc:LogProd:1</r:URN>
        <l:VariableScheme>
          <r:URN>urn:ddi:us.mpc:VScheme:1</r:URN>
          <l:Variable>
            <r:URN>urn:ddi:us.mpc:Var_CaseID:1</r:URN>
            <r:Label><r:Content>Case ID</r:Content></r:Label>
          </l:Variable>
          <l:Variable isWeight="true">
            <r:URN>urn:ddi:us.mpc:Var_PWGT:1</r:URN>
            <r:Label><r:Content>Person Weight</r:Content></r:Label>
          </l:Variable>
          <l:Variable>
            <r:URN>urn:ddi:us.mpc:Var_1:1</r:URN>
            <l:WeightingProcessReference>
              <r:URN>urn:ddi:us.mpc:WgtEvent_3:1</r:URN>
              <r:TypeOfObject>Weighting</r:TypeOfObject>
            </l:WeightingProcessReference>
            <l:VariableRepresentation>
              <r:WeightVariableReference>
                <r:URN>urn:ddi:us.mpc:Var_PWGT:1</r:URN>
                <r:TypeOfObject>Variable</r:TypeOfObject>
              </r:WeightVariableReference>
            </l:VariableRepresentation>
          </l:Variable>
          <l:Variable>
            <r:URN>urn:ddi:us.mpc:Var_1:1</r:URN>
            <l:WeightingProcessReference>
              <r:URN>urn:ddi:us.mpc:WgtEvent_2:1</r:URN>
              <r:TypeOfObject>Weighting</r:TypeOfObject>
            </l:WeightingProcessReference>
            <l:VariableRepresentation>
              <l:StandardWeightReference>
                <r:URN>urn:ddi:us.mpc:SW:1</r:URN>
                <r:TypeOfObject>StandardWeight</r:TypeOfObject>
              </l:StandardWeightReference>
            </l:VariableRepresentation>
          </l:Variable>
        </l:VariableScheme>
      </l:LogicalProduct>
    </g:ResourcePackage>
