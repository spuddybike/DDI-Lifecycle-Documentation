Sampling  
=========
        
.. code-block:: XML

  <?xml version="1.0" encoding="UTF-8"?>
  <!--
      
    Example - Sampling
    
  -->
    
    <g:ResourcePackage xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN>urn:ddi:us.mpc:RP_Sample:1</r:URN>
      <d:DataCollection isMaintainable="true" scopeOfUniqueness="Agency">
        <r:URN>urn:ddi:us.mpc:DColl:1</r:URN>
        <d:Methodology isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:Meth_2:1</r:URN>
          <d:SamplingProcedure isIdentifiable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:SampProc_1:1</r:URN>
            <d:TypeOfSamplingProcedure>Probability</d:TypeOfSamplingProcedure>
            <r:Description><r:Content><xhtml:p>The CPS sample is a probability sample designed primarily to produce national and state estimates of labor force characteristics of the civilian non-institutional population 16 years of age and older. The sample consists of independent samples in each state and the District of Columbia, and each state sample is specifically tailored to the demographic and labor market conditions that prevail in that particular state.</xhtml:p><xhtml:p>About 60,000 housing units are required in order to meet the national and State reliability criteria, drawn from 824 sample areas. Sample sizes are determined by reliability requirements that are expressed in terms of the coefficient of variation or CV. The coefficient of variation is a relative measure of the sampling error and is calculated as sampling error divided by the expected value of the given characteristic. Sufficient sample is allocated to maintain, at most, a 1.9-percent coefficient of variation on national monthly estimates of unemployment level, assuming a 6-percent unemployment rate. This translates into a change of 0.2 percentage point in the unemployment rate being significant at a 90-percent confidence level. For each of the 50 States and for the District of Columbia, the design maintains a coefficient of variation of at most 8 percent on the annual average estimate of unemployment level, assuming a 6-percent unemployment rate.</xhtml:p></r:Content></r:Description>
            <d:PopulationOfConcern>
              <r:Description><r:Content>Housing units</r:Content></r:Description>
              <r:UniverseReference>
                <r:URN>urn:ddi:us.mpc:HousingUnits:1</r:URN>
                <r:TypeOfObject>Universe</r:TypeOfObject>
              </r:UniverseReference>
            </d:PopulationOfConcern>
            <d:PopulationOfConcern>
              <r:Description><r:Content>Persons residing in housing units 15 years of age or over and not in the Armed Forces</r:Content></r:Description>
              <r:UniverseReference>
                <r:URN>urn:ddi:us.mpc:Persons_typeD:1</r:URN>
                <r:TypeOfObject>Universe</r:TypeOfObject>
              </r:UniverseReference>
            </d:PopulationOfConcern>  
            <d:OverallTargetSampleSize>
              <d:PrimaryPopulation numberOfUnits="60000">Housing Units</d:PrimaryPopulation>
            </d:OverallTargetSampleSize>
            <d:ApplicationDetails>
              <d:SampleFrameReference>
                <r:URN>urn:ddi:us.mpc:SF_1:1</r:URN>
                <r:TypeOfObject>SampleFrame</r:TypeOfObject>
              </d:SampleFrameReference>
              <d:TargetSampleSize>
                <d:StrataNumber>1</d:StrataNumber>
                <d:DesiredSampleSize numberOfUnits="60000">Housing Units</d:DesiredSampleSize>
              </d:TargetSampleSize>
              <d:DateOfSample><r:SimpleDate>2013-01-01</r:SimpleDate></d:DateOfSample>
              <d:ResponsibleForSamplingReference>
                <r:URN>urn:ddi:us.mpc:US_BLS:1</r:URN>
                <r:TypeOfObject>Organization</r:TypeOfObject>
              </d:ResponsibleForSamplingReference>
            </d:ApplicationDetails>
          </d:SamplingProcedure>
        </d:Methodology>
        <d:ProcessingInstructionScheme isMaintainable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:ProcInstrScheme:1</r:URN>
          <d:GenerationInstruction isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:ProcInstr_1:1</r:URN>
            <d:ExternalInformation>
              <r:OtherMaterial>
                <r:URN>urn:ddi:us.mpc:CPS_meth:1</r:URN>
                <r:ExternalURLReference>http://www.census.gov/prod/2006pubs/tp-66.pdf</r:ExternalURLReference>
              </r:OtherMaterial>
            </d:ExternalInformation>  
            <r:Description><r:Content>The overall state sampling interval is the inverse of the probability of selection of each housing unit in a state for a self-weighting design. By design, the overall state sampling interval is fixed, but the state sample size is not fixed, allowing growth of the CPS sample because of housing units built after Census 2000. (See Appendix B for details on how the desired sample size is maintained.)</r:Content></r:Description>
          </d:GenerationInstruction>
        </d:ProcessingInstructionScheme>
        <d:SampleFrameScheme isMaintainable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:SamFrameScheme:1</r:URN>
          <d:SampleFrame>
            <r:URN>urn:ddi:us.mpc:SF_1:1</r:URN>
            <d:SampleFrameName><r:String>2000 Decennial Census of Population and Housing and the Building Permit Survey</r:String></d:SampleFrameName>
            <r:Description><r:Content>Census 2000 collected information on all living quarters existing as of April 1, 2000, including characteristics of living quarters as well as the demographic composition of people residing in these living quarters. However, since the census does not cover housing units constructed since April 1, 2000, a sample of building permits issued in 2000 and later is used to supplement the census data. These data are collected via the Building Permit Survey, which is an ongoing survey conducted by the Census Bureau.</r:Content></r:Description>
            <d:ValidPeriod>
              <r:StartDate>2000-04-01</r:StartDate>
              <r:EndDate>2010-03-31</r:EndDate>
            </d:ValidPeriod>
            <d:CustodianReference>
              <r:URN>urn:ddi:us.mpc:USCB:1</r:URN>
              <r:TypeOfObject>Organization</r:TypeOfObject>
            </d:CustodianReference>
            <r:UniverseReference>
              <r:URN>urn:ddi:us.mpc:UnitedStates:1</r:URN>
              <r:TypeOfObject>Universe</r:TypeOfObject>
            </r:UniverseReference>
            <d:UnitsOfFrame>
              <d:PrimaryPopulation numberOfUnits="131704730">Housing Units</d:PrimaryPopulation>
              <d:SecondaryPopulation numberOfUnits="532488">Group Quarters</d:SecondaryPopulation>
              <d:SecondaryPopulation numberOfUnits="390217">Area</d:SecondaryPopulation>
              <d:SecondaryPopulation numberOfUnits="2891048">Permit</d:SecondaryPopulation>
            </d:UnitsOfFrame>
            <d:FrameLimitations><r:Content>Where city-type street addresses from Census 2000 do not exist, or where residential construction does not need or require building permits, area samples are sometimes necessary.</r:Content></d:FrameLimitations>
            <d:AuxiliaryInformation><r:Content>CPS sample selection is coordinated with the following demographic surveys in the 2000 redesign: the American Housing Survey—Metropolitan sample, the American Housing Survey—National sample, the Consumer Expenditure Survey— Diary sample, the Consumer Expenditure Survey—Quarterly sample, the Current Point of Purchase Survey, the National Crime Victimization Survey, the National Health Interview Survey, the Rent and Property Tax Survey, and the Survey of Income and Program Participation.</r:Content></d:AuxiliaryInformation>
          </d:SampleFrame>
        </d:SampleFrameScheme>
        <d:SamplingPlanScheme isMaintainable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:SamPlanScheme:1</r:URN>
        </d:SamplingPlanScheme>
      </d:DataCollection>
    </g:ResourcePackage>
