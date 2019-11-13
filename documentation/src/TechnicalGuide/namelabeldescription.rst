Name, Label, and Description
-------------------------------

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
~~~~

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
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

 ------------------------------------------------------------
 Namespace: r
 Parent Maintainable: varies by usage
 Type: InternationalStringType
 ------------------------------------------------------------

 NameType
 String                                  (0..n)
   @xml:lang                             (optional)
   @isTranslated                         (default=”false”)
   @isTranslatable                       (default=”true”)
   @translationSourceLangauge            (optional)
   @translationDate                      (optional)
   @isPreferred                          (optional)
   @context                              (optional)

Label
~~~~~

A Label is intended to provide content for use in a display (a table
layout, printed content, web site, etc.). In all locations where Label
is used it may be repeated to reflect different types of label (i.e. a
short label, or a full label, etc.). The Label uses an extension base of
StructuredStringType which managed both multilingual content and allows
for the use of a set of xhtml structure tags (see pt2:2.5.1).
Differences in the intended use of each Label are expressed by the
element TypeOfLabel and a set of attributes that apply to all language
versions of the Label. The TypeOfLabel uses the extension base
CodeValueType which supports the use of an external controlled
vocabulary (see pt2:2.5.1). The attribute locationVariant is an
xs:string to allow for either a common geographic specification such as
a country code or a descriptive term (i.e. urban, northwest region,
etc.). For Labels with a limited period of use the pair of attributes
validForStartDate and validForEndDate allow clear specification for when
a Label is valid. Finally the attribute maxLength is useful for
identifying labels that must meet a specific length limitation, for
example in publishing content within a specific format or software
system.


`Label <http://www.ddialliance.org/Specification/DDI-Lifecycle/3.2/XMLSchema/FieldLevelDocumentation/schemas/reusable_xsd/elements/Label.html>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

 ------------------------------------------------------------
 Namespace: r
 Parent Maintainable: varies by usage
 Type: StructuredStringType
 ------------------------------------------------------------

 Label
   Content                               (0..n)
     xhtml:BlkNoForm.mix                 (0..n)
     @xml:lang                           (optional)
     @isTranslated                       (default=”false”)
     @isTranslatable                     (default=”true”)
     @translationSourceLangauge          (optional)
     @translationDate                    (optional)
   TypeOfLabel                           (0..n)
   @locationVariant                      (optional)
   @validForStartDate                    (optional)
   @validForEndDate                      (optional)
   @maxLength                            (optional)

Description
~~~~~~~~~~~

Description is of type StructuredStringType with no additional
extensions. It generally appears with a cardinality of 0..1. If it is
important to differentiate be original and added content it is possible
to do this by using the content structure features of the
StructuredString (see pt2:2.5.1). Note that if the object containing the
Name, Label, Description sequence may be used in a comparison process,
providing content for Description is critical as comparison is based
upon the comparison of the Description of the object, not its Name or
Label.

`Description <http://www.ddialliance.org/Specification/DDI-Lifecycle/3.2/XMLSchema/FieldLevelDocumentation/schemas/reusable_xsd/elements/Description.html>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

 ------------------------------------------------------------
 Namespace: r
 Parent Maintainable: varies by usage
 Type: StructuredStringType
 ------------------------------------------------------------

 Description
   Content                               (0..n)
    xhtml:BlkNoForm.mix                  (0..n)
    @xml:lang                            (optional)
    @isTranslated                        (default=”false”)
    @isTranslatable                      (default=”true”)
    @translationSourceLangauge           (optional)
    @translationDate                     (optional)

