QualityStatement
==================
        
.. code-block:: XML    
        
  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    
    Example - Quality declarations in Collection Event, Physical Instance, Archive Specific, Quality Statement Scheme, and Data Appraisal
    
  -->
    
    <g:ResourcePackage   xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN>urn:ddi:us.archive:QualResource_1:1</r:URN>
    
    <!-- Data Collection/ Collection Event/ Quality Statement Reference -->
      
      <d:DataCollection isMaintainable="true" scopeOfUniqueness="Maintainable">
        <r:URN>urn:ddi:us.archive:DataColl_1:1</r:URN>
        <d:CollectionEvent isIdentifiable="true" scopeOfUniqueness="Maintainable">
          <r:URN>urn:ddi:us.archive:DataColl_1.CE_1:1</r:URN>
          <r:QualityStatementReference isReference="true" isExternal="true" lateBound="false">
            <r:URN>urn:ddi:us.archive:QScheme_1.QS_2:1</r:URN>
            <r:TypeOfObject>QualityStatement</r:TypeOfObject>
          </r:QualityStatementReference>
        </d:CollectionEvent>
      </d:DataCollection>
    
    <!-- Physical Instance/ Quality Statement Reference -->
        
      <pi:PhysicalInstance isMaintainable="true" scopeOfUniqueness="Maintainable">
        <r:URN>urn:ddi:us.archive:PhysInst_1:1</r:URN>
        <r:QualityStatementReference isReference="true" isExternal="true" lateBound="false">
          <r:URN>urn:ddi:us.archive:QScheme_1.QS_3:1</r:URN>
          <r:TypeOfObject>QualityStatement</r:TypeOfObject>
        </r:QualityStatementReference>
      </pi:PhysicalInstance>
    
    <!-- Archive/ ArchiveSpecific/ Quality Statement Reference -->
      
      <a:Archive isMaintainable="true" scopeOfUniqueness="Maintainable">
        <r:URN>urn:ddi:us.archive:Archive_1:1</r:URN>
        <a:ArchiveSpecific>
          <r:QualityStatementReference isReference="true" isExternal="true" lateBound="false">
            <r:URN>urn:ddi:us.archive:QScheme_1.QS_1:1</r:URN>
            <r:TypeOfObject>QualityStatement</r:TypeOfObject>
          </r:QualityStatementReference>
        </a:ArchiveSpecific>
      </a:Archive>
      
    <!-- Quality Statement Scheme -->
    
      <r:QualityScheme isMaintainable="true" scopeOfUniqueness="Maintainable">
        <r:URN>urn:ddi:us.archive:QScheme_1:1</r:URN>
        <r:QualityStatement isVersionable="true" scopeOfUniqueness="Maintainable">
          <r:URN>urn:ddi:us.archive:QScheme_1.QS_1:1</r:URN>
          <r:QualityStandard isVersionable="true" scopeOfUniqueness="Maintainable">
            <r:URN>urn:ddi:us.archive:QScheme_1.QSTD_1:1</r:URN>
            <r:StandardUsed>
              <r:OtherMaterial isVersionable="true" scopeOfUniqueness="Maintainable">
                <r:URN>urn:ddi:us.archive:QScheme_1.Standard_a:1</r:URN>
                <r:TypeOfMaterial>Standard</r:TypeOfMaterial>
                <r:Citation>
                  <r:Title><r:String>Reference Model for an Open Archival Information System (OAIS): Recommended Practice CCSDS 650.0-M-2</r:String></r:Title>
                </r:Citation>
                <r:ExternalURNReference> http://public.ccsds.org/publications/archive/650x0m2.pdf</r:ExternalURNReference>
              </r:OtherMaterial>
            </r:StandardUsed>
          </r:QualityStandard>
          <r:ComplianceStatement><r:Content>The archive complies with the OAIS model regarding the tracking of information from SIP through data processing and archival management to the creation of the AIP and assembly of the DIP.</r:Content></r:ComplianceStatement>
        </r:QualityStatement>
        <r:QualityStatement isVersionable="true" scopeOfUniqueness="Maintainable">
          <r:URN>urn:ddi:us.archive:QScheme_1.QS_2:1</r:URN>
          <r:QualityStandard isVersionable="true" scopeOfUniqueness="Maintainable">
            <r:URN>urn:ddi:us.archive:QScheme_1.QSTD_2:1</r:URN>
            <r:StandardUsed>
              <r:OtherMaterial isVersionable="true" scopeOfUniqueness="Maintainable">
                <r:URN>urn:ddi:us.archive:QScheme_1.Standard_b:1</r:URN>
                <r:TypeOfMaterial>Policy</r:TypeOfMaterial>
                <r:Citation>
                  <r:Title><r:String>Univerity Of Minnesota Board Of Regents Policy: Reserch Involving Human Subjects</r:String></r:Title>
                </r:Citation>
                <r:ExternalURNReference>http://www1.umn.edu/regents/policies/academic/HumanSubjects.pdf</r:ExternalURNReference>
                </r:OtherMaterial>
            </r:StandardUsed>
          </r:QualityStandard>
          <r:ComplianceStatement><r:Content>Policy strictly complied to.</r:Content></r:ComplianceStatement>
        </r:QualityStatement>
        <r:QualityStatement isVersionable="true" scopeOfUniqueness="Maintainable">
          <r:URN>urn:ddi:us.archive:QScheme_1.QS_3:1</r:URN>
          <r:OtherStatementOfQuality>
            <r:Content>As data is ported from one format to another, the following checks are made to verify the accurate transfer of the data items. Record Count and frequency count on all data items at the category level. A random sample of records is pulled from each file for item by item comparison. </r:Content>
          </r:OtherStatementOfQuality>
        </r:QualityStatement>
      </r:QualityScheme>
      
    <!-- Processing Event Scheme/ Processing Event/ Data Appraisal -->
      
      <d:ProcessingEventScheme isMaintainable="true" scopeOfUniqueness="Maintainable">
        <r:URN>urn:ddi:us.archive:ProcEventSch_1:1</r:URN> 
        <d:ProcessingEvent isVersionable="true" scopeOfUniqueness="Maintainable">
          <r:URN>urn:ddi:us.archive:ProcEventSch_1.PE_1:1</r:URN> 
          <d:DataAppraisalInformation>
            <d:ResponseRate>  
              <d:SampleSize>5000</d:SampleSize>
              <d:NumberOfResponses>3768</d:NumberOfResponses>
              <d:SpecificResponseRate>.7536</d:SpecificResponseRate>
            </d:ResponseRate>
            <d:SamplingError><r:Content><xhtml:div><xhtml:b>Calculation of Standard Errors <xhtml:br/>Totals and percentages. </xhtml:b> Tables A through C in this chapter contain the necessary information for calculating the standard errors of sample estimates in this data product. To calculate the standard error, it is necessary to know:<xhtml:ul><xhtml:li>The unadjusted standard error for the characteristic (given in Table A for estimated totals or Table B for estimated percentages) that would result under a simple random sample design of people, housing units, households, or families.</xhtml:li><xhtml:li>The design factor for the particular characteristic estimated (given in Table C) based on the sample design and estimation techniques employed to produce long form data estimates. </xhtml:li><xhtml:li>The number of people, housing units, households, or families in the publication area. </xhtml:li><xhtml:li>The observed sampling rate.</xhtml:li></xhtml:ul>The design factor is the ratio of the estimated standard error to the standard error of a simple random sample. The design factors reflect the effects of the actual sample design and the complex ratio estimation procedure used for Census 2000.</xhtml:div></r:Content></d:SamplingError>
          </d:DataAppraisalInformation>
        </d:ProcessingEvent>  
      </d:ProcessingEventScheme>
    </g:ResourcePackage>
