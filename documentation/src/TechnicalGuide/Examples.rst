Examples
========


Dates
------

.. code-block:: XML

  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    Example - Dates: Simple, complete date range, range with unknown start, range with unknown end
  -->

  <r:TemporalCoverage xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3"     
    xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" 
    xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" 
    xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" 
    xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
	<r:URN>urn:ddi:us.mpc:TempCov:1</r:URN>
	
  <!-- SimpleDate -->

	<r:ReferenceDate>
		<r:SimpleDate>2013-02-26</r:SimpleDate>
		<r:HistoricalDate>
			<r:NonISODate>26 February 2013</r:NonISODate>
			<r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
			<r:Calendar>Gregorian</r:Calendar>
		</r:HistoricalDate>
	</r:ReferenceDate>

  <!-- Complete Date Range -->

	<r:ReferenceDate>
		<r:StartDate>2010-06-05T20:20:00</r:StartDate>
		<r:HistoricalStartDate>
			<r:NonISODate>24 Sivan 2770</r:NonISODate>
			<r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
			<r:Calendar>Jewish</r:Calendar>
		</r:HistoricalStartDate>
		<r:EndDate>2010-08-05T20:20:00</r:EndDate>
		<r:HistoricalEndDate>
			<r:NonISODate>28 Sivan 5770</r:NonISODate>
			<r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
			<r:Calendar>Jewish</r:Calendar>
		</r:HistoricalEndDate>
	</r:ReferenceDate>

  <!-- Range with unknown start date -->

	<r:ReferenceDate>
		<r:EndDate>2013-02-26</r:EndDate>
		<r:HistoricalEndDate>
			<r:NonISODate>February 26, 2013</r:NonISODate>
			<r:HistoricalDateFormat>Month dd, yyyy</r:HistoricalDateFormat>
			<r:Calendar>Gregorian</r:Calendar>
		</r:HistoricalEndDate>
	</r:ReferenceDate>

  <!-- Range with unknown end date -->

	<r:ReferenceDate>
		<r:StartDate>2013-02-26</r:StartDate>
		<r:HistoricalStartDate>
			<r:NonISODate>26 February 2013</r:NonISODate>
			<r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
			<r:Calendar>Gregorian</r:Calendar>
		</r:HistoricalStartDate>
	</r:ReferenceDate>
	
  </r:TemporalCoverage>


Identifiable
--------------

::

  <l:Code isIdentifiable="true" scopeOfUniqueness="Maintainable">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:CL\_1.Code\_1:1
    </r:URN>
    <r:Agency>us.mpc</r:Agency>
    <r:ID>Code\_1</r:ID>
    <r:Version>1</r:Version>
    <r:UserID typeOfUserID="NHGIS">Gender\_1</r:UserID>
    <r:MaintainableObject>
      <r:TypeOfObject>CodeList</r:TypeOfObject>
      <r:MaintainableID>CL\_1</r:MaintainableID>
      <r:MaintainableVersion>1</r:MaintainableVersion>
    </r:MaintainableObject>
    ...
  </l:Code>

Minimum required content of the above::

  <l:Code isIdentifiable="true" scopeOfUniqueness="Maintainable">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:CL\_1.Code\_1:1
    </r:URN>
    ...
  </l:Code>

Versionable
------------

::

  <l:Variable isVersionable="true" scopeOfUniqueness="Agency" versionDate="2012-10-31">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:Var\_1234:2
    </r:URN>
    <r:Agency>us.mpc</r:Agency>
    <r:ID>Var\_1234</r:ID>
    <r:Version>2</r:Version>
    <r:UserID typeOfUserID="IPUMS">MOMLOC</r:UserID>
    <r:VersionResponsibility>John Doe</r:VersionResponsibility>
    <r:VersionRationale>
      <r:RationaleDescription><r:String xml:lang="en">Expanded description to more clearly define the process of determining the MOCLOC value in households with multiple mothers.</r:String></r:RationaleDescription>
      <r:RationaleCode>Update</r:RationaleCode>
    </r:VersionRationale>
    <r:MaintainableObject>
      <r:TypeOfObject>VariableScheme</r:TypeOfObject>
      <r:MaintainableID>VS\_IPUMS</r:MaintainableID>
      <r:MaintainableVersion>6</r:MaintainableVersion>
    </r:MaintainableObject>
    ...
  </l:Variable>

Minimum required content of the above::

  <l:Variable isVersionable="true" scopeOfUniqueness="Agency" versionDate="2012-10-31">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:Var\_1234:2
    </r:URN>
    ...
  </l:Variable>

Maintainable
-------------

 ::

  <l:VariableScheme isVersionable="true" scopeOfUniqueness="Agency" versionDate="2012-10-31" isPublished="true" xml:lang="en">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:VS\_IPUMS:6
    </r:URN>
    <r:Agency>us.mpc</r:Agency>
    <r:ID>VS\_IPUMS</r:ID>
    <r:Version>6</r:Version>
    <r:UserID typeOfUserID="IPUMS">IPUMS\_VARS</r:UserID>
    <r:VersionResponsibility>John Doe</r:VersionResponsibility>
    <r:VersionRationale>
    <r:RationaleDescription>
      <r:String xml:lang="en">Versioned MOMLOC</r:String>
    </r:RationaleDescription>
    <r:RationaleCode>Update</r:RationaleCode>
    </r:VersionRationale>
    <r:Software></r:Software>
    <r:MetadataQuality>
      <r:QualityMeature>InternalReview</r:QualityMeasure>
      <r:MeasurePurpose><r:Content xml:lang="en">Content has be reviewed and confirmed for use on Public site.</r:Content></r:MeasurePurpose>
      <r:MeasureValue>Public</r:MeasureValue>
    </r:MetadataQuality>
    ...
  </l:VariableScheme>

Minimum required content of the above::

  <l:VariableScheme isVersionable="true" scopeOfUniqueness="Agency" versionDate="2012-10-31" isPublished="true" xml:lang="en">
    <r:URN typeOfIdentifier="Canonical">
    urn:ddi:us.mpc:VS\_IPUMS:6
    </r:URN>
    ...
  </l:VariableScheme>

Note that by including the information for the MaintainableObject in an Identifiable or Versionable the user has provided sufficient information to build either a Canonical or Deprecated URN scoped to either the agency or the maintainable. While the information may not be part of the URN as expressed by the maintaining agency, the information contained in the MaintainableObject provides contextual information that may be important to the user and may need to be passed to them for purposes other than strict identification. The inclusion of Versioning information in Versionable and Maintainable may be used internally to track quality control and processing activities and may also be valuable to the user in determining whether the change caused by versioning will affect their analysis work.


Reference
------------

Note that in this case Version 1 of Var\_1234 originally appeared in Version 1 of VS\_IPUMS.
However, the sourceContext indicates that VS\_IPUMS:4 is the context at the point of reference.

::

  <l:VariableReference isReference="true" isExternal="false" lateBound="false" objectLanguage="en" sourceContext="urn:ddi:us.mpc:VS\_IPUMS:4.0">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:Var\_1234:1.0
    </r:URN>
    <r:Agency>us.mpc</r:Agency>
    <r:ID>Var\_1234</r:ID>
    <r:Version>1.0</r:Version>
    <r:TypeOfObject>Variable</r:TypeOfObject>
    <r:MaintainableObject>
      <r:TypeOfObject>VariableScheme</r:TypeOfObject>
      <r:MaintainableID>VS\_IPUMS</r:MaintainableID>
      <r:MaintainableVersion>1.0</r:MaintainableVersion>
    </r:MaintainableObject>
  </l:VariableReference>

Minimum required content of the above::

  <l:VariableReference isReference="true" isExternal="false" lateBound="false">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:Var\_1234:1.0
    </r:URN>
    <r:TypeOfObject>Variable</r:TypeOfObject>
  </l:VariableReference>

Above reference as a lateBound reference where the most recent minor
version of major version 1 of the variable is being requested.::

  <l:VariableReference isReference="true" isExternal="false" lateBound="true" objectLanguage="en" sourceContext="urn:ddi:us.mpc:VS\_IPUMS:4.0" lateBoundRestriction="1">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:Var\_1234:1.0
    </r:URN>
    <r:Agency>us.mpc</r:Agency>
    <r:ID>Var\_1234</r:ID>
    <r:Version>1.0</r:Version>
    <r:TypeOfObject>Variable</r:TypeOfObject>
    <r:MaintainableObject>
      <r:TypeOfObject>VariableScheme</r:TypeOfObject>
      <r:MaintainableID>VS\_IPUMS</r:MaintainableID>
      <r:MaintainableVersion>1.0</r:MaintainableVersion>
    </r:MaintainableObject>
  </l:VariableReference>

SchemeReference
-----------------

::

  <l:VariableSchemeReference isReference="true" isExternal="false" lateBound="false" objectLanguage="en">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:VS\_IPUMS:1.0
    </r:URN>
    <r:Agency>us.mpc</r:Agency>
    <r:ID>VS\_IPUMS</r:ID>
    <r:Version>1.0</r:Version>
    <r:TypeOfObject>VariableScheme</r:TypeOfObject>
    <r:Exclude isReference="true" isExternal="false" lateBound="false" typeOfIdentifier="Canonical">
      <r:URN>urn:ddi:us.mpc:Var\_1234:1.0</r:URN>
      <r:TypeOfObject>Variable</r:TypeOfObject>
    </l:Exclude>
  </l:VariableSchemeReference>

Minimum required content of the above::

  <l:VariableSchemeReference isReference="true" isExternal="false" lateBound="false" objectLanguage="en">
    <r:URN typeOfIdentifier="Canonical">
      urn:ddi:us.mpc:VS\_IPUMS:1.0
    </r:URN>
    <r:TypeOfObject>VariableScheme</r:TypeOfObject>
    <r:Exclude isReference="true" isExternal="false" lateBound="false" typeOfIdentifier="Canonical">
      <r:URN>urn:ddi:us.mpc:Var\_1234:1.0</r:URN>
      <r:TypeOfObject>Variable</r:TypeOfObject>
    </l:Exclude>
  </l:VariableSchemeReference>

In / Out Parameter, Binding and Command Code
---------------------------------------------

::

 <g:ResourcePackage xmlns:ddi="ddi:instance:3_2" xmlns:a="ddi:archive:3_2" xmlns:c="ddi:conceptualcomponent:3_2" xmlns:cm="ddi:comparative:3_2" xmlns:d="ddi:datacollection:3_2" xmlns:g="ddi:group:3_2" xmlns:l="ddi:logicalproduct:3_2"
                  xmlns:p="ddi:physicaldataproduct:3_2" xmlns:pi="ddi:physicalinstance:3_2" xmlns:pr="ddi:ddiprofile:3_2" xmlns:r="ddi:reusable:3_2" xmlns:s="ddi:studyunit:3_2" xmlns:dc="http://purl.org/dc/elements/1.1/"
                  xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_2 http://www.ddialliance.org/Specification/DDI-Lifecycle/3.2/XMLSchema/instance.xsd">
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
     <r:URN>urn:ddi:us.mpc:QC_IN_2:1  </r:URN>
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
      <d:Text xml:lang="en" xml:space="default">What is the name of your oldest child?  </d:Text>
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
      <d:Text xml:lang="en" xml:space="preserve">How old is</d:Text>
     </d:LiteralText>
     <d:ConditionalText>
      <r:SourceParameterReference isReference="true" isExternal="false" lateBound="false">
       <r:URN>urn:ddi:us.mpc:Q2_Name:1</r:URN>
       <r:TypeOfObject>InParameter</r:TypeOfObject>
      </r:SourceParameterReference>
     </d:ConditionalText>
     <d:LiteralText>
      <d:Text xml:lang="en" xml:space="preserve"> ?  </d:Text>
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
       <r:URN>urn:ddi:us.mpc:GI_Age:1  </r:URN>
       <r:Alias>AGE  </r:Alias>
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


