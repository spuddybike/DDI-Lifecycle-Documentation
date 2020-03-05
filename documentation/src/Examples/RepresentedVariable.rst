Represented Variable
====================
                    
.. code-block:: XML    
                    
  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    Example - Represented Variable and use by a Variable with restrictions 
  -->

    <l:LogicalProduct xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:LogProd:1</r:URN>
      <l:RepresentedVariableScheme scopeOfUniqueness="Agency" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:RepVarSheme:1</r:URN>
    
        <!-- Represented Variable Example 2 -->
    
        <l:RepresentedVariable isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:RV_1:1</r:URN>
          <l:RepresentedVariableName>
            <r:String xml:lang="en">Household Type</r:String>
          </l:RepresentedVariableName>
          <r:Label>
            <r:Content xml:lang="en">Household Type</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">Defines the type of household in terms of Non-Family and Family components</r:Content>
          </r:Description>
          <r:UnitTypeReference isReference="true" isExternal="false" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Households:1</r:URN>
            <r:TypeOfObject>Universe</r:TypeOfObject>
          </r:UnitTypeReference>
          <r:ConceptReference isReference="true" isExternal="false" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:HouseholdType:1</r:URN>
            <r:TypeOfObject>Concept</r:TypeOfObject>
          </r:ConceptReference>
          <r:CategorySchemeReference isReference="true" isExternal="false" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CatS_HouseholdType:1</r:URN>
            <r:TypeOfObject>CategoryScheme</r:TypeOfObject>
          </r:CategorySchemeReference>
        </l:RepresentedVariable>
    
        <!-- Represented Variable Example 2 -->
    
        <l:RepresentedVariable isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:RV_Age:1</r:URN>
          <l:RepresentedVariableName>
            <r:String xml:lang="en">Age of Person</r:String>
          </l:RepresentedVariableName>
          <r:Label>
            <r:Content xml:lang="en">Age of Person in Years</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">Age of Person expressed as a measure of the number of years of age</r:Content>
          </r:Description>
          <r:UnitTypeReference isReference="true" isExternal="true" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Persons:1.0</r:URN>
            <r:TypeOfObject>Universe</r:TypeOfObject>
          </r:UnitTypeReference>
          <r:ConceptReference isReference="true" isExternal="true" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Concept_Age:1.0</r:URN>
            <r:TypeOfObject>Concept</r:TypeOfObject>
          </r:ConceptReference>
          <r:NumericRepresentation interval="1" decimalPositions="0" classificationLevel="Interval">
            <r:NumericTypeCode>Integer</r:NumericTypeCode>
          </r:NumericRepresentation>
        </l:RepresentedVariable>
      </l:RepresentedVariableScheme>
    
      <l:VariableScheme scopeOfUniqueness="Agency" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:VarSheme:1</r:URN>
    
        <!-- The following Variable reference the RepresentedVariable that is its base and restricts the Universe to Persons in the United States -->
    
        <l:Variable isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Var_Age:1</r:URN>
          <l:VariableName>
            <r:String xml:lang="en">Age of Person</r:String>
          </l:VariableName>
          <r:Label>
            <r:Content xml:lang="en">Age of Person in Years</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">Age of Person in the United States expressed as a measure of the number of years of age 0 to 100 with topcode of 100 being "100 or over"</r:Content>
          </r:Description>
          <r:RepresentedVariableReference isReference="true" isExternal="true" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:RV_Age:1</r:URN>
            <r:TypeOfObject>RepresentedVariable</r:TypeOfObject>
          </r:RepresentedVariableReference>
          <r:UniverseReference isReference="true" isExternal="true" lateBound="false">
            <r:URN>urn:ddi:us.mpc:Univ_PersonsInUS:1.0</r:URN>
            <r:TypeOfObject>Universe</r:TypeOfObject>
          </r:UniverseReference>
          <r:ConceptReference isReference="true" isExternal="true" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Concept_Age:1.0</r:URN>
            <r:TypeOfObject>Concept</r:TypeOfObject>
          </r:ConceptReference>
          <l:VariableRepresentation>
            <r:NumericRepresentationReference isReference="true" isExternal="true" lateBound="false">
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Num_1_100_top:1.0</r:URN>
              <r:TypeOfObject>ManagedNumericRepresentation</r:TypeOfObject>
            </r:NumericRepresentationReference>
          </l:VariableRepresentation>
        </l:Variable>
    
        <!-- The following Variable reference the RepresentedVariable that is its base and restricts the Universe to teenagers (ages 13-19) -->
    
        <l:Variable isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Var_Age_13_19:1</r:URN>
          <l:VariableName>
            <r:String xml:lang="en">Age of Teenager</r:String>
          </l:VariableName>
          <r:Label>
            <r:Content xml:lang="en">Age of Person 13 to 19 years of age in Years</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">Age of a Teenage Person expressed as a measure of the number of years of age 13 to 19</r:Content>
          </r:Description>
          <r:RepresentedVariableReference isReference="true" isExternal="true" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:RV_Age:1</r:URN>
            <r:TypeOfObject>RepresentedVariable</r:TypeOfObject>
          </r:RepresentedVariableReference>
          <r:UniverseReference isReference="true" isExternal="true" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Univ_Persons_Age_13_19:1.0</r:URN>
            <r:TypeOfObject>Universe</r:TypeOfObject>
          </r:UniverseReference>
          <r:ConceptReference isReference="true" isExternal="true" lateBound="false">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:Concept_Age:1.0</r:URN>
            <r:TypeOfObject>Concept</r:TypeOfObject>
          </r:ConceptReference>
          <l:VariableRepresentation>
            <r:NumericRepresentation classificationLevel="Interval">
              <r:RecommendedDataType>Integer</r:RecommendedDataType>
              <r:MeasurementUnit>Years</r:MeasurementUnit>
              <r:NumberRange>
                <r:Low isInclusive="true">13</r:Low>
                <r:High isInclusive="true">19</r:High>
              </r:NumberRange>
            </r:NumericRepresentation>
          </l:VariableRepresentation>
        </l:Variable>
      </l:VariableScheme>
    </l:LogicalProduct>
