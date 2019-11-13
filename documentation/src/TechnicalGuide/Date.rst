Date
---------

With the exception of describing the date format in a data capture system or as it is represented in a data file, DDI requires the use of the standard ISO 860 formats for all machine actionable dates. ISO 860 uses the Gregorian calendar so dates in other calendars must be translated. The basic form of a date in DDI is the BaseDateType which is a union of ISO dates types including:

+--------------------+-------------------------+-----------------------+ 
| xml property       | ISO Format              | Example               |
+====================+=========================+=======================+
| xs:dateTime        | yyyy-mm-ddThh:mm:ss     | 1982-01-05T23:05:15   |
+--------------------+-------------------------+-----------------------+ 
| xs:date            | yyyy-mm-dd              | 1982-01-05            |
+--------------------+-------------------------+-----------------------+ 
| xs:gYearMonth      | yyyy-mm                 | 1982-01               |
+--------------------+-------------------------+-----------------------+ 
| xs:gYear           | yyyy                    | 1982                  |
+--------------------+-------------------------+-----------------------+ 
| xs:duration        | PnnYnnMnnDTnnHnnMnn     | SP26Y02M22DT11H05M20S |
+--------------------+-------------------------+-----------------------+ 

Note that all upper case letters are literals, for example, the “T” in dateTime is literal, denoting the beginning of the Time section. Seconds (ss) may contain decimals. Optionally, dateTime can be extended by a time zone offset of “Z” to represent Zulu time or GMT. For example, Eastern Standard Time is Z-4, Central Europe is Z+1.
“P” in xs:duration indicates that this is a Period of duration and the number precedes the type of period, (i.e., nnY is the number of Years). A period may be of negative duration by placing a negative sign before the “P”, for example a period of minus 10 days (-P10D).
Elements of DateType support the use of a single date or date range. Date ranges are assumed to be inclusive. While normally a range will have a StartDate and EndDate, DDI supports the use of open ranges where only the StartDate or EndDate is known. SimpleDate, StartDate, and EndDate are all BaseDateType.

All dates may be replicated in their HistoricalDate format to reflect how the date was expressed in original documentation. Historical date information parallels the simple date, start date and end date structures of the standard DateType. The date is captured as a string in NonISODate, the format is provided in HistoricalDateFormat (supports the use of a controlled vocabulary), and the calendar type may be specified in Calendar (supports the use of a controlled vocabulary). HistoricalDate, HistoricalStartDate, and HistoricalEndDate are all HistoricalDateType

The overall date format is composed of three primary structures, BaseDateType, DateType, and HistoricalDateType:

Eight elements are defined as DateType. Three additional elements use DateType as an extension base, adding specific additional elements or attributes to define the use of the date in that particular location. Five attributes use BaseDateType. Usage locations are listed below.

+---------------------------------------------------+ 
| Element using DateType                            |
+=========================+=========================+
| datacollection.xsd      | DataCollectionDate      |
+---------------------------------------------------+ 
| reusable.xsd            | EffectivePeriod         |
+---------------------------------------------------+ 
| reusable.xsd            | GeographicTime          |
+---------------------------------------------------+    
| reusable.xsd            | PublicationDate         |
+-------------------------+-------------------------+ 

+-------------------------+-------------------------+ 
| Element using extension base DateType             |
+=========================+=========================+
| datacollection.xsd      | DataCollectionFrequency |
+---------------------------------------------------+ 
| reusable.xsd            | AccessRestrictionDate   |
+---------------------------------------------------+ 
| reusable.xsd            | ReferenceDate           |
+---------------------------------------------------+ 

+---------------------------------------------------+ 
| Attribute using BaseDateType                      |
+=========================+=========================+
| reusable.xsd            | authorizationDate       |
+---------------------------------------------------+ 
| reusable.xsd            | completionDate          |
+---------------------------------------------------+ 
| reusable.xsd            | validForEndDate         |
+---------------------------------------------------+ 
| reusable.xsd            | validForStartDate       |
+---------------------------------------------------+ 
| reusable.xsd            | versionDate             |
+-------------------------+-------------------------+ 
