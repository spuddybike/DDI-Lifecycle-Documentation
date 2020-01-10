Change Log
============

Change Notes for Conversion of DDI-Lifecycle 3.2 Instances to DDI-Lifecycle 3.3
 
+----------------------------+-----------------------------------+-------------------------------+
| **CHANGE Number**          | **NOTES**                         | **SCHEMA**                    |
+============================+===================================+===============================+
| 1                          | CodeValueType and                 | reusable.xsd                  |
|                            | Inter                             |                               |
|                            | nationalCodeValueType             |                               |
|                            | have had all                      |                               |
|                            | attribute names                   |                               |
|                            | changed from                      |                               |
|                            | codeListXxx to                    |                               |
|                            | controlledVocabularyXxx.          |                               |
|                            | This aligns the                   |                               |
|                            | naming with the                   |                               |
|                            | Controlled                        |                               |
|                            | Vocabularies                      |                               |
|                            | published by the DDI              |                               |
|                            | and prevents name                 |                               |
|                            | conflicts with the                |                               |
|                            | element CodeList in               |                               |
|                            | the DDI schemas. Note             |                               |
|                            | controlledVocabularyVersionID     |                               |
|                            | has changed from a                |                               |
|                            | default value of                  |                               |
|                            | “1.0” to “optional”.              |                               |
|                            | Change all                        |                               |
|                            | codeListXxx attribute             |                               |
|                            | names to                          |                               |
|                            | controlledVocabularyXxx           |                               |
|                            | names. If relying on              |                               |
|                            | the default value for             |                               |
|                            | controlledVocabularyXxx           |                               |
|                            | add the value “1.0”               |                               |
|                            | to your instance.                 |                               |
|                            | NOTE that the old                 |                               |
|                            | codeListName                      |                               |
|                            | attribute has a name              |                               |
|                            | conflict with the new             |                               |
|                            | CodeListName added to             |                               |
|                            | CodeListType.                     |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 2                          | ComponentParts                    | reusable.xsd                  |
|                            | changed from                      |                               |
|                            | type=”ComponentPartsType”         |                               |
|                            | to                                |                               |
|                            | type=”LocationValueBundleType”    |                               |
|                            | This makes it the                 |                               |
|                            | same base as used for             |                               |
|                            | the new                           |                               |
|                            | “ImmediateParentLocation”.        |                               |
|                            | The only structural               |                               |
|                            | difference between                |                               |
|                            | the old                           |                               |
|                            | ComponentPartsType and            |                               |
|                            | LocationValueBundleType           |                               |
|                            | is that                           |                               |
|                            | LocationValueReference            |                               |
|                            | changed from a                    |                               |
|                            | cardinality of 0..1               |                               |
|                            | to a cardinality of               |                               |
|                            | 0..n. Change does not             |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 3                          | The ControlConstruct              | datacollection.xsd            |
|                            | reference no longer               |                               |
|                            | supports the use of               |                               |
|                            | binding. If this is               |                               |
|                            | required for                      |                               |
|                            | specifying the path               |                               |
|                            | of data into a                    |                               |
|                            | Variable, route it                |                               |
|                            | through a                         |                               |
|                            | ProcessingInstruction.            |                               |
|                            | The                               |                               |
|                            | ProcessingInstructionReference    |                               |    
|                            | continues to support              |                               |
|                            | the use of binding.               |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 4                          | DefiningConceptReference          | conceptualcomponent.xsd       |
|                            | moved from                        |                               |
|                            | conceptualcomponent.xsd           |                               |
|                            | to reusable.xsd. Used             |                               |
|                            | by UniverseType and               |                               |
|                            | SubUniverseType.                  |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 5                          | Extension base of                 | datacollection.xsd            |
|                            | GenerationInstruction             |                               |
|                            | and                               |                               |
|                            | GeneralInstruction                |                               |
|                            | changed from                      |                               |
|                            | r:VersionableType to              |                               |
|                            | ProcessingInstructionType.        |                               |
|                            | Change does not                   |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 6                          | Extension base of                 | archive.xsd                   |
|                            | Individual and                    |                               |
|                            | Organization changed              |                               |
|                            | from                              |                               |
|                            | r:VersionableType to              |                               |
|                            | ArchiveType. Change               |                               |
|                            | does not affect                   |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 7                          | CountryCode changes               | reusable.xsd                  |
|                            | from a prescribed use             |                               |
|                            | of DDI country codes              |                               |
|                            | where were not                    |                               |
|                            | published to a                    |                               |
|                            | standard                          |                               |
|                            | CodeValueType. Change             |                               |
|                            | affects parsing only              |                               |
|                            | if the default values             |                               |
|                            | were used as a) the               |                               |
|                            | names of the                      |                               |
|                            | attributes have                   |                               |
|                            | changed (see Change               |                               |
|                            | #1) and b) the                    |                               |
|                            | referenced codes were             |                               |
|                            | not published.                    |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 8                          | Extension base of                 | datacollection.xsd            |
|                            | QuestionItem,                     |                               |
|                            | QuestionGrid, and                 |                               |
|                            | QuestionBlock changed             |                               |
|                            | from                              |                               |
|                            | r:VersionableType to              |                               |
|                            | QuestionType. Change              |                               |
|                            | does not affect                   |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 9                          | BUG FIX: Element                  | physicalinstance.xsd          |
|                            | declaration                       |                               |
|                            | name=”FilterCategoryValueType”    |                               |
|                            | type=”CategoryValueType”          |                               |
|                            | was corrected to                  |                               |
|                            | name=”FilterCategoryValue”        |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 10                         | GridResponseDomain (used in       | datacollection.xsd            |
|                            | StructuredMixedGrid		 |                               |
|                            | ResponseDomainType)               |                               |
|                            | changed to                        |                               |
|                            | GridResponseDomainInMixed.        |                               |
|                            | GridResponseDomainInMixedType     |                               |
|                            | retains all of the                |                               |
|                            | content of                        |                               |
|                            | GridResponseDomainType            |                               |
|                            | and adds                          |                               |
|                            | ResponseAttachmentLocation        |                               |
|                            | and attachementBase.              |                               |
|                            | Change                            |                               |
|                            | d:GridResponseDomain              |                               |
|                            | to                                |                               |
|                            | d:GridResponseDomainInMixed       |                               |
|                            | and                               |                               |
|                            | d:G ridResponseDomainType         |                               |
|                            | to                                |                               |
|                            | d:GridResponseDomainInMixedType.  |                               | 
+----------------------------+-----------------------------------+-------------------------------+
| 11                         | Extension base of                 | reusable.xsd                  |
|                            | OtherMaterialType                 |                               |
|                            | changed from                      |                               |
|                            | IdentifiableType to               |                               |
|                            | VersionableType.                  |                               |
|                            | Change isIdentifiable=”true”      |                               |
|                            | to isVersionable=”true”           |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 12                         | Interval changes name             | reusable.xsd                  |
|                            | to InveralIncrement               |                               |
|                            | (element declaration              |                               |
|                            | and use in                        |                               |
|                            | LevelType). The                   |                               |
|                            | element type has not              |                               |
|                            | changed. Change name              |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 13                         | Removed maxOccurs=”1”             | reusable.xsd                  |
|                            | on ContributorType                |                               |
|                            | referenced element                |                               |
|                            | ContributorReference              |                               |
|                            | as redundant. Change              |                               |
|                            | does not affect                   |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 14                         | AggregationType                   | datacollection.xsd            |
|                            | xs:choice (1..1) of               |                               |
|                            | AggregationVariable               |                               |
|                            | (0..1) or                         |                               |
|                            | AggregationVariableReference      |                               |
|                            | (0..1) corrected to               |                               |
|                            | remove cardinality                |                               |
|                            | from elements                     |                               |
|                            | contained in the                  |                               |
|                            | choice. xs:choice                 |                               |
|                            | cardinality has be                |                               |
|                            | loosened to 0..1                  |                               |
|                            | Change does not                   |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 15                         | ConditionalTextType               | datacollection.xsd            |
|                            | xs:choice (1..1) of               |                               |
|                            | Express (0..1) or                 |                               |
|                            | r:SourceParameterReference        |                               |
|                            | (0..1). Removed                   |                               |
|                            | element cardinality               |                               |
|                            | statement of                      |                               |
|                            | minOccurs=”0” as                  |                               |
|                            | redundant Change does             |                               |
|                            | not affect parsing.               |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 16                         | AttachmentLocationType            | datacollection.xsd            |
|                            | xs:choice cardinality             |                               |
|                            | minOccurs=”1” removed             |                               |
|                            | as redundant Change               |                               |
|                            | does not affect                   |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 17                         | AbtractIdentifiableType           | reusable.xsd                  |
|                            | and Refrencetype                  |                               |
|                            | xs:choice of URN or               |                               |
|                            | sequence [Agency, ID,             |                               |
|                            | Version] cardinality              |                               |
|                            | minOccurs=”1” removed             |                               |
|                            | as redundant Change               |                               |
|                            | does not affect                   |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 18                         | BUG:                              | physicalinstance.xsd          |
|                            | FilterVariableCategoryType        |                               |
|                            | contained element                 |                               |
|                            | name=”FilterCategoryValue”        |                               |
|                            | to                                |                               |
|                            | ref=”FilterCategoryValue”.        |                               |
|                            | If a value is                     |                               |
|                            | provided change                   |                               |
|                            | <pi:FilterCategoryValue>          |                               |
|                            | [value]</pi:FilterCategoryValue>  |                               | 
|                            | to                                |                               |
|                            | <pi:FilterCategoryValue><r:Value> |                               |
|                            | [value]</r:Value>                 |                               |
|                            | </pi:FilterCategoryValue>         |                               |
|                            | OR if the reference               |                               |
|                            | to a Code was                     |                               |
|                            | provided change                   |                               |
|                            | <pi:FilterCategoryValue>[URN]     |                               |
|                            | </pi:FilterCategoryValue>         |                               |
|                            | to                                |                               |
|                            | <pi:FilterCategoryValue>          |                               |
|                            | <r:CodeRefence><r:URN>[URN]       |                               |
|                            | </r:URN><r:TypeOfObject>          |                               |
|                            | Code</r:TypeOfObject>             |                               |
|                            | </r:CodeReference>                |                               |
|                            | </pi:FilterCategoryValue>         |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 19                         | BUG: IncludedCodeName             | reusable.xsd                  |
|                            | contained element                 |                               |
|                            | name=”CodeReference”              |                               |
|                            | to                                |                               |
|                            | ref=”CodeReference”               |                               |
|                            | Change                            |                               |
|                            | <r:CodeReference>[URN]            |                               |
|                            | </r:CodeReference > to            |                               |
|                            | <r:CodeRefence><r:URN>[URN]       |                               |
|                            | </r:URN><r:TypeOfObject>Code      |                               |
|                            | </r:TypeOfObject>                 |                               |
|                            | </r:CodeReference>                |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 20                         | BUG:                              | reusable.xsd                  |
|                            | DimensionRankValueType            |                               |
|                            | contained element                 |                               |
|                            | name=”Value” to                   |                               |
|                            | ref=”Value” Change                |                               |
|                            | does not affect                   |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 21                         | OtherStatementOfQuality           | reusable.xsd                  |
|                            | type changed name                 |                               |
|                            | from                              |                               |
|                            | OtherQualityStatement             |                               |
|                            | to                                |                               |
|                            | OtherStatementOfQuality.          |                               |
|                            | Change all occurances             |                               |
|                            | of                                |                               |
|                            | OtherQualityStatement             |                               |
|                            | to                                |                               |
|                            | OtherStatementOfQuality           |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 22                         | Renamed                           | reusable.xsd                  |
|                            | ProcessingInstructionReferenceType|                               |
|                            | to                                |                               |
|                            | ReferenceWithBindingType.         |                               |
|                            | Changed                           |                               |
|                            | ProcessInstructionReference       |                               |
|                            | from                              |                               |
|                            | ProcessingInstructionReferenceType|                               |
|                            | to                                |                               |
|                            | ReferenceWithBindingType.         |                               |
|                            | Change does not                   |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 23                         | Renamed the following             | reusable.xsd                  |
|                            | names related to                  |                               |
|                            | Quality:                          |                               |
|                            | QualityStatementSchemeName        |                               |
|                            | to QualitySchemeName;             |                               |
|                            | QualityStatementSchemeReference   |                               |
|                            | to                                |                               |
|                            | QualitySchemeReference;           |                               |
|                            | QualityStatementSchemeType        |                               |
|                            | to QualitySchemeType;             |                               |
|                            | and                               |                               |
|                            | QualityStatementScheme            |                               |
|                            | to QualityScheme.                 |                               |
|                            | Change all occurances             |                               |
|                            | of these names                    |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 24                         | ExternalAid and                   | datacollection.xsd            |
|                            | ExternalInformation               |                               |
|                            | changed from                      |                               |
|                            | r:OtherMaterialType               |                               |
|                            | to an unidentified                |                               |
|                            | object containing a               |                               |
|                            | choice of                         |                               |
|                            | r:OtherMaterial or                |                               |
|                            | r:OtherMaterialReference.         |                               |
|                            | Change example: FROM              |                               |
|                            | <d:ExternalAid                    |                               |
|                            | isIdentifiable=                   |                               |
|                            | ”true”>[OtherMaterialcontent]     |                               |
|                            | </d:ExternalAid>                  |                               |
|                            | TO                                |                               |
|                            | <d:ExternalAid><r:OtherMaterial   |                               |
|                            | isVersionable=”true”>		 |                               |
|                            | [OtherMaterialcontent]            |                               |
|                            | </r:OtherMaterial>                |                               |
|                            | </d:ExternalAid>                  |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 25                         | In RepresentedVariableType        | logicalproduct.xsd            |
|                            | r:UniverseReference               |                               |
|                            | changed to                        |                               |
|                            | r:UnitTypeReference               |                               |
|                            | Change contained                  |                               |
|                            | element in                        |                               |
|                            | RepresentedVariableType           |                               |
|                            | from                              |                               |
|                            | r:UniverseReference               |                               |
|                            | to                                |                               |
|                            | r:UnitTypeReference               |                               |
|                            | This will require                 |                               |
|                            | creation of                       |                               |
|                            | c:UnitType content,               |                               |
|                            | change of referenced              |                               |
|                            | URN, and change of                |                               |
|                            | TypeOfObject in                   |                               |
|                            | reference to UnitType             |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 26                         | RepresentedVariableReference      | logicalproduct.xsd            |
|                            | moved from                        |                               |
|                            | logicalproduct.xsd to             |                               |
|                            | reusable.xsd Change               |                               |
|                            | FROM                              |                               |
|                            | <l:RepresentedVariableReference>  |                               |
|                            | TO                                |                               |
|                            | <r:RepresentedVariableReference>  |                               |
|                            | in                                |                               |
|                            | RepresentedVariableSchemeType     |                               |
|                            | and                               |                               |
|                            | RepresentedVariableGroupType      |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 27                         | GenericMapType                    | comparative.xsd               |
|                            | elements                          |                               |
|                            | SourceSchemeReference             |                               |
|                            | and                               |                               |
|                            | TargetSchemeReference             |                               |
|                            | changed from                      |                               |
|                            | cardinality 1..1 to               |                               |
|                            | 0..1 Change does not              |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 28                         | ItemMapType elements              | comparative.xsd               |
|                            | changed from                      |                               |
|                            | SourceItem and                    |                               |
|                            | TargetItem to                     |                               |
|                            | SourceItemReference               |                               |
|                            | to                                |                               |
|                            | TargetItemReference.              |                               |
|                            | SourceItem and                    |                               |
|                            | TargetItem both                   |                               |
|                            | changed from                      |                               |
|                            | type=”r:IDType” to                |                               |
|                            | type=”r:Reference”                |                               |
|                            | Change to full                    |                               |
|                            | Reference content                 |                               |
|                            | Example: FROM                     |                               |
|                            | <cm:SourceItem>[ID]               |                               |
|                            |</cm:SourceItem>                   |                               |
|                            | TO                                |                               |
|                            | <cm:SourceItemReference><r:URN>   |                               |
|                            | urn:ddi:[agency]:[ID]             |                               |
|                            | :[version]</r:URN>                |                               |
|                            | <r:TypeOfObject>[objecttype]      |                               |
|                            | </r:TypeOfObject>                 |                               |
|                            | </cm:SourceItemReference>         |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 29                         | DDIMaintenanceAgencyIDType        | archive.xsd                   |
|                            | attribute startDate               |                               |
|                            | changes name to                   |                               |
|                            | activationDate Change             |                               |
|                            | name of attribute                 |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 30                         | BudgetDocuement and               |                               |
|                            | StimulasMaterial were             |                               |
|                            | changed from                      |                               |
|                            | type=”OtherMaterial”              |                               |
|                            | to                                |                               |
|                            | type=”BudgetDocumentType”         |                               |
|                            | and                               |                               |
|                            | type=”StimulasMaterialType”.      |                               |
|                            | These new objects are             |                               |
|                            | not identifiable and              |                               |
|                            | bundle together an                |                               |
|                            | inline and by                     |                               |
|                            | reference option for              |                               |
|                            | OtherMaterial. To                 |                               |
|                            | change existing                   |                               |
|                            | content to comply                 |                               |
|                            | with 3.3 change:                  |                               |
|                            |                                   |                               |
|                            | -  Change the name of             |                               |
|                            |    the object to                  |                               |
|                            |    r:OtherMaterial                |                               |
|                            |                                   |                               |
|                            | -  Wrap the content               |                               |
|                            |    in an element with             |                               |
|                            |    the former name                |                               |
|                            |                                   |                               |
|                            | -  Any references to              |                               |
|                            |    the object will                |                               |
|                            |    need the                       |                               |
|                            |    TypeOfObject                   |                               |
|                            |    changed to                     |                               |
|                            |    “OtherMaterial”                |                               |
|                            |                                   |                               |
|                            | -  Example:                       |                               |
|                            |                                   |                               |
|                            | <r:BudgetDocument>                |                               |
|                            | <r:URN>				 |                               |
|                            | ddi:urn:int.example:BD1111:1	 |                               |
|                            | </r:URN>                          |                               |
|                            | </r:BudgetDocument>               |                               |
|                            |                                   |                               |
|                            | TO                                |                               |
|                            |                                   |                               |
|                            | <r:BudgetDocument>                |                               |
|                            | <r:OtherMaterial>                 |                               |
|                            | <r:URN>				 |                               |
|                            | ddi:urn:int.example:BD1111:1	 |                               |
|                            | </r:URN>                          |                               |
|                            | </r:OtherMaterial>                |                               |
|                            | </r:BudgetDocument>               |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 31                         | Extension base for                | reusable.xsd                  |
|                            | all Managed                       |                               |
|                            | Representations was               |                               |
|                            | changed from                      |                               |
|                            | VersionableType to                |                               |
|                            | the new                           |                               |
|                            | ManagedRepresentationType.        |                               |
|                            | Change does not                   |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 32                         | Change of datatype                | various                       |
|                            | from xs:integer to                |                               |
|                            | xs:nonNegativeInteger             |                               |
|                            | was made in                       |                               |
|                            | allocations where a               |                               |
|                            | negative number would             |                               |
|                            | not be applicable by              |                               |
|                            | definition, such as               |                               |
|                            | the number of items               |                               |
|                            | in a collection.                  |                               |
|                            | Locations are noted               |                               |
|                            | is spreadsheet.                   |                               |
|                            | Change does not                   |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 33                         | OtherMaterial is now              | reusable.xsd                  |
|                            | versionable and has               |                               |
|                            | been moved to the                 |                               |
|                            | Versionable section               |                               |
|                            | of TypeOfObjectType               |                               |
|                            | enumerations. Change              |                               |
|                            | does not affect                   |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 34                         | RepresentedVariableType           | logicalproduct.xsd            |
|                            | xs:choice for                     |                               |
|                            | r:ConceptualVariableReference     |                               |
|                            | or the xs:sequence                |                               |
|                            | [r:UnitTypeReference              |                               |
|                            | (0..1) and                        |                               |
|                            | r:ConceptReference                |                               |
|                            | (0..1) the                        |                               |
|                            | cardinality statement             |                               |
|                            | on                                |                               |
|                            | r:ConceptualVariableReference     |                               |
|                            | was moved from                    |                               |
|                            | r:ConceptualVariableReference     |                               |
|                            | to the xs:choice as               |                               |
|                            | 0..1. The provides                |                               |
|                            | the option of not                 |                               |
|                            | providing this                    |                               |
|                            | information and                   |                               |
|                            | clarifies the option              |                               |
|                            | for the choice.                   |                               |
|                            | Change does not                   |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 35                         | FragmentType now only             | instance.xsd                  |
|                            | references an                     |                               |
|                            | r:OtherMaterial as                |                               |
|                            | the payload of the                |                               |
|                            | Fragment. The                     |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 36                         | BUG FIX: BaseIDType               | reusable.xsd                  |
|                            | and DDIAgencyIDType               |                               |
|                            | patterns were edited              |                               |
|                            | to allow a single “.”             |                               |
|                            | extension in the ID               |                               |
|                            | and multiple “.”                  |                               |
|                            | Extensions in the                 |                               |
|                            | AgencyID. Both are                |                               |
|                            | carried into the                  |                               |
|                            | composite URN                     |                               |
|                            | pattern. The use of               |                               |
|                            | “.”                               |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 37                         | xs:choice in                      | datacollection.xsd            |
|                            | StructuredMixedGridResponseDomain |                               |
|                            | changed cardinality               |                               |
|                            | from minOccurs=”0” to             |                               |
|                            | minOccurs=”2”. As the             |                               |
|                            | usage of                          |                               |
|                            | StructuredMixedGridResponseDomain |                               |
|                            | implied the use of 2              |                               |
|                            | or more response                  |                               |
|                            | domains this change               |                               |
|                            | should not affect                 |                               |
|                            | parsing.                          |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 38                         | In                                | datacollection.xsd            |
|                            | GenerationInstructionType         |                               |
|                            | change SourceQuestion             |                               |
|                            | to                                |                               |
|                            | InputQuestionReference            |                               |
|                            | and SourceVariable to             |                               |
|                            | InputVariableReference.           |                               |
|                            | A similar change has              |                               |
|                            | been made in the                  |                               |
|                            | element declarations.             |                               |
|                            | Note that these both              |                               |
|                            | continue to be of                 |                               |
|                            | type=”SourceReferenceType”.       |                               |
|                            | Change element name               |                               |
|                            | “SourceQuestion" to               |                               |
|                            | “InputQuestionReference”          |                               |
|                            | and “SourceVariable”              |                               |
|                            | to                                |                               |
|                            | InputVariableReference”           |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 39                         | In UsedType change                | ddiprofile.xsd                |
|                            | attribute                         |                               |
|                            | “defaultValue”                    |                               |
|                            | type=”xs:string” to               |                               |
|                            | element                           |                               |
|                            | ref=”r:DefaultValue”              |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 40                         | CitationType element              | reusable.xsd                  |
|                            | ref=”dc:elementsAndRefinements”   |                               |
|                            | has changed to                    |                               |
|                            | “dcterms:elementsAnRefinements”.  |                               |
|                            | Note that this                    |                               |
|                            | supports both “dc”                |                               |
|                            | and “dcterms”                     |                               |
|                            | namespaces. The file              |                               |
|                            | dcterms.xsd has been              |                               |
|                            | updated to the                    |                               |
|                            | current version.                  |                               |
|                            | Change does not                   |                               |
|                            | affect parsing.                   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 41                         | Change element name               | reusable.xsd                  |
|                            | “TopLevelReference”               |                               |
|                            | to                                |                               |
|                            | "HighestLevelReference”           |                               |
|                            | in “SpatialCoverage”              |                               |
|                            | (type=”GeographicCoverageType”)   |                               |
+----------------------------+-----------------------------------+-------------------------------+
| 42                         | In                                | reusable.xsd                  |
|                            | IdentifierParsingInformationType  |                               |
|                            | and                               |                               |
|                            | LimitedCodeSegmentCapturedType    |                               |
|                            | change attribute                  |                               |
|                            | name=”arrayBase” to               |                               |
|                            | element                           |                               |
|                            | ref=”ArrayBase” of                |                               |
|                            | type                              |                               |
|                            | xs:nonNegativeInteger.            |                               |
|                            | The attribute used                |                               |
|                            | ArrayBaseCodeType all             |                               |
|                            | values of which were              |                               |
|                            | xs:nonNegativeInteger             |                               |
+----------------------------+-----------------------------------+-------------------------------+


ChangeLog.xlsx contains a listing of all Additions, Removals, and
Changes made between DDI-Lifecycle version 3.2 and DDI-Lifecycle version
3.3

-  The CHANGE Note column on the sheet “Changes” corresponds to the
   change note above

-  Objects noted in the sheets “Additions” and “Removals” without a
   parent listed are element declarations

-  New ComplexTypes found in the “Additions” list do not provide
   complexContent details, those are found in the schemas and
   documentation

For a complete listing of issues reviewed in the development of
DDI-Lifecycle version 3.3 see:

https://ddi-alliance.atlassian.net/issues/?filter=11223
