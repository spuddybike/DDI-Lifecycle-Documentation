Examples
^^^^^^^^^^^^

Note that by including the information for the MaintainableObject in an
Identifiable or Versionable the user has provided sufficient information
to build either a Canonical or Deprecated URN scoped to either the
agency or the maintainable. While the information may not be part of the
URN as expressed by the maintaining agency, the information contained in
the MaintainableObject provides contextual information that may be
important to the user and may need to be passed to them for purposes
other than strict identification. The inclusion of Versioning
information in Versionable and Maintainable may be used internally to
track quality control and processing activities and may also be valuable
to the user in determining whether the change caused by versioning will
affect their analysis work.

Identifiable
^^^^^^^^^^^^

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
^^^^^^^^^^^^
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
^^^^^^^^^^^^
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

Reference
^^^^^^^^^
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
^^^^^^^^^^^^^^^

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
