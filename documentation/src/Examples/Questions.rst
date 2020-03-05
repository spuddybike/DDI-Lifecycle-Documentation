Questions
==================
            
.. code-block:: XML    
            
  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    
    Example - Question Scheme, Question Item, Question Grid, Question Block with related schemes
    
  -->

    <g:ResourcePackage isMaintainable="true"  versionDate="2012-09-18" scopeOfUniqueness="Maintainable" xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:ResourcePkg_QBlock:1</r:URN>
      <d:QuestionScheme scopeOfUniqueness="Maintainable" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS:1</r:URN>
        <d:QuestionSchemeName><r:String xml:lang="en-us">Questions for PISA</r:String></d:QuestionSchemeName>
              <r:Description><r:Content xml:lang="en-us"></r:Content></r:Description>
              <d:QuestionItem isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_1:1</r:URN>
          <d:QuestionText><d:LiteralText><d:Text>What is the extract from the play about? The duchess thinks of a trick</d:Text></d:LiteralText></d:QuestionText>
          <d:CodeDomain>
            <r:CodeListReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_1:1</r:URN>
              <r:TypeOfObject>CodeList</r:TypeOfObject>
            </r:CodeListReference>
          </d:CodeDomain>
              </d:QuestionItem>
              <d:QuestionItem isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_2:1</r:URN>
          <d:QuestionText><d:LiteralText><d:Text><xhtml:div><xhtml:p>A. In the script of the play, in addition to the words to be spoken by the actors, there are directions for the actors and theatre technicians to follow.</xhtml:p><xhtml:p>B. How can these directions be recognized in the script?</xhtml:p></xhtml:div></d:Text></d:LiteralText></d:QuestionText>
          <d:TextDomainReference isReference="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MgdRep.Text_1:1</r:URN>
            <r:TypeOfObject>ManagedTextRepresentation</r:TypeOfObject>
          </d:TextDomainReference>
              </d:QuestionItem>
              <d:QuestionItem isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_3:1</r:URN>
          <d:QuestionText><d:LiteralText><d:Text><xhtml:div><xhtml:p>The director positions the actors on the stage. On a diagram, the director represents Amanda with the letter A and the Duchess with the letter D.</xhtml:p><xhtml:p>Put an A and a D on the following diagram of the set to show approximately where Amanda and the Duchess are when the Prince arrives.</xhtml:p></xhtml:div></d:Text></d:LiteralText></d:QuestionText>
          <d:LocationDomain>
          <r:Object>Image</r:Object>
            <r:Action>
              <r:RegionOfAction>
                <r:ImageArea>
                  <r:Shape>Rectangle</r:Shape>
                  <r:Coordinates>[define the coordinate points of the response area]</r:Coordinates>
                </r:ImageArea>
              </r:RegionOfAction>
              <r:Description><r:Content xml:lang="en-us">Place the letter A within the defined Image Area</r:Content></r:Description>
            </r:Action>
            <r:Action>
              <r:RegionOfAction>
                <r:ImageArea>
                  <r:Shape>Rectangle</r:Shape>
                  <r:Coordinates>[define the coordinate points of the response area]</r:Coordinates>
                </r:ImageArea>
              </r:RegionOfAction>
              <r:Description><r:Content xml:lang="en-us">Place the letter D within the defined Image Area</r:Content></r:Description>
            </r:Action>
          </d:LocationDomain>
          <d:ExternalAid>
            <r:OtherMaterial isVersionable="true" scopeOfUniqueness="Maintainable">
                 <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.EXT_1:1</r:URN>
                 <r:TypeOfMaterial>Image</r:TypeOfMaterial>
                 <r:ExternalURNReference>stageimage.pdf</r:ExternalURNReference>
            </r:OtherMaterial>
          </d:ExternalAid>
              </d:QuestionItem>
              <d:QuestionItem isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_4:1</r:URN>
          <d:QuestionText><d:LiteralText><d:Text>Towards the end of the extract from the play, Amanda says, "He didn't recognise me...". What does she mean by that?</d:Text></d:LiteralText></d:QuestionText>
          <d:CodeDomain>
            <r:CodeListReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_3:1</r:URN>
              <r:TypeOfObject>CodeList</r:TypeOfObject>
            </r:CodeListReference>
          </d:CodeDomain>
              </d:QuestionItem>
              <d:QuestionGrid isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QG_1:1</r:URN>
          <d:QuestionText><d:LiteralText><d:Text>The table below lists theatre technicians involved in staging this extract from Locadia. Complete the table by indicating one stage direction from Text 1 which would require the involvement of each technician. The first one has been done for you.</d:Text></d:LiteralText></d:QuestionText>
          <d:GridDimension rank="1" displayCode="false" displayLabel="true">
            <d:CodeDomain>
              <r:CodeListReference>
                <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_2:1</r:URN>
                <r:TypeOfObject>CodeList</r:TypeOfObject>
              </r:CodeListReference>
            </d:CodeDomain>
          </d:GridDimension>
          <d:GridDimension rank="2">
            <d:Roster baseCodeValue="1" minimumRequired="1" maximumAllowed="1" codeIterationValue="1">
                    <r:Label><r:Content xml:lang="en-us">Stage direction</r:Content></r:Label>
            </d:Roster>
          </d:GridDimension>
          <d:StructuredMixedGridResponseDomain>
            <d:NoDataByDefinition>
            </d:NoDataByDefinition>
            <d:GridResponseDomainInMixed>
              <d:TextDomainReference isReference="true">
                <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MgdRep.Text_1:1</r:URN>
                <r:TypeOfObject>ManagedTextRepresentation</r:TypeOfObject>
              </d:TextDomainReference>
              <d:GridAttachment>
                <d:CellCoordinatesAsDefined>
                  <d:SelectDimension rank="1" rangeMinimum="2" rangeMaximum="4"/>
                  <d:SelectDimension rank="2" allValues="true"/>
                </d:CellCoordinatesAsDefined>
              </d:GridAttachment>
            </d:GridResponseDomainInMixed>
          </d:StructuredMixedGridResponseDomain>
          <d:CellLabel>
            <r:Content xml:lang="en-us">A circular bench around a small obelisk</r:Content>
            <d:GridAttachment>
              <d:SpecificCellCoordinate>1,1</d:SpecificCellCoordinate>
            </d:GridAttachment>
          </d:CellLabel>
              </d:QuestionGrid>
              <d:QuestionBlock isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QB_1:1</r:URN>
          <d:StimulusMaterial>
            <r:OtherMaterial isVersionable="true" scopeOfUniqueness="Maintainable">
                 <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.Eval_1:1</r:URN>
                 <r:TypeOfMaterial>Image</r:TypeOfMaterial>
                 <r:ExternalURNReference>ScriptText1.pdf</r:ExternalURNReference>
            </r:OtherMaterial>
          </d:StimulusMaterial>
          <d:StimulusMaterial>
            <r:OtherMaterial isVersionable="true" scopeOfUniqueness="Maintainable">
                 <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.Eval_2:1</r:URN>
                 <r:TypeOfMaterial>Image</r:TypeOfMaterial>
                 <r:ExternalURNReference>ScriptText2.pdf</r:ExternalURNReference>
            </r:OtherMaterial>
          </d:StimulusMaterial>
          <d:QuestionItemReference>  
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_1:1</r:URN>
            <r:TypeOfObject>QuestionItem</r:TypeOfObject>
          </d:QuestionItemReference>
          <d:QuestionItemReference>  
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_2:1</r:URN>
            <r:TypeOfObject>QuestionItem</r:TypeOfObject>
          </d:QuestionItemReference>
          <d:QuestionItemReference>  
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QG_1:1</r:URN>
            <r:TypeOfObject>QuestionItem</r:TypeOfObject>
          </d:QuestionItemReference>
          <d:QuestionItemReference>  
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_3:1</r:URN>
            <r:TypeOfObject>QuestionItem</r:TypeOfObject>
          </d:QuestionItemReference>
          <d:QuestionItemReference>  
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_QS.QI_4:1</r:URN>
            <r:TypeOfObject>QuestionItem</r:TypeOfObject>
          </d:QuestionItemReference>
              </d:QuestionBlock>            
      </d:QuestionScheme>
      <l:CategoryScheme scopeOfUniqueness="Maintainable" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1:1</r:URN>
        <l:CategorySchemeName><r:String xml:lang="en-us">Trick</r:String></l:CategorySchemeName>
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_1:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Attract Prince</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">to get the Prince to come and see her more often.</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_2:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Prince Decision</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">to get the Prince to make up his mind finally to get married</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_3:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Amanda Influence</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">to get Amanda to make the Prince forget his grief.</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_4:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Amanda move to castle</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">to get Amanda to come and live at the castle with her.</r:Content></r:Label>
        </l:Category>     
      </l:CategoryScheme>
      <l:CategoryScheme scopeOfUniqueness="Maintainable" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2:1</r:URN>
        <l:CategorySchemeName><r:String xml:lang="en-us">Theatre technicians</r:String></l:CategorySchemeName>
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_1:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Set designer</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">Set designer</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_2:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Props manager</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">Props manager</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_3:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Sound technician</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">Sound technician</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_4:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Lighting technician</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">Lighting technician</r:Content></r:Label>
        </l:Category>     
      </l:CategoryScheme>
      <l:CategoryScheme scopeOfUniqueness="Maintainable" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3:1</r:URN>
        <l:CategorySchemeName><r:String xml:lang="en-us">Amanda intent</r:String></l:CategorySchemeName>
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_1:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Didn't look</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">That the Prince didn't look at Amanda.</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_2:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Didn't recognize status</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">That the Prince didn't realise that Amanda was a shop assistant.</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_3:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Didn't recognize past meeting</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">That the Prince didn't realise that he'd already met Amanda.</r:Content></r:Label>
        </l:Category>     
        <l:Category isVersionable="true" scopeOfUniqueness="Maintainable">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_4:1</r:URN>
          <l:CategoryName><r:String xml:lang="en-us">Didn't see resemblance</r:String></l:CategoryName>
                <r:Label><r:Content xml:lang="en-us">That the Prince didn't notice that Amanda looked like Locadia.</r:Content></r:Label>
        </l:Category>     
      </l:CategoryScheme>
      <l:CodeListScheme scopeOfUniqueness="Maintainable" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CodeS_QBlock:1</r:URN>
        <l:CodeListSchemeName><r:String xml:lang="en-us">Code Lists for PISA</r:String></l:CodeListSchemeName>
        <l:CodeList scopeOfUniqueness="Maintainable" isMaintainable="true">
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_1:1</r:URN>
          <r:RecommendedDataType>Character</r:RecommendedDataType>
          <r:CategorySchemeReference>
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1:1</r:URN>
            <r:TypeOfObject>CategoryScheme</r:TypeOfObject>
          </r:CategorySchemeReference>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_1.C_1:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_1:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>A</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_1.C_2:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_2:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>B</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_1.C_3:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_3:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>C</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_1.C_4:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_1.Cat_4:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>D</r:Value>
          </l:Code>
        </l:CodeList>  
        <l:CodeList scopeOfUniqueness="Maintainable" isMaintainable="true">
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_2:1</r:URN>
                <r:Label><r:Content xml:lang="en-us">Theatre technicians</r:Content></r:Label>
          <r:RecommendedDataType>Integer</r:RecommendedDataType>
          <r:CategorySchemeReference>
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2:1</r:URN>
            <r:TypeOfObject>CategoryScheme</r:TypeOfObject>
          </r:CategorySchemeReference>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_2.C_1:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_1:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>1</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_2.C_2:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_2:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>2</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_2.C_3:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_3:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>3</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_2.C_4:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_2.Cat_4:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>4</r:Value>
          </l:Code>
        </l:CodeList>  
        <l:CodeList scopeOfUniqueness="Maintainable" isMaintainable="true">
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_3:1</r:URN>
          <r:RecommendedDataType>Character</r:RecommendedDataType>
          <r:CategorySchemeReference>
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3:1</r:URN>
            <r:TypeOfObject>CategoryScheme</r:TypeOfObject>
          </r:CategorySchemeReference>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_3.C_1:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_1:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>A</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_3.C_2:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_2:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>B</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_3.C_3:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_3:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>C</r:Value>
          </l:Code>
          <l:Code isDiscrete="true" scopeOfUniqueness="Maintainable" isIdentifiable="true">
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:PISA_CL_3.C_4:1</r:URN>
            <r:CategoryReference>
              <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:CS_PISA_3.Cat_4:1</r:URN>
              <r:TypeOfObject>Category</r:TypeOfObject>
            </r:CategoryReference>
            <r:Value>D</r:Value>
          </l:Code>
        </l:CodeList>  
      </l:CodeListScheme>
      <r:ManagedRepresentationScheme scopeOfUniqueness="Maintainable" isMaintainable="true">
        <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MgdRep:1</r:URN>
        <r:ManagedTextRepresentation isVersionable="true" scopeOfUniqueness="Maintainable" maxLength="250">
             <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MgdRep.Text_1:1</r:URN>
          <r:ManagedTextRepresentationName><r:String xml:lang="en-us">0 min to 250 max length response.</r:String></r:ManagedTextRepresentationName>
        </r:ManagedTextRepresentation>     
      </r:ManagedRepresentationScheme>
    </g:ResourcePackage>
    
