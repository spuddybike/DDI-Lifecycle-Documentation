Common Structures
*****************

There are a number of common structures used by many of the objects in DDI. These deal either with content like strings, dates, and controlled vocabularies, or with common complex structures like Citation, Coverage, Notes, and OtherMaterial. A basic understanding of these common structures allows you to focus on the content coverage and arrangement rather than the fine details.

Note that Identification and Reference structures are covered in **THE TECHNICAL GUIDE**. 

String, Controlled Vocabularies
--------------------------------

All DDI string content is based on an extension of xs:string and is designed to support the use of multiple language content for a given element where appropriate, structured text content, and for questionnaire
related materials, dynamic text. In addition, DDI supports the use of external controlled vocabularies through the structure CodeValue which identifies the source and location of the external controlled
vocabulary as well as the term content.

The basic structure is an xs:string which allows for any character in any sequence. 
Note that XML ignores leading and trailing white spaces as well as control characters like tabs and hard returns.  In short it will ignore internal structuring of content. 

DDI has created the following xs:string extensions to provide support for content structure and language specification where needed.
In some cases, such as the value of a code, leading and trailing spaces are important to both understanding and matching the content. 
Elements of *type="ValueType"* provide the attribute *xml:space* with which the user can declare that leading and trailing white spaces have implications for the meaning of the content. 

The default value of *xml:space* is "default". This states that the leading and  trailing spaces may be stripped off. 
By changing the value of *xml:space* to "preserve" the user specifies that leading and trailing spaces should be retained as they are critical to the understanding of the
content. 

All elements of *type="InternationalStringType"* support the use of one or more strings with equivalent language content **see technical Guide**. 

A common example of this occurs in all primary element names, i.e., VariableName. 
An InternationalStringType bundles together one or more language equivalents of the same content. 
This requires the use of a sub-element "String" which is repeated for each language provided. 
String contains attributes to designate the language of the content and basic translation information.

.. code-block:: XML

  <l:VariableName>
    <r:String xml:lang="en" isTranslated="false" isTranslatable="true">Household Relationship</r:String>
    <r:String xml:lang="fr" isTranslated="false" isTranslatable="true">Relation des ménages</r:String>
    <r:String xml:lang="es" isTranslated="true" isTranslatable="true" 
      translationSourceLanguage="en" translationDate="2012-12-03">Relación de Hogares</r:String>
  </l:VariableName>

What this example states is that the contents of the three strings are language equivalents for the VariableName content. The English and French are both original language content. The Spanish content is a translation of the English done on 2012-12-03. All the content may be translated. Bundling language equivalents together within a single object clarifies which language strings contain the same meaning when an object is repeatable.

All elements of a StructuredStringType use the sub-element "Content". Content supports the same language structures using the same attributes as an InternationalStringType. In addition Content may contain a limted set of XHTML structure tags to provide structure to the content. There is one addition attribute "isPlainText" has been added to clarify if the content is to be treated as plain text (no
formatting structure). The default value for this attribute is "true". If the content contains structure tags this attribute should be changed to "false". Label and Description are two commonly used elements of this type. 

A full list of allowed XHTML tags and their usage is found in the appendixes [Appendix B – XHTML Tags Supported by DDI]. The following example is a Description using an unordered (i.e., bulleted) list. Note that, like InternationalStringType the sub-element Content can be repeated for language equivalents.

.. code-block:: XML

  <r:Description>
    <r:Content xml:lang="en" isTranslated="false" isTranslatable="true"
      isPlainText=”false”>A single person may include any of the following: 
      <xhtml:list>
        <xhtml:item>Never married</xhtml:item>
        <xhtml:item>Widowed</xhtml:item>
        <xhtml:item>Divorced</xhtml:item>
      </xhtml:list>
    </r:Content>
  </r:Description>

It would be interpreted as:

A single person may include any of the following:
- Never married
- Widowed
- Divorced

Note that if isPlainText="true" the same line would be interpreted as: 

A single person may include any of the following:

.. code-block:: XML

<xhtml:list><xhtml:item>Nevermarried</xhtml:item>
<xhtml:item>Widowed</xhtml:item>
<xhtml:item>Divorced</xhtml:item></xhtml:list>

Dates
-------

The standard Date structure supports single dates and date ranges with a start date only, start and end
date, and end date only. Single date should only be used for events attached to a specific date, a point in
time rather than a period of time. This allows capturing dates as expressed in original do documents or to
capture more descriptive date information. The ISO 8601 allowed structures include:

+--------------------+-------------------------+-----------------------+ 
| xml property       | ISO Format              | Example               |
+--------------------+-------------------------+-----------------------+ 
| xs:dateTime        | yyyy-mm-ddThh:mm:ss     | 1982-01-05T23:05:15   |
|                    |                         |                       |
| xs:date            | yyyy-mm-dd              | 1982-01-05            |
|                    |                         |                       |
| xs:gYearMonth      | yyyy-mm                 | 1982-01               |
|                    |                         |                       |
| xs:gYear           | yyyy                    | 1982                  |
|                    |                         |                       |
| xs:duration        | PnnYnnMnnDTnnHnnMnn     | SP26Y02M22DT11H05M20S |
+--------------------+-------------------------+-----------------------+ 

Note that the "T" in dateTime is literal, denoting the beginning of the Time section, and that "ss" can
contain decimals. Optionally, dateTime can be extended by a time zone offset of "Z" to represent Zulu
time or GMT. For example, Eastern Standard Time is Z-4. 

Note that the "P" in duration is literal and indicates that this is a Period of duration. The other upper
case letters are also required with the preceding number providing the number of years (nY), months
(nM), etc. A period may be of negative duration, for example a period of minus 10 days (-P10D), by
preceding the "P" with a negative sign.

All dates must be expressed in the standard ISO 8601 format but may also be expressed as a HistoricalDate. This is simply a string containing the historical date and an attribute historicalDateFormat used to specify the non-ISO date format. For example:

.. code-block:: XML

  <r:HistoricalDate>
    <r:NonISODate>January 5, 1982</r:NonISODate>
    <r:HistoricalDateFormat>Month DD, YYYY</r:HistoricalDateFormat>
    <r:Calendar>Georgian</r:Calender>
  </r:HistoricalDate>

Historical date information parallels the simple date, start date and end date structures of the standard
DateType.

Citation and Coverage
----------------------

Citation in DDI is used by all publication structures, Phyiscal Instance, Other Material, and Collection or
Item descriptions. A citation in DDI reflects the content of a basic bibliographic citation. All citations
support the use of full Dublin Core Terms. The fields in the DDI citation support linking to Organizations
and Individuals described in an Organization Scheme where appropriate. Note that the citation in
Physical Instance is the citation for the related data file.

Coverage is represented in a separate section available in all maintainable modules. Coverage is separated into Temporal, Topical, and Spatial coverage. It is assumed that coverage expressed in a Study Unit or Group represents the extent of coverage of their contained modules. A module such as DataCollection may be expressed as a restriction of the parent Study Unit. For example, a Data
Collection for a specific time period within the full temporal coverage of the Study Unit, or a Physical Instance for a data set that covers only a single country within a multi-country study. 

Citation and Coverage are intended to contain information that is readily mapped to external search systems that support standard Dublin Core-like discovery metadata and should reflect the needs of these external systems. The use of shared or common subject headings or thesauri facilitate discovery in these systems.

Notes
-------

The element Note is available within all Maintainable objects. A Note allows the user to provide
information not covered by DDI. It is **not intended to replace formal local extensions of the schema**, but
to support capturing run-time extensions, content that is held in anticipation of a bug correction, or a
temporary work-around. The primary use of Note is to capture mid-process Notes or instructions which
may be removed later during the processing of the metadata.

A Note is captured once within a Maintainable object and then references the objects that it is related to. A Note can be attached by reference to any object with an ID. The intent of a Note is to be easily removable (removal of the Note also removes all reference links between the Note and the related objects). If a Note is related to objects outside of the Maintainable within which it exists, the Note should be duplicated in the Maintainable object which contains the other related objects. By placing the Note in the parent Maintainable, the user is assured of having all notes related to an object by checking in the parent Maintainable.

When a Note contains information that will be transferred to future elements or attributes (new content of a sub-minor version correction or the development of formal extensions) the use of the ProprietaryInfo (key/value pair) or well-structured content within the NoteContent field is recommended. Examples of different types of Notes are provided in **TECHNICAL GUIDE [Note]**.

OtherMaterial
--------------

OtherMaterial provides a generic means of identifying an external object such as a publication, video, image, etc. that can be described by a citation and/or identified by a URI. The identified material can be related to the maintainable as a whole or to a specific object by reference. It is good practice to include the OtherMaterial within the maintainable of the objects it is related to. In addition OtherMaterial is used as an extension base or type for specific pieces of information that are generally held externally
but need to be more tightly bound to a specific use. For example, an ExternalInterviewerInstruction extends OtherMaterial by adding display information. 

OtherMaterial can be very useful when creating very basic DDI documentation for a large collection. Materials that have not been transformed to DDI (Code lists, questionnaires, interviewer manuals, etc.) can be quickly described and linked to the basic record, retaining their link without full transformation to DDI. The internal content of the material is not as accessible as if it was in DDI but the relationship is not lost.



