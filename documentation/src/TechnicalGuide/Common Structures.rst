Commononly Used Structures
===========================

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



