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




