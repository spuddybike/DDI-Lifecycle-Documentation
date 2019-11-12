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

::

<l:VariableName>
  <r:String xml:lang="en" isTranslated="false" isTranslatable="true">Household Relationship</r:String>
  <r:String xml:lang="fr" isTranslated="false" isTranslatable="true">Relation des ménages</r:String>
  <r:String xml:lang="es" isTranslated="true" isTranslatable="true" 
    translationSourceLanguage="en" translationDate="2012-12-03">Relación de Hogares</r:String>
</l:VariableName>

