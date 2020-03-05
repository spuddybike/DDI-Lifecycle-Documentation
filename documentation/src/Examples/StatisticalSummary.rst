Statistical Summary
====================

.. code-block:: XML
   
  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    Example - Statistical Summary  
  -->
  
    <pi:StatisticalSummary xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">          
      <pi:VariableStatistics isVersionable="true" scopeOfUniqueness="Agency">
      <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:VS_2:1</r:URN>          
        <r:VariableReference>
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:V1:1</r:URN>
          <r:TypeOfObject>Variable</r:TypeOfObject>
        </r:VariableReference>  
        <pi:TotalResponses>100</pi:TotalResponses>        
        <pi:StandardWeightReference>
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:SW:1</r:URN>
          <r:TypeOfObject>StandardWeight</r:TypeOfObject>
        </pi:StandardWeightReference>
        <pi:MissingValuesReference>
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MV_1:1</r:URN>
          <r:TypeOfObject>ManagedMissingValuesRepresentation</r:TypeOfObject>
        </pi:MissingValuesReference>
        <pi:SummaryStatistic>        
          <pi:TypeOfSummaryStatistic>wtCount</pi:TypeOfSummaryStatistic>      
          <pi:Statistic isWeighted="true" computationBase="validOnly">1000</pi:Statistic>      
        </pi:SummaryStatistic>        
        <pi:UnfilteredCategoryStatistics>        
          <pi:VariableCategory>      
            <pi:CategoryValue><r:Value>1</r:Value></pi:CategoryValue>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>wtCount</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">450</pi:Statistic>  
            </pi:CategoryStatistic>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>weightedPct</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">0.45</pi:Statistic>  
            </pi:CategoryStatistic>    
          </pi:VariableCategory>      
          <pi:VariableCategory>      
            <pi:CategoryValue><r:Value>2</r:Value></pi:CategoryValue>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>wtCount</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">550</pi:Statistic>  
            </pi:CategoryStatistic>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>weightedPct</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">0.55</pi:Statistic>  
            </pi:CategoryStatistic>    
          </pi:VariableCategory>      
        </pi:UnfilteredCategoryStatistics>        
        <pi:FilteredCategoryStatistics>        
          <pi:FilterVariableReference>
            <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:V2:1</r:URN>
            <r:TypeOfObject>Variable</r:TypeOfObject>
          </pi:FilterVariableReference>      
          <pi:FilterVariableCategory>      
            <pi:FilterCategoryValue><r:Value>a</r:Value></pi:FilterCategoryValue>    
            <pi:VariableCategory>    
              <pi:CategoryValue><r:Value>1</r:Value></pi:CategoryValue>  
              <pi:CategoryStatistic>  
              <pi:TypeOfCategoryStatistic>Count</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">20</pi:Statistic>
              </pi:CategoryStatistic>  
              <pi:CategoryStatistic>  
                <pi:TypeOfCategoryStatistic>colPct</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">0.4</pi:Statistic>
              </pi:CategoryStatistic>  
            </pi:VariableCategory>    
            <pi:VariableCategory>    
              <pi:CategoryValue><r:Value>2</r:Value></pi:CategoryValue>  
              <pi:CategoryStatistic>  
                <pi:TypeOfCategoryStatistic>Count</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">30</pi:Statistic>
              </pi:CategoryStatistic>  
              <pi:CategoryStatistic>  
                <pi:TypeOfCategoryStatistic>colPct</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">0.6</pi:Statistic>
              </pi:CategoryStatistic>  
            </pi:VariableCategory>    
          </pi:FilterVariableCategory>      
          <pi:FilterVariableCategory>      
            <pi:FilterCategoryValue><r:Value>b</r:Value></pi:FilterCategoryValue>    
            <pi:VariableCategory>    
              <pi:CategoryValue><r:Value>1</r:Value></pi:CategoryValue>  
              <pi:CategoryStatistic>  
                <pi:TypeOfCategoryStatistic>Count</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">25</pi:Statistic>
              </pi:CategoryStatistic>  
              <pi:CategoryStatistic>  
                <pi:TypeOfCategoryStatistic>colPct</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">0.5</pi:Statistic>
              </pi:CategoryStatistic>  
            </pi:VariableCategory>    
            <pi:VariableCategory>    
              <pi:CategoryValue><r:Value>2</r:Value></pi:CategoryValue>  
              <pi:CategoryStatistic>  
                <pi:TypeOfCategoryStatistic>Count</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">25</pi:Statistic>
              </pi:CategoryStatistic>  
              <pi:CategoryStatistic>  
                <pi:TypeOfCategoryStatistic>colPct</pi:TypeOfCategoryStatistic>
                <pi:Statistic isWeighted="true" computationBase="validOnly">0.5</pi:Statistic>
              </pi:CategoryStatistic>  
            </pi:VariableCategory>    
          </pi:FilterVariableCategory>      
        </pi:FilteredCategoryStatistics>        
      </pi:VariableStatistics>          
      <pi:VariableStatistics isVersionable="true" scopeOfUniqueness="Agency">
      <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:VS_2:1</r:URN>    
        <r:VariableReference>
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:V2:1</r:URN>
          <r:TypeOfObject>Variable</r:TypeOfObject>
        </r:VariableReference>        
        <pi:TotalResponses>100</pi:TotalResponses>        
        <pi:StandardWeightReference>
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:SW:1</r:URN>
          <r:TypeOfObject>StandardWeight</r:TypeOfObject>
        </pi:StandardWeightReference>
        <pi:MissingValuesReference>
          <r:URN typeOfIdentifier="Canonical">urn:ddi:us.mpc:MV_1:1</r:URN>
          <r:TypeOfObject>ManagedMissingValuesRepresentation</r:TypeOfObject>
        </pi:MissingValuesReference>
        <pi:SummaryStatistic>        
          <pi:TypeOfSummaryStatistic>wtCount</pi:TypeOfSummaryStatistic>      
          <pi:Statistic isWeighted="true" computationBase="validOnly">1000</pi:Statistic>      
        </pi:SummaryStatistic>        
        <pi:UnfilteredCategoryStatistics>        
          <pi:VariableCategory>      
            <pi:CategoryValue><r:Value>a</r:Value></pi:CategoryValue>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>wtCount</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">500</pi:Statistic>  
            </pi:CategoryStatistic>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>weightedPct</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">0.50</pi:Statistic>  
            </pi:CategoryStatistic>    
          </pi:VariableCategory>      
          <pi:VariableCategory>      
            <pi:CategoryValue><r:Value>b</r:Value></pi:CategoryValue>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>wtCount</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">500</pi:Statistic>  
            </pi:CategoryStatistic>    
            <pi:CategoryStatistic>    
              <pi:TypeOfCategoryStatistic>weightedPct</pi:TypeOfCategoryStatistic>  
              <pi:Statistic isWeighted="true" computationBase="validOnly">0.50</pi:Statistic>  
            </pi:CategoryStatistic>    
          </pi:VariableCategory>      
        </pi:UnfilteredCategoryStatistics>        
      </pi:VariableStatistics>          
    </pi:StatisticalSummary>            
    
    
    
