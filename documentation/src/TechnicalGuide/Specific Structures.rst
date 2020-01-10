Specific Structures (by Topic)
===============================

This will link through to the DDI Model documentation, each topic needs some form of description / introduction.

Administration
--------------
A description of what adminstration means ......

- DDIInstance
- DDIProfile
- Group
- LocalHoldingPackage
- OtherMaterial
- ResourcePackage
- StudyUnit

Classification
---------------
- ClassificationCorrespondenceTable
- ClassificationFamily
- ClassificationIndex
- ClassificationItem
- ClassificationLevel
- ClassificationSeries
- StatisticalClassification

Comparison
------------
- Comparison
- GenericMap
- RepresentationMap

Data Capture
-------------

DDI-L supports both data capture from questions and measurements. The latter being introduced in DDI-L 3.3.

Questions
...........

As the complexity of question structures has increased, three general question structures have been identified within DDI and are addressed by the following specific structures: QuestionItem, QuestionGrid, and QuestionBlock. 

Note that all three structures reflect the reusable structure of various question types and do not relay any information on the applied use of the question within an instrument. The applied information, including question order, is captured by the ControlConstruct structures used by the Instrument. 

All question structures are maintained within a QuestionScheme and can be further organized for administrative purposes by QuestionGroup (a standard grouping structure available in most schemes). Only QuestionItem, QuestionGrid, and QuestionBlock may be referenced by a QuestionConstruct. 

A Sequence (type of ControlConstruct) is used to order questions within an instrument and is maintained separately as a reusable object. All question structures are versionable and contain a name for the question. All response domains may be described inline while a set of commonly used structures may be captured as managed representations and be reused by reference. These include Missing Values, Text, Numeric, DateTime, and Scale.

QuestionItem
^^^^^^^^^^^^^

A QuestionItem is a basic question containing a QuestionIntent, the concept being measured by the question, text for the question, response domain information, clarifying instructions, external aids (clarifying objects used in presenting the question to the respondent), Input and Output Parameters and Bindings, allowed response cardinality and an estimation of the time required to respond. The QuestionText is a DynamicTextString. Note that due to the variation of content in the QuestionText that is required to illicit equivalent responses in different languages, QuestionText is repeatable. A StructuredMixedResponseDomain supports situations where a response may include more than one type of response domain. This could be the inclusion of a set of Missing Values (responses that capture non-response and other values to be treated as invalid during analysis), or the commonly used addition of a text response to capture specific information when the code or category response is “Other”. StructuredMixedResponse allows for the addition of text and/or another response domain to be attached to one or more values of the primary response domain as well as stacking combinations of response options with intervening text.

QuestionGrid
^^^^^^^^^^^^^

A QuestionGrid provides a multidimensional structure used to capture a complex response. In many cases these are simple structures, for example a question regarding an assessment of each of a list of candidates for political office. However, some grids are complex and capture different responses for each of a list of items. In addition, the list may be provided by the question or by the respondent (indicated by the use of a “roster” of blank text items). A QuestionGrid contains the basic elements of the QuestionItem but rather than a ResponseDomain or StructuredMixedResponseDomain contains a GridDimension that sorts one or more ResponseDomains or StructuredMixedGridResponseDomains into a specific dimension of the grid. The structure is similar to the NCube dimensional structure using code domain or roster rather than variables to structure the dimension, and then providing a response domain for each cell in the grid. A single ResponseDomain indicates that this is the response domain for each cell in the grid. Note that an internal cell label may be added to any cell for clarification purposes.

QuestionBlock 
^^^^^^^^^^^^^^^

A QuestionBlock is intended to bundle together a set of questions (items and/or grids) that have meaning only in relation to a specified object expressed as the stimulus material. This form of question set is common in educational testing where a text, image, or other material is provided and the respondent is asked questions specific to the material. For example, a portion of a play script is provided and the respondent is asked question concerning the dialog and/or stage directions provided in the script. Note that the intent of QuestionBlock is NOT to bundle together a set of questions that are commonly used together or used in a specified order. 

A Sequence (type of control construct) is the appropriate way to manage this type of set relationship. It is assumed that one or more StimulusMaterial objects will be used. The 0..n cardinality of the CHOICE of StimulusMaterial, QuestionItemReference, and QuestionGridReference is provided simply to support the use of DDI during the development process when this piece of information may be unavailable. StimulusMaterial is part of this choice to allow for its insertion at any location before, after, or in the midst of the referenced Questions.

QuestionBlock contains the standard elements of QuestionItem and QuestionGrid and then structures any combination of StimulusMaterial with referenced QuestionItems and QuestionGrids. It allows for an indication of QuestionSequence (i.e., a means of declaring the sequence is important or that it can be randomized or otherwise altered).

MeasurementItem
^^^^^^^^^^^^^^^^

A MeasurementItem is analagous to a QuestionItem, the difference being that the QuesitonText is replaced by a TypeofMeasurementItem which is a CodeValueType for which a controlled vocabulary mey be used, and a MeasurementItemIntent which is a textual description of what the MeasurementItem is designed to measure.

ControlConstructs
...................

The following items are designed to be used to control the flow or processing within an Instrument

- ComputationItem
- GeneralInstruction
- GenerationInstruction
- IfThenElse
- Loop
- MeasurementConstruct
- ProcessingEvent
- QuestionConstruct
- RepeatUntil
- RepeatWhile
- Sequence
- StatementItem
- Split
- SplitJoin

Other
...........

- DataCollection
- Instrument
- Instruction


Data Description
-----------------

- ConceptualVariable
- DataRelationship
- DataSet
- LogicalProduct
- ManagedDateTimeRepresentation
- ManagedMissingValuesRepresentation
- ManagedNumericRepresentation
- ManagedScaleRepresentation
- ManagedTextRepresentation
- NCube
- PhysicalDataProduct
- PhysicalInstance
- PhysicalStructure
- QualityStandard
- QualityStatement
- RecordLayout
- RepresentedVariable
- Variable
- VariableStatistics
- Weighting
- WeightingMethodology

Foundational
--------------

- Category
- CodeList
- Concept
- ConceptualComponent
- Individual
- Organization
- Relation
- SubUniverseClass
- UnitType
- Universe

Geographic
-------------

- GeographicLocation
- GeographicStructure

Grouping
--------

- CategoryGroup
- CodeListGroup
- ConceptGroup
- ConceptualVariableGroup
- ControlConstructGroup
- DevelopmentActivityGroup
- GeographicLocationGroup
- GeographicStructureGroup
- Group
- InstructionGroup
- InstrumentGroup
- ManagedRepresentationGroup
- MeasurementGroup
- NCubeGroup
- OrganizationGroup
- OtherMaterialGroup
- PhysicalInstanceGroup
- PhysicalStructureGroup
- ProcessingEventGroup
- ProcessingInstructionGroup
- QualityStandardGroup
- QualityStatementGroup
- QuestionGroup
- RecordLayoutGroup
- RepresentedVariableGroup
- UnitTypeGroup
- UniverseGroup
- VariableGroup

Schemes
--------

Schemes are designed to bring together sets of similar objects (i.e. Variables, Concepts, RecordLayouts, etc.) which are managed as a unit for either conceptual or administrative purposes. Schemes have a common structure providing descriptive information about the scheme, a set of similar objects, and the ability to group those objects for administrative purposes.

- CategoryScheme
- CodeListScheme
- ConceptScheme
- ConceptualVariableScheme
- ControlConstructScheme
- DevelopmentActivityScheme
- GeographicLocationScheme
- GeographicStructureScheme
- InstrumentScheme
- InterviewerInstructionScheme
- ManagedRepresentationScheme
- MeasurementScheme
- NCubeScheme
- OrganizationScheme
- OtherMaterialScheme
- PhysicalStructureScheme
- ProcessingEventScheme
- ProcessingInstructionScheme
- QualityScheme
- QuestionScheme
- RecordLayoutScheme
- RepresentedVariableScheme
- SamplingInformationScheme
- UnitTypeScheme
- UniverseScheme
- VariableScheme

Study
-------

- Archive
- Group
- StudyUnit

Survey Development
-------------------

- CognitiveExpertReviewActivity
- CognitiveInterviewActivity
- ContentReviewActivity
- DataCaptureDevelopment
- DevelopmentImplementation
- DevelopmentPlan
- DevelopmentResults
- DevelopmentStep
- FocusGroupActivity
- Methodology
- PretestActivity
- Sample
- SampleFrame
- SampleStep
- SamplingInformationGroup
- SamplingPlan
- SamplingStage
- TranslationActivity
- WeightingMethodology










