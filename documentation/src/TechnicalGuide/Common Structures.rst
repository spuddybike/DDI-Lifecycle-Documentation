Commonly Used Structures
===========================

DDI Instance and DDI Fragments
------------------------------

TODO
......


Name, Label, and Description
-----------------------------

DDI modules designed to contain published objects (DDIInstance,
StudyUnit, Group, ResourcePackage, LocalHoldingPackage, and
PhysicalInstance) all contain full citation information which provides
detailed information on the name of the object, as well as means of
labeling and describing it. DDI has identified a number of objects,
primarily non-publication structure modules, schemes, and versionable
objects within schemes as items that have the potential to be managed in
an ISO/IEC 11179 type repository. In line with ISO/IEC 11179-5, DDI has
provided this set of objects with a sequence of a name, label, and
description. Label and Description are standard structures.

Name
.....

Name is used as a type specification for a specific object name, i.e.
VariableName type=”r:NameType”. A complete listing of objects of
NameType will be found in Appendix: X.

A name is what an object is called within a registry. All elements of
type NameType may be repeated to supply different names for different
contexts, such as different sections within a registry system. Do not
repeat the use of the NameType object to capture multilingual content.
This is handled by the base type, InternationalString [see pt2:2.5.1].
Each String within the NameType represents the same content in a
different language. Each language string can be identified by its
language designation (with optional country specification, i.e. en-UK),
with information on whether the content was translated, can be
translated (i.e. is not machine code), the source langauges for the
translation, and the translation date. The two attributes specific to
NameType identify the preferred name if multiple name sets are available
and capture the context within which the specified name is used. If the
element of type NameType is repeated, it is the attribute context which
is used to disambiguate between the options. The attribute isPreferred
allows the content creator to designate the preferred or default name
for the object.

`NameType <http://www.ddialliance.org/Specification/DDI-Lifecycle/3.2/XMLSchema/FieldLevelDocumentation/schemas/reusable_xsd/complexTypes/NameType.html>`_

Label
.......

A Label is intended to provide content for use in a display (a table layout, printed content, web site, etc.). In all locations where Label is used it may be repeated to reflect different types of label (i.e. a short label, or a full label, etc.). The Label uses an extension base of StructuredStringType which managed both multilingual content and allows for the use of a set of xhtml structure tags.

Differences in the intended use of each Label are expressed by the element TypeOfLabel and a set of attributes that apply to all language versions of the Label. The TypeOfLabel uses the extension base CodeValueType which supports the use of an external controlled
vocabulary (see pt2:2.5.1). The attribute locationVariant is an xs:string to allow for either a common geographic specification such as
a country code or a descriptive term (i.e. urban, northwest region, etc.). For Labels with a limited period of use the pair of attributes validForStartDate and validForEndDate allow clear specification for when a Label is valid. Finally the attribute maxLength is useful for identifying labels that must meet a specific length limitation, for example in publishing content within a specific format or software system.

`Label <http://www.ddialliance.org/Specification/DDI-Lifecycle/3.2/XMLSchema/FieldLevelDocumentation/schemas/reusable_xsd/elements/Label.html>`_

Description
............

Description is of type StructuredStringType with no additional extensions. It generally appears with a cardinality of 0..1. If it is
important to differentiate be original and added content it is possible to do this by using the content structure features of the
StructuredString (see pt2:2.5.1). Note that if the object containing the Name, Label, Description sequence may be used in a comparison process, providing content for Description is critical as comparison is based upon the comparison of the Description of the object, not its Name or Label.

`Description <http://www.ddialliance.org/Specification/DDI-Lifecycle/3.2/XMLSchema/FieldLevelDocumentation/schemas/reusable_xsd/elements/Description.html>`_

Note 
------

A Note is designed to capture local information related to one or more identifiable objects. Note is designed to be an inherent part of the DDI. The information may be passed along with a DDI object over its lifetime. It is not intended to replace formal extension mechanisms. Formal extension should be used whenever a locally used object needs to be added to the schema. However, run-time extension needs may arise and Note can be used to capture the required metadata and associate it with the appropriate object. 

Note may be used to capture information during processing which is then removed prior to publication. Removing a Note removes all the links to related objects within the DDI structure.

DDI recommends placing the Note within the maintainable object containing the objects referenced by the Note. Each note may indicate who is responsible for the note, its type using a controlled vocabulary, the subject of the note, a head and note content, a set of key/value pairs and language specification for the overall note. In addition each note must be related to one or more identifiable objects.

A Note may be classified by its type and subject. TypeOfNote should express the purpose of the note (e.g. processing note, request for review, run time extension, etc.). NoteSubject is used to express the topical subject of the Note. Both TypeOfNote and NoteSubject may be expressed using a controlled vocabulary. Relationship provides a reference to any object with an ID, preferably within the same maintainable, and a description of the relationship if needed for clarity. This is expressed as a structured string. The direction of the link between a Note and another object is always from the Note to the object. 

The Header provides a brief label or heading for the NoteContent which is expressed as a structured string. The provision of ProprietaryInfo (a StandardKeyValuePair) allows for the expression of the content as a tuple (attribute key and value pair) to support computer systems and applications. The overall language of the Note can be provided with the xml:lang attribute.

User Attribute Pairs
---------------------

UserAttributePair is a structure that supports the use of a user specified standard key value pair, this can be attached to any VersionableType, (these are listed in the documentation for UserAttributePair).

The intent of this structure is that it allows the addition of business specific metadata for primarily internal processes that is not likely to be widely shared between different organisations.

Examples of usage would be:

- Holding adhoc information about individuals such as place and date of birth, 
- Adding additional functionality to an existing element such as a controlled vocabulary to copyright to support internal systems.

Date
---------

With the exception of describing the date format in a data capture system or as it is represented in a data file, DDI requires the use of the standard ISO 860 formats for all machine actionable dates. ISO 860 uses the Gregorian calendar so dates in other calendars must be translated. The basic form of a date in DDI is the BaseDateType which is a union of ISO dates types including:

+--------------------+-------------------------+-----------------------+ 
| xml property       | ISO Format              | Example               |
+====================+=========================+=======================+
| xs:dateTime        | yyyy-mm-ddThh:mm:ss     | 1982-01-05T23:05:15   |
+--------------------+-------------------------+-----------------------+ 
| xs:date            | yyyy-mm-dd              | 1982-01-05            |
+--------------------+-------------------------+-----------------------+ 
| xs:gYearMonth      | yyyy-mm                 | 1982-01               |
+--------------------+-------------------------+-----------------------+ 
| xs:gYear           | yyyy                    | 1982                  |
+--------------------+-------------------------+-----------------------+ 
| xs:duration        | PnnYnnMnnDTnnHnnMnn     | SP26Y02M22DT11H05M20S |
+--------------------+-------------------------+-----------------------+ 

Note that all upper case letters are literals, for example, the “T” in dateTime is literal, denoting the beginning of the Time section. Seconds (ss) may contain decimals. Optionally, dateTime can be extended by a time zone offset of “Z” to represent Zulu time or GMT. For example, Eastern Standard Time is Z-4, Central Europe is Z+1.
“P” in xs:duration indicates that this is a Period of duration and the number precedes the type of period, (i.e., nnY is the number of Years). A period may be of negative duration by placing a negative sign before the “P”, for example a period of minus 10 days (-P10D).
Elements of DateType support the use of a single date or date range. Date ranges are assumed to be inclusive. While normally a range will have a StartDate and EndDate, DDI supports the use of open ranges where only the StartDate or EndDate is known. SimpleDate, StartDate, and EndDate are all BaseDateType.

All dates may be replicated in their HistoricalDate format to reflect how the date was expressed in original documentation. Historical date information parallels the simple date, start date and end date structures of the standard DateType. The date is captured as a string in NonISODate, the format is provided in HistoricalDateFormat (supports the use of a controlled vocabulary), and the calendar type may be specified in Calendar (supports the use of a controlled vocabulary). HistoricalDate, HistoricalStartDate, and HistoricalEndDate are all HistoricalDateType

The overall date format is composed of three primary structures, BaseDateType, DateType, and HistoricalDateType:

Eight elements are defined as DateType. Three additional elements use DateType as an extension base, adding specific additional elements or attributes to define the use of the date in that particular location. Five attributes use BaseDateType. Usage locations are listed below.

.. table:
   :width 60%
+---------------------------------------------------+ 
| Element using DateType                            |
+=========================+=========================+
| datacollection.xsd      | DataCollectionDate      |
+-------------------------+-------------------------+ 
| reusable.xsd            | EffectivePeriod         |
+-------------------------+-------------------------+ 
| reusable.xsd            | GeographicTime          |
+-------------------------+-------------------------+    
| reusable.xsd            | PublicationDate         |
+-------------------------+-------------------------+ 

.. table:
   :width 60%

+---------------------------------------------------+ 
| Element using extension base DateType             |
+=========================+=========================+
| datacollection.xsd      | DataCollectionFrequency |
+-------------------------+-------------------------+ 
| reusable.xsd            | AccessRestrictionDate   |
+-------------------------+-------------------------+ 
| reusable.xsd            | ReferenceDate           |
+-------------------------+-------------------------+ 

.. table:
   :width 60%

+---------------------------------------------------+ 
| Attribute using BaseDateType                      |
+=========================+=========================+
| reusable.xsd            | authorizationDate       |
+-------------------------+-------------------------+ 
| reusable.xsd            | completionDate          |
+-------------------------+-------------------------+ 
| reusable.xsd            | validForEndDate         |
+-------------------------+-------------------------+ 
| reusable.xsd            | validForStartDate       |
+-------------------------+-------------------------+ 
| reusable.xsd            | versionDate             |
+-------------------------+-------------------------+ 


In / Out Parameter, Binding and Command Code
---------------------------------------------

The set of classes, InParameter, OutParameter, Binding and CommandCode allow for specific tracking of a set of information (data) through processing. 

For example the response captured by a question is expressed as the OutParameter of the Question. 

A GenerationInstruction specifies that it has an InParameter which goes through a mathematical process resulting in an OutParameter content. A variable has an InParameter. 

Binding is used to link the OutParameter of the Question to the InParamter of the GenerationInstruction. 

The InParameter of the GenerationInstruction to a specific usage in a Command Code and the OutParameter of the GenerationInstruction to the InParameter of a Variable. 


Quality Descriptions
---------------------

DDI addresses descriptions of quality at three levels, the quality of the metadata as captured, means of ensuring policy for processing, and the quality of the data. Statements regarding the quality standards used for processing or measuring the quality of the data related to the metadata may be referenced from the following areas: study unit, group, sub-group, resource package, methodology, various descriptions of data processing, data file creation or copying, and archival processing.

Metadata Quality
_________________

Metadata quality is captured at the level of the Maintainable object and refers to the metadata contained in that object. It is held in the complex element MetadataQuality which is found in AbstractMaintainable. It is a relatively simple statement of quality such as completeness, transcription of content from the original source, level of review or verification, etc.

Both TypeOfMetadataQuality and MeasureValue are CodeValueType and support the use of an external controlled vocabulary. These are the two primary pieces of information needed to track metadata quality internally within an organization. TypeOfMetadataQuality identifies the measure being tracked and MeasureValue provides a specific value for that measure. For example, an organization may have a number of measures one of which rates its transcription quality. 

It may have various values for this including: 

- 1) Tagging and transfer of a digital content, 
- 2) double entry, 
- 3) single entry direct transcription, 
- 4) selected transcription, and 
- 5) summarization. T

he purpose for capturing the measure is held in MeasurePurpose (StructuredStringType) and other descriptive information that is useful to the organization or in particular a user, is held in Description (StructuredStringType).

Quality Statement
__________________

Quality statements are compiled in a QualityStatementScheme which may be published within a StudyUnit, Group, or ResourcePackage. Quality statements primarily address processes and steps that are taken to ensure quality within those processes. A QualityStatement allows for either the identification of an external standard plus a statement regarding compliance with that standard, or a general statement of steps taken to ensure quality for a given process or activity. A QualityStatement is attached to a processing area by reference from the description of the process/activity itself.

StandardsCompliance consists of a reference to the Standard using the structure of OtherMaterial. This could reference a document, web site, or other source containing a formal standard for processing, best practice, internal protocol, or other statement of quality. ComplianceDescription (StructuredStringType) provides details on how this standard or protocol was applied, in particular noting any deviations or issues that would have an impact on the quality factors being assessed. 

When no formal standard or protocol exists, use OtherQualityStatement (StructuredStringType to describe steps taken to ensure quality. Quality statements can be referenced from the following locations and should relate quality assessment information focused on the process activity or general coverage area where the reference is included.

Data Quality
_________________

The quality of the data collected is addressed in the ProcessingEvent containing DataAppraisalInformation. This contains two common measures of data quality from survey methodology, ResponseRate and SamplingError. It also allows for the description of other quality measures in OtherAppraisalProcess. Note that ProcessingEvent also contains a QualityStatementReference. This should be used to relay information on process quality. DataAppraisalInformation is used primarily to capture the results of data appraisal measures.

The response rate can be repeated to express differing response rates by mode of deliver, location, etc. The individual response rates may be expressed as a total sample size with number of responses and/or as a specific response rate. The description should be used to differentiate when multiple response rates are provided. SamplingError (StructuredStringType) is intended to contain a discussion of the sampling error. It may be structured to differentiate between the statement of the error itself, how it was calculated, etc. OtherAppraisalProcess allows for the description of other measures of data appraisal as needed.


Questions
----------

As the complexity of question structures increase, three general question structures have been identified within DDI and are addressed by the following structures: QuestionItem, QuestionGrid, and QuestionBlock. Note that all three structures reflect the reusable structure of various question types and do not relay any information on the applied use of the question within an instrument. The applied information, including question order, is captured by the ControlConstruct structures used by the Instrument. 

All question structures are maintained within a QuestionScheme and can be further organized for administrative purposes by QuestionGroup (a standard grouping structure available in most schemes). Only QuestionItem, QuestionGrid, and QuestionBlock may be referenced by a QuestionConstruct. 

A Sequence (type of ControlConstruct) is used to order questions within an instrument and is maintained separately as a reusable object. All question structures are versionable and contain a name for the question. All response domains may be described inline while a set of commonly used structures may be captured as managed representations and be reused by reference. These include Missing Values, Text, Numeric, DateTime, and Scale **(see Section 4.51** for details on all value representations and response domains).

QuestionItem
.............

A QuestionItem is a basic question containing a QuestionIntent, the concept being measured by the question, text for the question, response domain information, clarifying instructions, external aids (clarifying objects used in presenting the question to the respondent), Input and Output Parameters and Bindings, allowed response cardinality and an estimation of the time required to respond. The QuestionText is a DynamicTextString. Note that due to the variation of content in the QuestionText that is required to illicit equivalent responses in different languages, QuestionText is repeatable. A StructuredMixedResponseDomain supports situations where a response may include more than one type of response domain. This could be the inclusion of a set of Missing Values (responses that capture non-response and other values to be treated as invalid during analysis), or the commonly used addition of a text response to capture specific information when the code or category response is “Other”. StructuredMixedResponse allows for the addition of text and/or another response domain to be attached to one or more values of the primary response domain as well as stacking combinations of response options with intervening text.

QuestionGrid
...............

A QuestionGrid provides a multidimensional structure used to capture a complex response. In many cases these are simple structures, for example a question regarding an assessment of each of a list of candidates for political office. However, some grids are complex and capture different responses for each of a list of items. In addition, the list may be provided by the question or by the respondent (indicated by the use of a “roster” of blank text items). A QuestionGrid contains the basic elements of the QuestionItem but rather than a ResponseDomain or StructuredMixedResponseDomain contains a GridDimension that sorts one or more ResponseDomains or StructuredMixedGridResponseDomains into a specific dimension of the grid. The structure is similar to the NCube dimensional structure using code domain or roster rather than variables to structure the dimension, and then providing a response domain for each cell in the grid. A single ResponseDomain indicates that this is the response domain for each cell in the grid. Note that an internal cell label may be added to any cell for clarification purposes.

QuestionBlock 
..............

A QuestionBlock is intended to bundle together a set of questions (items and/or grids) that have meaning only in relation to a specified object expressed as the stimulus material. This form of question set is common in educational testing where a text, image, or other material is provided and the respondent is asked questions specific to the material. For example, a portion of a play script is provided and the respondent is asked question concerning the dialog and/or stage directions provided in the script. Note that the intent of QuestionBlock is NOT to bundle together a set of questions that are commonly used together or used in a specified order. 

A Sequence (type of control construct) is the appropriate way to manage this type of set relationship. It is assumed that one or more StimulusMaterial objects will be used. The 0..n cardinality of the CHOICE of StimulusMaterial, QuestionItemReference, and QuestionGridReference is provided simply to support the use of DDI during the development process when this piece of information may be unavailable. StimulusMaterial is part of this choice to allow for its insertion at any location before, after, or in the midst of the referenced Questions.

QuestionBlock contains the standard elements of QuestionItem and QuestionGrid and then structures any combination of StimulusMaterial with referenced QuestionItems and QuestionGrids. It allows for an indication of QuestionSequence (i.e., a means of declaring the sequence is important or that it can be randomized or otherwise altered).
