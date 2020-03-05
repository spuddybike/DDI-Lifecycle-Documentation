Dates
======

.. code-block:: XML

  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    Example - Dates: Simple, complete date range, range with unknown start, range with unknown end
  -->

  <r:TemporalCoverage xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3"     
    xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" 
    xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" 
    xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" 
    xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd"> 
    <r:URN>urn:ddi:us.mpc:TempCov:1</r:URN>
	
  <!-- SimpleDate -->

    <r:ReferenceDate>
      <r:SimpleDate>2013-02-26</r:SimpleDate>
      <r:HistoricalDate>
        <r:NonISODate>26 February 2013</r:NonISODate>
        <r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
        <r:Calendar>Gregorian</r:Calendar>
      </r:HistoricalDate>
    </r:ReferenceDate>

  <!-- Complete Date Range -->

    <r:ReferenceDate>
      <r:StartDate>2010-06-05T20:20:00</r:StartDate>
      <r:HistoricalStartDate>
        <r:NonISODate>24 Sivan 2770</r:NonISODate>
        <r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
        <r:Calendar>Jewish</r:Calendar>
      </r:HistoricalStartDate>
      <r:EndDate>2010-08-05T20:20:00</r:EndDate>
      <r:HistoricalEndDate>
        <r:NonISODate>28 Sivan 5770</r:NonISODate>
        <r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
        <r:Calendar>Jewish</r:Calendar>
      </r:HistoricalEndDate>
    </r:ReferenceDate>

  <!-- Range with unknown start date -->

    <r:ReferenceDate>
      <r:EndDate>2013-02-26</r:EndDate>
      <r:HistoricalEndDate>
        <r:NonISODate>February 26, 2013</r:NonISODate>
        <r:HistoricalDateFormat>Month dd, yyyy</r:HistoricalDateFormat>
        <r:Calendar>Gregorian</r:Calendar>
      </r:HistoricalEndDate>
    </r:ReferenceDate>

  <!-- Range with unknown end date -->

    <r:ReferenceDate>
      <r:StartDate>2013-02-26</r:StartDate>
      <r:HistoricalStartDate>
        <r:NonISODate>26 February 2013</r:NonISODate>
        <r:HistoricalDateFormat>dd Month yyyy</r:HistoricalDateFormat>
        <r:Calendar>Gregorian</r:Calendar>
      </r:HistoricalStartDate>
    </r:ReferenceDate>
	
  </r:TemporalCoverage>


