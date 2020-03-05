Note
======

.. code-block:: XML

  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    Example - Note Types
  -->

    <g:ResourcePackage  xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN>urn:ddi:us.mpc:resourceNotes:1</r:URN>

      <!-- Example 1: Production Process-->

      <r:Note xml:lang="en">
  	    <r:TypeOfNote>Verification</r:TypeOfNote>
  	    <r:NoteSubject>Translation.English</r:NoteSubject>
  	    <r:Relationship>
  		    <r:RelatedToReference isReference="true" isExternal="false" lateBound="false">
  			    <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MS1295:1</r:URN>
	  		    <r:TypeOfObject>Variable</r:TypeOfObject>
		      </r:RelatedToReference>
		      <r:RelationshipDescription><r:Content xml:lang="en">VariableName verification</r:Content></r:RelationshipDescription>
	      </r:Relationship>
      
	      <r:Relationship>
		      <r:RelatedToReference isReference="true" isExternal="false" lateBound="false">
			      <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MS1295:1</r:URN>
			      <r:TypeOfObject>Variable</r:TypeOfObject>
		      </r:RelatedToReference>
		      <r:RelationshipDescription><r:Content xml:lang="en">VariableName verification</r:Content></r:RelationshipDescription>
	      </r:Relationship>
	      <r:Header><r:String xml:lang="en">Translation Question</r:String></r:Header>
	      <r:NoteContent><r:Content xml:lang="en">The source of this translation was XXX rather than the standard source. The content of the English translation string should be verified prior to publication.</r:Content></r:NoteContent>
      </r:Note>	

  <!-- Example 2: Work-around-->

      <r:Note xml:lang="en">
	      <r:TypeOfNote>WorkAround</r:TypeOfNote>
	      <r:NoteSubject>RecordRelationship</r:NoteSubject>
	      <r:Relationship>
		      <r:RelatedToReference isReference="true" isExternal="false" lateBound="false">
			      <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:XB9376:1</r:URN>
			      <r:TypeOfObject>RecordRelationship</r:TypeOfObject>
		      </r:RelatedToReference>
		      <r:RelationshipDescription><r:Content xml:lang="en">Target Source Clarification</r:Content></r:RelationshipDescription>
	      </r:Relationship>
	      <r:NoteContent><r:Content xml:lang="en"><xhtml:dl><xhtml:dt>SourceRecordURN</xhtml:dt><xhtml:dd>urn:ddi:us.mpc:LR_1:1</xhtml:dd><xhtml:dt>SourceRecordLinkURN</xhtml:dt><xhtml:dd>urn:ddi:us.mpc:Var_1:1</xhtml:dd><xhtml:dt>TargetRecordURN</xhtml:dt><xhtml:dd>urn:ddi:us.mpc:LR_2:1</xhtml:dd><xhtml:dt>TargetRecordLink</xhtml:dt><xhtml:dd>urn:ddi:us.mpc:Var_2:1</xhtml:dd></xhtml:dl></r:Content></r:NoteContent>
      </r:Note>	

  <!-- Example 3: Proprietary-->

      <r:Note>
	      <r:Relationship>
		      <r:RelatedToReference>
			      <r:Agency>int.example</r:Agency>
			      <r:ID>Concept1</r:ID>
			      <r:Version>1</r:Version>
			      <r:TypeOfObject>Concept</r:TypeOfObject>
		      </r:RelatedToReference>
	      </r:Relationship>
	      <r:ProprietaryInfo>
		      <r:ProprietaryProperty>
		      	<r:AttributeKey>CustomProperty1</r:AttributeKey>
			      <r:AttributeValue>Custom value 1</r:AttributeValue>
		      </r:ProprietaryProperty>
		    <r:ProprietaryProperty>
			    <r:AttributeKey>CustomProperty2</r:AttributeKey>
			    <r:AttributeValue>Custom value 2</r:AttributeValue>
		    </r:ProprietaryProperty>
	    </r:ProprietaryInfo>
    </r:Note>
  </g:ResourcePackage>
  
