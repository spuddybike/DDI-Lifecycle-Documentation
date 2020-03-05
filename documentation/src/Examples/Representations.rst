Representations
==================
                
.. code-block:: XML    
                
  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    
    Example - Representations
    
  -->
  
    <g:ResourcePackage xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN>urn:ddi:us.mpc:RepresentationRP:1</r:URN>
      <d:QuestionScheme>
        <r:URN>urn:ddi:us.mpc:QuestionScheme:1</r:URN>
    
    
        <!-- Category Representation -->
    
        <d:QuestionItem>
          <r:URN>urn:ddi:us.mpc:QICatRep:1</r:URN>
          <d:CategoryDomain>
            <r:CategorySchemeReference isExternal="false" isReference="true" lateBound="false" lateBoundRestriction="0" objectLanguage="en-US">
              <r:URN type="URN" typeOfIdentifier="Canonical">urn:ddi:us.mpc:PRES2000:1.0</r:URN>
              <r:TypeOfObject>CategoryScheme</r:TypeOfObject>
              <r:Exclude isExternal="false" externalReferenceDefaultURI="URI" isReference="true" lateBound="false" lateBoundRestriction="0" objectLanguage="en-US" sourceContext="URI">
                <r:URN type="URN" typeOfIdentifier="Canonical">urn:ddi:us.mpc:PRES2000_1:1.0</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:Exclude>
              <r:Exclude isExternal="false" externalReferenceDefaultURI="URI" isReference="true" lateBound="false" lateBoundRestriction="0" objectLanguage="en-US" sourceContext="URI">
                <r:URN type="URN" typeOfIdentifier="Canonical">urn:ddi:us.mpc:PRES2000_2:1.0</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:Exclude>
            </r:CategorySchemeReference>
          </d:CategoryDomain>
        </d:QuestionItem>
    
        <!-- Distribution Representation expressed as a ResponseDomain -->
    
        <d:QuestionItem>
          <r:URN>urn:ddi:us.mpc:QIDistDel_1:1</r:URN>
          <d:DistributionDomain decimalPositions="1">
            <r:DistributionValue>100</r:DistributionValue>
          </d:DistributionDomain>
        </d:QuestionItem>
    
        <!-- Geographic Representation expressed as a ResponseDomain -->
    
        <d:QuestionItem>
          <r:URN>urn:ddi:us.mpc:QIGPS_1:1</r:URN>
          <d:GeographicDomain pointFormat="DecimalDegree" spatialPrimitive="Point">
            <r:Datum>NAD83</r:Datum>
            <r:CoordinateSystem>SPCS</r:CoordinateSystem>
            <r:CoordinateZone>2203</r:CoordinateZone>
            <r:CoordinateSource>GPS</r:CoordinateSource>
            <r:ErrorCorrection>WAAS</r:ErrorCorrection>
            <r:Offset>0</r:Offset>
            <r:GeoreferencedObject>Residential Front Door</r:GeoreferencedObject>
            <r:CoordinatePairs maxArray="2" arraySeparator="|"/>
            <r:AlternateOffset maxLength="15"/>
            <r:AlternateCoordinateSystem maxLength="25"/>
          </d:GeographicDomain>
        </d:QuestionItem>
    
        <!-- Location Representation expressed as a ResponseDomain -->
    
        <d:QuestionItem>
          <r:URN>urn:ddi:us.mpc:QILocDel_1:2</r:URN>
          <d:LocationDomain>
            <r:Object>Image</r:Object>
            <r:Action regExp="[Dd]">
              <r:RegionOfAction>
                <r:ImageArea>
                  <r:Shape>Rectangle</r:Shape>
                  <r:Coordinates>5,-5 5,-2 2,-2 2,-5</r:Coordinates>
                </r:ImageArea>
              </r:RegionOfAction>
              <r:Description>
                <r:Content xml:lang="en">Mark the letter D (upper or lower case accepted) in the upper left (3x3) section of the 10x10 gridded image.</r:Content>
              </r:Description>
            </r:Action>
          </d:LocationDomain>
        </d:QuestionItem>
    
        <!-- Ranking Representation expressed as a ResponseDomain -->
    
        <d:QuestionItem>
          <r:URN>urn:ddi:us.mpc:QIRankDel_1:1</r:URN>
          <d:RankingDomain>
            <r:RankingRange maximumRepetitionOfSingleValue="1">
              <r:RangeUnit>Integer</r:RangeUnit>
              <r:MinimumValue included="true">1</r:MinimumValue>
              <r:MaximumValue included="true">5</r:MaximumValue>
            </r:RankingRange>
          </d:RankingDomain>
        </d:QuestionItem>
    
        <!-- Nominal Representation expressed as a ResponseDomain -->
    
        <d:QuestionGrid>
          <r:URN>urn:ddi:us.mpc:QGNomDel_1:2</r:URN>
          <d:NominalDomain regExp="[Xx]"/>
        </d:QuestionGrid>
      </d:QuestionScheme>
    
      <l:VariableScheme>
        <r:URN>urn:ddi:us.mpc:VarScheme:1</r:URN>
    
        <!-- Geographic Location Code Representation US counties excepting Alaska and Hawaii-->
    
        <l:Variable>
          <r:URN>urn:ddi:us.mpc:VarGeoLoc:1</r:URN>
          <l:VariableRepresentation>
            <r:GeographicLocationCodeRepresentation>
              <r:RecommendedDataType>String</r:RecommendedDataType>
              <r:IncludedGeographicLocationCodes>
                <r:AuthorizedSourceReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:FIPS:1.0</r:URN>
                  <r:TypeOfObject>AuthorizedSource</r:TypeOfObject>
                </r:AuthorizedSourceReference>
                <r:GeographicLocationReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:CNTY:1.0</r:URN>
                  <r:TypeOfObject>GeographicLocation</r:TypeOfObject>
                </r:GeographicLocationReference>
                <r:ExcludedLocationValueReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:ALASKA_CNTY:1.0</r:URN>
                  <r:TypeOfObject>LocationValue</r:TypeOfObject>
                </r:ExcludedLocationValueReference>
                <r:ExcludedLocationValueReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:HAWAII_CNTY:1.0</r:URN>
                  <r:TypeOfObject>LocationValue</r:TypeOfObject>
                </r:ExcludedLocationValueReference>
              </r:IncludedGeographicLocationCodes>
            </r:GeographicLocationCodeRepresentation>
          </l:VariableRepresentation>
        </l:Variable>
    
        <!-- Geographic Structure Code Representation including US, Regions, and Divisions -->
    
        <l:Variable>
          <r:URN>urn:ddi:us.mpc:VarGeoStruc:1</r:URN>
          <l:VariableRepresentation>
            <r:GeographicStructureCodeRepresentation>
              <r:IncludedGeographicStructureCodes>
                <r:AuthorizedSourceReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:US_Census:1.0</r:URN>
                  <r:TypeOfObject>AuthorizedSource</r:TypeOfObject>
                </r:AuthorizedSourceReference>
                <r:GeographicStructureReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:US_1990:1.0</r:URN>
                  <r:TypeOfObject>GeographicStructure</r:TypeOfObject>
                </r:GeographicStructureReference>
                <r:ExcludedGeographicLevelReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:REGION:1.0</r:URN>
                  <r:TypeOfObject>GeographicLevel</r:TypeOfObject>
                </r:ExcludedGeographicLevelReference>
                <r:ExcludedGeographicLevelReference isReference="true" isExternal="true" lateBound="false">
                  <r:URN>urn:ddi:us.mpc:DIVISION:1.0</r:URN>
                  <r:TypeOfObject>GeographicLevel</r:TypeOfObject>
                </r:ExcludedGeographicLevelReference>
              </r:IncludedGeographicStructureCodes>
            </r:GeographicStructureCodeRepresentation>
          </l:VariableRepresentation>
        </l:Variable>
    
        <!-- Code Representation including Industrial Classifications (SIC) -->
    
        <l:Variable>
          <r:URN>urn:ddi:us.mpc:VarCode:1</r:URN>
          <l:VariableRepresentation>
            <r:CodeRepresentation classificationLevel="Nominal">
              <r:RecommendedDataType>String</r:RecommendedDataType>
              <r:CodeListReference isReference="true" isExternal="true" lateBound="false">
                <r:URN>urn:ddi:us.mpc:SIC:1.0</r:URN>
                <r:TypeOfObject>CodeList</r:TypeOfObject>
              </r:CodeListReference>
              <r:CodeSubsetInformation>
                <r:DataExistence>
                  <r:DiscreteCategory>true</r:DiscreteCategory>
                </r:DataExistence>
              </r:CodeSubsetInformation>
            </r:CodeRepresentation>
          </l:VariableRepresentation>
        </l:Variable>
      </l:VariableScheme>
    
      <r:ManagedRepresentationScheme>
        <r:URN>urn:ddi:us.mpc:mrs:1</r:URN>
    
        <!-- Date Time Representation -->
    
        <r:ManagedDateTimeRepresentation regExp="[0-9]{2}/[0-9]{4}">
          <r:URN>urn:ddi:us.mpc:DateTime:1</r:URN>
          <r:DateFieldFormat>MM/YYYY</r:DateFieldFormat>
          <r:DateTypeCode>gYearMonth</r:DateTypeCode>
        </r:ManagedDateTimeRepresentation>
    
        <!-- Numeric Representation -->
    
        <r:ManagedNumericRepresentation isVersionable="true" scopeOfUniqueness="Agency" scale="1" decimalPositions="0" interval="1">
          <r:URN>urn:ddi:us.mpc:NumRange_1_10:1</r:URN>
          <r:ManagedNumericRepresentationName>
            <r:String xml:lang="en">Range 1-10+</r:String>
          </r:ManagedNumericRepresentationName>
          <r:Label>
            <r:Content xml:lang="en">Number Range covering 1 through 10 plus</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">Defines the allowed content for a number range of 1 - 10 where 10 is topcoded to imply 10 or more</r:Content>
          </r:Description>
          <r:NumberRange>
            <r:Low isInclusive="true">1</r:Low>
            <r:High isInclusive="true">10</r:High>
            <r:TopCode>10</r:TopCode>
          </r:NumberRange>
          <r:NumericTypeCode>Integer</r:NumericTypeCode>
        </r:ManagedNumericRepresentation>
    
        <!-- Text Representation -->
    
        <r:ManagedTextRepresentation isVersionable="true" scopeOfUniqueness="Agency" minLength="5" maxLength="5" regExp="[0-9]{5}">
          <r:URN>urn:ddi:us.icpsr:TD_1:1</r:URN>
          <r:ManagedTextRepresentationName isPreferred="true">
            <r:String xml:lang="en">ZIPCode</r:String>
          </r:ManagedTextRepresentationName>
          <r:Label>
            <r:Content xml:lang="en">United States 5-digit ZIP Code</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">The  5-digit ZIP Code used by the United States Postal Service for mail delivery.</r:Content>
          </r:Description>
        </r:ManagedTextRepresentation>
    
        <!-- Scale Representation (1) -->
    
        <r:ManagedScaleRepresentation isVersionable="true" scopeOfUniqueness="Maintainable">
          <r:URN>urn:ddi:us.mpc:ScaleRepresenationScheme_1.ScaleRepresenation_1:1</r:URN>
          <r:ManagedScaleRepresentationName>
            <r:String xml:lang="en">Simple ScaleRepresenation</r:String>
          </r:ManagedScaleRepresentationName>
          <r:Label>
            <r:Content xml:lang="en">Simple ScaleRepresenation</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">Example 1</r:Content>
          </r:Description>
          <r:ScaleDimension>
            <r:NumberRange>
              <r:Low isInclusive="true">0</r:Low>
              <r:High isInclusive="true">10</r:High>
            </r:NumberRange>
            <r:Anchor value="0">
              <r:CategoryReference>
                <r:URN>urn:ddi:us.mpc:CatScheme_1.Never:1</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:CategoryReference>
            </r:Anchor>
            <r:Anchor value="10">
              <r:CategoryReference>
                <r:URN>urn:ddi:us.mpc:CatScheme_1.Continually:1</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:CategoryReference>
            </r:Anchor>
            <r:ValueIncrement increment="1" startValue="0" endValue="10"/>
          </r:ScaleDimension>
          <r:DisplayLayout>ScaleRepresenationLine</r:DisplayLayout>
        </r:ManagedScaleRepresentation>
    
        <!-- Scale Representation (2) -->
    
        <r:ManagedScaleRepresentation isVersionable="true">
          <r:URN>urn:ddi:us.mpc:ScaleRepresenation_2:1</r:URN>
          <r:ManagedScaleRepresentationName>
            <r:String xml:lang="en">Likert ScaleRepresenation</r:String>
          </r:ManagedScaleRepresentationName>
          <r:Label>
            <r:Content xml:lang="en">Likert Scale as Scale Represenation</r:Content>
          </r:Label>
          <r:Description><r:Content xml:lang="en">Example 2</r:Content></r:Description>
          <r:ScaleDimension>
            <r:NumberRange>
              <r:Low isInclusive="true">1</r:Low>
              <r:High isInclusive="true">5</r:High>
            </r:NumberRange>
            <r:Anchor value="1">
              <r:CategoryReference>
                <r:URN>urn:ddi:us.mpc:CatScheme_1.StronglyDisagree:1</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:CategoryReference>
            </r:Anchor>
            <r:Anchor value="2">
              <r:CategoryReference>
                <r:URN>urn:ddi:us.mpc:CatScheme_1.Disagree:1</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:CategoryReference>
            </r:Anchor>
            <r:Anchor value="3">
              <r:CategoryReference>
                <r:URN>urn:ddi:us.mpc:CatScheme_1.NeitherAgreeNorDisagree:1</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:CategoryReference>
            </r:Anchor>
            <r:Anchor value="4">
              <r:CategoryReference>
                <r:URN>urn:ddi:us.mpc:CatScheme_1.Agree:1</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:CategoryReference>
            </r:Anchor>
            <r:Anchor value="5">
              <r:CategoryReference>
                <r:URN>urn:ddi:us.mpc:CatScheme_1.StronglyAgree:1</r:URN>
                <r:TypeOfObject>Category</r:TypeOfObject>
              </r:CategoryReference>
            </r:Anchor>
            <r:MarkedIncrement increment="1" startValue="1" endValue="5"/>
            <r:ValueIncrement increment="1" startValue="1" endValue="5"/>
          </r:ScaleDimension>
          <r:DisplayLayout>ScaleLine</r:DisplayLayout>
        </r:ManagedScaleRepresentation>
    
        <!-- Scale Representation (3) -->
    
        <r:ManagedScaleRepresentation isVersionable="true">
          <r:URN>urn:ddi:us.mpc:ScaleRepresenation_3:1</r:URN>
          <r:ManagedScaleRepresentationName>
            <r:String xml:lang="en">Diamond</r:String>
          </r:ManagedScaleRepresentationName>
          <r:Label>
            <r:Content xml:lang="en">Dimond of Opposites</r:Content>
          </r:Label>
          <r:Description>
            <r:Content xml:lang="en">Describes an area within which response is collected against opposing Scale.</r:Content>
          </r:Description>
          <r:ScaleDimension>
            <r:Label>
              <r:Content xml:lang="en">Repulsion</r:Content>
            </r:Label>
            <r:NumberRange>
              <r:Low isInclusive="true">0</r:Low>
              <r:High isInclusive="true">10</r:High>
            </r:NumberRange>
            <r:MarkedIncrement increment="10" startValue="0" endValue="10"/>
            <r:ValueIncrement increment="10" startValue="0" endValue="10"/>
          </r:ScaleDimension>
          <r:ScaleDimension>
            <r:Label>
              <r:Content xml:lang="en">Attraction</r:Content>
            </r:Label>
            <r:NumberRange>
              <r:Low isInclusive="true">0</r:Low>
              <r:High isInclusive="true">10</r:High>
            </r:NumberRange>
            <r:MarkedIncrement increment="10" startValue="0" endValue="10"/>
            <r:ValueIncrement increment="10" startValue="0" endValue="10"/>
          </r:ScaleDimension>
          <r:DimensionIntersect>
            <r:IncludedDimension>1</r:IncludedDimension>
            <r:IncludedDimension>2</r:IncludedDimension>
          </r:DimensionIntersect>
          <r:DisplayLayout>Outline</r:DisplayLayout>
        </r:ManagedScaleRepresentation>
    
        <!-- Missing Values -->
    
        <r:ManagedMissingValuesRepresentation isVersionable="true" scopeOfUniqueness="Agency" versionDate="2012-10-16">
          <r:URN>urn:ddi:us.mpc:MVD1:1</r:URN>
          <r:ManagedMissingValuesRepresentationName isPreferred="true" context="ANES">
            <r:String xml:lang="en-US">ANES standard missing values</r:String>
          </r:ManagedMissingValuesRepresentationName>
          <r:MissingCodeRepresentation>
            <r:CodeListReference isReference="true">
              <r:URN>urn:ddi:us.mpc:CodeList_X:1</r:URN>
              <r:TypeOfObject>CodeList</r:TypeOfObject>
            </r:CodeListReference>
          </r:MissingCodeRepresentation>
          <r:MissingNumericRepresentation>
            <r:NumberRange>
              <r:Label>
                <r:Content>No Response</r:Content>
              </r:Label>
              <r:Low isInclusive="true">-1</r:Low>
              <r:High isInclusive="true">-1</r:High>
            </r:NumberRange>
          </r:MissingNumericRepresentation>
        </r:ManagedMissingValuesRepresentation>
      </r:ManagedRepresentationScheme>
    </g:ResourcePackage>
