In / Out Parameter, Binding
============================
    
.. code-block:: XML    
    
  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    
  Example - In/Out Parameters and Bindings
  This is a very detailed example walking through all the control constructs, questions, dynamic text, and control constructs. 
  In general usage bindings out parameters and bindings would be noted at the highest discrete levell such as the Question Construct for the data captured by a Question Item. 
  Identification and binding at this level keeps the question reusable across various uses in a questionnaire.
    
  -->
    <g:ResourcePackage xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3"
                       xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/"
                       xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN>urn:ddi:us.mpc:ParamerterBindingRP:1</r:URN>
      <d:ControlConstructScheme scopeOfUniqueness="Agency" isMaintainable="true">
        <r:URN>urn:ddi:us.mpc:CCScheme:1</r:URN>
        <d:Sequence isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:SEQ:1</r:URN>
          <r:Binding>
            <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:QC_OUT_1:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:SourceParameterReference>
            <r:TargetParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:QC_IN_2:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:TargetParameterReference>
          </r:Binding>
          <d:ControlConstructReference isReference="true">
            <r:URN>urn:ddi:us.mpc:QC_1:1</r:URN>
            <r:TypeOfObject>QuestionConstruct</r:TypeOfObject>
          </d:ControlConstructReference>
          <d:ControlConstructReference isReference="true">
            <r:URN>urn:ddi:us.mpc:QC_2:1</r:URN>
            <r:TypeOfObject>QuestionConstruct</r:TypeOfObject>
          </d:ControlConstructReference>
        </d:Sequence>
        <d:QuestionConstruct isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:QC_1:1</r:URN>
          <r:OutParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
            <r:URN>urn:ddi:us.mpc:QC_OUT_1:1</r:URN>
          </r:OutParameter>
          <r:Binding>
            <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:Q1_Name:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:SourceParameterReference>
            <r:TargetParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:QC_OUT_1:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:TargetParameterReference>
          </r:Binding>
          <r:QuestionReference isReference="true" isExternal="false" lateBound="false">
            <r:URN>urn:ddi:us.mpc:Q1:1</r:URN>
            <r:TypeOfObject>QuestionItem</r:TypeOfObject>
          </r:QuestionReference>
        </d:QuestionConstruct>
        <d:QuestionConstruct isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:QC_2:1</r:URN>
          <r:InParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
            <r:URN>urn:ddi:us.mpc:QC_IN_2:1</r:URN>
          </r:InParameter>
          <r:OutParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
            <r:URN>urn:ddi:us.mpc:QC_OUT_2:1</r:URN>
          </r:OutParameter>
          <r:Binding>
            <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:QC_IN_2:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:SourceParameterReference>
            <r:TargetParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:Q2_Name:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:TargetParameterReference>
          </r:Binding>
          <r:Binding>
            <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:Q2_Age:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:SourceParameterReference>
            <r:TargetParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:QC_OUT_2:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:TargetParameterReference>
          </r:Binding>
          <r:QuestionReference isReference="true" isExternal="false" lateBound="false">
            <r:URN>urn:ddi:us.mpc:Q2:1</r:URN>
            <r:TypeOfObject>QuestionItem</r:TypeOfObject>
          </r:QuestionReference>
        </d:QuestionConstruct>
      </d:ControlConstructScheme>
      <d:QuestionScheme scopeOfUniqueness="Agency" isMaintainable="true">
        <r:URN>urn:ddi:us.mpc:QScheme:1</r:URN>
        <d:QuestionItem isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:Q1:1</r:URN>
          <r:OutParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
            <r:URN>urn:ddi:us.mpc:Q1_Name:1</r:URN>
          </r:OutParameter>
          <r:Binding>
            <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:RD_Name:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:SourceParameterReference>
            <r:TargetParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:Q1_Name:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:TargetParameterReference>
          </r:Binding>
          <d:QuestionText>
            <d:LiteralText>
              <d:Text xml:lang="en" xml:space="default">What is the name of your oldest child?</d:Text>
            </d:LiteralText>
          </d:QuestionText>
          <d:TextDomainReference isReference="true" isExternal="false" lateBound="false">
            <r:URN>urn:ddi:us.mpc:TD_1:1</r:URN>
            <r:TypeOfObject>ManagedTextRepresentation</r:TypeOfObject>
            <r:OutParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
              <r:URN>urn:ddi:us.mpc:RD_Name:1</r:URN>
            </r:OutParameter>
          </d:TextDomainReference>
        </d:QuestionItem>
        <d:QuestionItem isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:Q2:1</r:URN>
          <r:InParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
            <r:URN>urn:ddi:us.mpc:Q2_Name:1</r:URN>
          </r:InParameter>
          <r:OutParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
            <r:URN>urn:ddi:us.mpc:Q2_Age:1</r:URN>
          </r:OutParameter>
          <r:Binding>
            <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:RD_Age:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:SourceParameterReference>
            <r:TargetParameterReference isReference="true" isExternal="false" lateBound="false">
              <r:URN>urn:ddi:us.mpc:Q2_Age:1</r:URN>
              <r:TypeOfObject>OutParameter</r:TypeOfObject>
            </r:TargetParameterReference>
          </r:Binding>
          <d:QuestionText>
            <d:LiteralText>
              <d:Text xml:lang="en" xml:space="preserve">How old is </d:Text>
            </d:LiteralText>
            <d:ConditionalText>
              <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
                <r:URN>urn:ddi:us.mpc:Q2_Name:1</r:URN>
                <r:TypeOfObject>InParameter</r:TypeOfObject>
              </r:SourceParameterReference>
            </d:ConditionalText>
            <d:LiteralText>
              <d:Text xml:lang="en" xml:space="preserve"> ?</d:Text>
            </d:LiteralText>
          </d:QuestionText>
          <d:NumericDomainReference>
            <r:URN>urn:ddi:us.mpc:ND_1:1</r:URN>
            <r:TypeOfObject>ManagedNumericRepresentation</r:TypeOfObject>
            <r:OutParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
              <r:URN>urn:ddi:us.mpc:RD_Age:1</r:URN>
            </r:OutParameter>
          </d:NumericDomainReference>
        </d:QuestionItem>
      </d:QuestionScheme>
      <l:VariableScheme scopeOfUniqueness="Agency" isMaintainable="true">
        <r:URN>urn:ddi:us.mpc:VarScheme:1</r:URN>
        <l:Variable isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:V1:1</r:URN>
          <l:VariableName>
            <r:String xml:lang="en">Age 5 year cohorts</r:String>
          </l:VariableName>
          <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
            <r:URN>urn:ddi:us.mpc:GI_Age_Cohort:1</r:URN>
            <r:TypeOfObject>OutParameter</r:TypeOfObject>
          </r:SourceParameterReference>
        </l:Variable>
      </l:VariableScheme>
      <d:ProcessingInstructionScheme scopeOfUniqueness="Agency" isMaintainable="true">
        <r:URN>urn:ddi:us.mpc:ProcInstScheme:1</r:URN>
        <d:GenerationInstruction isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:GI:1</r:URN>
          <r:CommandCode>
            <r:Command>
              <r:ProgramLanguage>SPSS</r:ProgramLanguage>
              <r:InParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
                <r:URN>urn:ddi:us.mpc:GI_Age:1</r:URN>
                <r:Alias>AGE</r:Alias>
              </r:InParameter>
              <r:OutParameter isIdentifiable="true" scopeOfUniqueness="Agency" isArray="false">
                <r:URN>urn:ddi:us.mpc:GI_Age_Cohort:1</r:URN>
                <r:Alias>AGE_5</r:Alias>
              </r:OutParameter>
              <r:Binding>
                <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:QC_OUT_2:1</r:URN>
                  <r:TypeOfObject>OutParameter</r:TypeOfObject>
                </r:SourceParameterReference>
                <r:TargetParameterReference isReference="true" isExternal="false" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:GI_Age:1</r:URN>
                  <r:TypeOfObject>InParameter</r:TypeOfObject>
                </r:TargetParameterReference>
              </r:Binding>
              <r:CommandContent>If (AGE &amp;lt; 5) AGE_5=1; If (AGE &amp;gt;=5) &amp; (AGE &amp;lt; 10) AGE_5=2; If (AGE &amp;gt;=10 &amp; (AGE &amp;lt; 15) AGE_5=3; If (AGE &amp;gt;=15 &amp; (AGE &amp;lt; 20) AGE_5=4; If (AGE &amp;gt;=20 AGE_5=5</r:CommandContent>
            </r:Command>
          </r:CommandCode>
        </d:GenerationInstruction>
      </d:ProcessingInstructionScheme>
    </g:ResourcePackage>
