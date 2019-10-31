Variable Value Representation and Question Response Domain
-----------------------------------------------------------

Representations describe the structure and content of data as it is captured from the population and held within a data file. They share common category schemes and code list as well as the means of defining numeric ranges and text content. DDI begins by defining the core descriptive content for a wide range of representations and then adds a set of common objects used by all Value Representations (Variables) or Response Domains (Questions) in their applied use. A number of these representations also have a Managed version which allows a single description of a Representation to be reused within and between studies. Some Representations reference reusable structures (Category Schemes, Code Lists, etc.) and are already reusable. Others such as Numeric Representations have a Managed Representation contained in a ManagedRepresentationScheme located in Logical Product. This Scheme contains all forms of Managed Representations and supports the standard Scheme organizational objects that allow for grouping and classification according to Subjects, Keywords, Concept and Universe.

This section describes the types of Representation available for use along with the added content for use as a Value Representation or Response Domain. This is followed by a full description each Representation Base type and a description of Managed Representation types. Note that wherever the substitution base ValueRepresentation or ResponseDomain is used there is also an option for a ValueRepresentationReference or ResponseDomainReference. Only Representations containing managed content (ManagedRepresentation types, CategoryScheme, CodeList, GeographicStructureCode, and GeographicLocationCode) can be mapped for comparison purposes. This excludes most Representation types that are used solely as Response Domains.

ValueRepresentation and ResponseDomain are the applied uses of Representations.

ValueRepresentation (abstract)
_______________________________

ValueRepresentation serves as the abstract head of a substitution group ValueRepresentation. Any member of the substitution group can be used as a substitution for r:ValueRepresentation wherever it occurs. All members of this group use r:RepresentationType as their extension base thereby providing a standard set of objects for each ValueRepresentation.

All ValueRepresentations contain a base set of objects describing its applied use. The RecommendedDataType is of type CodeValue and should contain a value reflecting a data type value (recommended: W3C XML Schema Part 2, but excluding string sub-types, QNAME, and NOTATION). The actual data type of the stored data content may vary (for example be of a broader type), but the purpose of this element is to capture the data type intended by the originator of the data. Likewise GenericOutputFormat allows the originator to provide guidance regarding the displayed format of the variable content. ContentDateOffset provides an alternate referent date for the variable content. For example, in a population survey the data may generally be collected for a particular date but some items such as the response to “Where did you live 5 years ago?” refers to a negative offset of 5 years from the general referent date. The attribute classificationLevel allows for definition of the variable content as Nominal, Ordinal, Interval, Ratio, or Continuous in nature.

Note that the two attributes @missingValue and @blankIsMissingValue have been retained from DDI 3.1 to support users for whom the shift to the new separation of missing (invalid) values from valid values would be problematic. Best practice strongly encourages the use of the separate MissingValueRepresentation to differentiate valid from invalid values.

ValueRepresentation substitutions
__________________________________

All value representation substitutions contain the basic ValueRepresentation objects plus a reference to one or more of the specific delineation of the same type. Note that if multiple representations are referenced they must not have duplicated values. These include:
- CodeRepresentation
- DateTimeRepresentation
- GeographicLocationRepresentation 
- GeographicStructureRepresentation 
- NumericRepresentation
- TextRepresentation

Within a Variable the representation of missing values is handled separately as a direct reference to a MissingValuesDelineation structure. This may also be declared as a default MissingValues within a LogicalRecord or within a PhysicalInstance.

ResponseDomain (abstract)
_______________________________

Response Domain serves as an abstract head of the substitution group Response Domain. Any member of the substitution group can be used as a substitution for d:ResponseDomain wherever it occurs. All members of this group use a specified Representation Base Type (ex. NumericRepresentationBaseType) as their extension base thereby providing the same set of content as contained in related Value Representation. 

**All members of the substitution group ResponseDomain also provide the following objects.**

All Response Domains can designate the intended cardinality of responses as a statement of minimum and maximum number of allowed responses. The OutParameter provides an ID for the response (or response array) so that it can be bound to the InParameter of an instruction or command (see Input/Output Parameters and Command Code for usage details). ContentDateOffset provides an alternate referent date for the question response content.

ResponseDomain substitutions
_______________________________

All response domain substitutions contain the basic ResponseDomain objects plus the contents of one of the specific Representation Base of the same type. Note that when using multiple domains in the StructuredMixedResponseDomain the multiple domains must not have duplicated values. Available Response Domains include:

- CategoryDomain
- CodeDomain
- DateTimeDomain
- DistributionDomain
- GeographicDomain
- GeographicStructureDomain
- GeographicLocationDomain
- LocationDomain
- MissingValuesDomain 
- NominalDomain
- NumericDomain
- RankingDomain
- ScaleDomain 
- TextDomain

Representation Base Types
_______________________________

A range of Representation Base Types are available. Each type is described as a specified Representation Base Type. All of these have related specific Response Domains, but not all have specific Value Representations. This reflects the way that the data captured by a question is represented within a data set. For example, a question may ask for a check mark to be made next to a category value which is later coded to a value which represents the category such as, M=Male. The ValueRepresentation would use the CodeRepresentation to define the valid values entered in the data file. 

**The following list of Representation Base Types defines the usage options for each type:**

Note that all Representation Base Types are never used directly (i.e. there is no “CodeRepresentationBase” but a “CodeRepresentation” of type “CodeRepresentationBaseType”). All Representation Base Types have an extension base of Representation Type and therefore **all contain the following objects preceding any specific content:**

CodeRepresentationBaseType
_______________________________

Defines a CodeRepresentation by referencing a CodeList and describing the valid code subset used. For example, the complete CodeList, a specified level or range, or only the most discrete codes in the list.

References the CodeList used by the Representation and defines the portion of the CodeList used by the CodeSubsetInformation. CodeSubsetInformation allows for the specification of a level number from the CodeList to be included in the RepresentationBase, included codes defined as a range, or the specification of the just the most discrete data codes. The Range specifies the unit of the range specification as well as a minimum and maximum value. Note that these values use and extended form of Value which allows for the declaration of significant leading or trailing white space within the value as well an attribute noting if the value is inclusive (i.e., included as a valid value in the range specification). DataExistence is specified by the lowest level number for regular hierarchies or by selecting those Code items with the attribute isDiscrete=”true” from the CodeList for irregular hierarchies.

DateTimeRepresentation
_______________________________

Defines a DateTimeRepresentation by prescribing its structure and content coverage.

The DateTimeFieldFormat is a CodeValue which describes the format of the date field, in formats such as YYYY/MM or MM-DD-YY, etc. If this element is omitted, then the format is assumed to be the XML Schema format corresponding to the type attribute value. The use of an external controlled vocabulary is strongly recommended. The DateTimeCode is a CodeValue and is required. This is a standard XML date type code for example date, dateTime, gYearMonth, gYear, and duration. The use of an external controlled vocabulary is strongly recommended.

GeographicLocationCodeRepresentation
_____________________________________

This Representation allows for the direct use of the contents of a Geographic Location Value as a GeographicLocationCodeRepresentation or a GeographicLocationCodeDomain. This relieves the user of creating a secondary Code List reflecting the same information and retains contextual information in the use of Geographic Locations as response domains or representations. References the GeographicLocation used, identifies which code is being used based on the AuthorizationSouce and allows specifying which codes to exclude from a set, similar to specific object exclusion from a Scheme Reference.

Note that the Representation references a single location type. The use of the Representation as a response domain or value representation may include the complete code or a component segment of the complete code. When used for a Response Domain if the full unique hierarchical string (i.e. State— County—Tract) is being collected as a single object then a single Representation can be used. 

However, if the captured data will be stored as separate variables use a StructuredMixedResponseDomain in a Question using one GeographicLocationCodeRepresentation for each segment of the complete code.

GeographicLocationCodeRepresentation provides a LimitedCodeSegmentCapture which is used to identify the segment of a Geographic Location Code which is captured in this domain. For example, a County’s unique location code may be a composite of a State code (2 characters) + County code (3 characters). LimitedCodeSegmentCapture provides a description of the code segment captured in the response and specifies it through the following attributes: arrayBase (clarifying the array based used when determining the start position in the code) startPosition (the first character of the captured code), and the length (the number of characters making up the captured code). 

GeographicLocationRepresentation also provides a LimitedCodeSegmentCapture which is used to identify the segment of a Geographic Location Code which is captured in this domain. See Response Domain section above for description of its use.

**This shows a GeographicLocationCodeRepresentation that contains the full required code for the unique identification of a county, both State and County codes. If the example also contained the LimitedCodeSegmentCapture described above the ValueRepresentation or ResponseDomain using this description would capture ONLY the 3 character County Code portion of the unique string. It would have to be paired with a State code in order to uniquely identify the County.**

GeographicStructureCodeRepresentationBase
__________________________________________

RepresentationBase for the direct use of a GeographicStructureCode as a GeographicStructureRepresentation or GeographicStructureDomain. This relieves the user of creating a secondary Code List reflecting the same information and retains contextual information in the use of Geographic Structures as response domains or representations. References the GeographicStructure used, identifies which code is being used based on the AuthorizationSouce and allows specifying which codes to exclude from a set, similar to specific object exclusion from a Scheme Reference.

Note that a single value representation or response domain can contain only a single code set for the structure which is identified by its Authorization Source. If a single agency manages several code types they should be clearly differentiated with separate Authorization Source identifiers (i.e., specified down to the specific coding list).


NumericRepresentationBase
_______________________________

Defines a NumericRepresentationBase by describing the valid numeric range, expressing top or bottom codes, and the valid type for the content.
Provides the valid numeric range in terms of a High and Low number, TopCode or Bottom code, as well as constraining the content through use of a controlled vocabulary. The NumericTypeCode provides definition of the W3C XML numeric type such as integer, decimal, etc.

TextRepresentationBase
_______________________________

Defines a TextRepresentationBase used by a TextRepresentation or TextDomain, describing the maximum and minimum length of the text string, and providing a regular expression to further constrain the content.

Text allows for the definition of a minimum and maximum length of the text object as well as constraining the allowed content through use of a regular expression.

CategoryRepresentationBase
_______________________________

Defines a CategoryRepresentationBase by specifying the Category Scheme used. References a CategoryScheme allowing for the exclusion of any specified object within the scheme.

DistributionRepresentationBase
_______________________________

Defines a distribution structure used as a response domain, indicating the total amount to be distributed among the response objects.

The DistributionValue provides the total value (xs:decimal) to be distributed among the response objects. The decimalPositions attribute clarifies the level of detail allowed in terms of the number of decimals accepted within a response.

GeographicRepresentationBase
_______________________________

A specialized RepresentationBase that contains the basic information required to collect geographic information from a GIS or similar system. Provides default values as well as fields to capture case specific deviations from the default.

The following objects define the default values defined for the response domain: 

- Datum identifies the geographic datum type of the object (recommend use of controlled vocabulary), 
- CooridnateSystem identifies the coordinate system used by the response domain, 
- CoordinateZone specifies the geographic coordinate zone used, 
- the source of the coordinate reading is supplied in CoordinateSource, 
- the standard offset is given in Offset,
- and the object used for identifying the point of the coordinate being collected is listed in the GeoreferenceObject (i.e., front door or centroid). 
- If an address match is used AddressMatchType specifies the type of matching used. CoordinatePairs provides the capture structure for the case content. The attributes pointFormat and spatial primitive specify the format structure of the point and the spatial type being captured (Point, Polygon, Line or Linear Ring). AltenateOffset, AlternateObject, and AlternateCoordinateSystem provide capture points for case specific information when the default values are not used.

LocationRepresentationBase
_______________________________

Defines a mark and the region within an object (i.e., image, text, etc.) where the mark should occur. Primarily used as a response domain within a QuestionBlock.

Object specifies the object upon which the action takes place. Action describes the action(s) which take place. Action specifies the region within which the action takes place described in terms of a start, stop, or region definition appropriate to each type as well as a description of the action itself.

NominalRepresentationBase
_______________________________

Defines a nominal response that is not coded or related to a particular category scheme. Used primarily by QuestionGrid, this defines a response where there is a simple check or other demarcation expressing a binary “yes | no” or “true | false” response.

A simple description of a nominal response which may be constrained by a regular express to a specified mark.

RankingRepresentationBase
_______________________________

Defines a ranking structure used as a response domain, indicating the ordering options for the response.

The RankingRange is an extension of Range adding the attribute maximumRepetitionOfSingleValue. The RankingRange specified the unit used for expressing the rank, provides a minimum and maximum value for the rank, and specifies how many items may have the same rank (default=”1”). 

The Range specifies the unit of the range specification as well as a minimum and maximum value. Note that these values use and extended form of Value which allows for the declaration of significant leading or trailing white space within the value as well an attribute noting if the value is inclusive (i.e., included as a valid value in the range specification).

ScaleRepresentationBase
_______________________________

Defines a range of scale based responses varying by display, number of dimensions, and anchors.

Scale layouts may affect the validity and comparability of the data captured. ScaleRepresentationBase allows a specific definition of each dimension of the scale, the DimensionIntersect for multi-dimensional scales, and the specific of the scale layout. The ScaleDimension indicates the complete numeric range or textual range, the anchor for the scale expressed as a category and/or value, a label for the dimension, the marked increments of the scale, and the value increment. 

Both MarkedIncrement and ValueIncrement are described by the attributes increment, startValue, and endValue. The DimensionIntersect is used when the scale contains more than one dimension. In its simplest form the attribute forAllDimensions is left at its default setting of “true” and the intersect point is defined by the attribute intersectValue. DisplayLayout is of CodeValueType and contains a definition of the type of scale such as scale line, value list outline, etc.

MissingValuesRepresentationBase
_______________________________


Defines missing values as a numeric or code RepresentationBase which can be used with any other response domain or value representation. When combining a MissingValueRepresentationBase with valid responses or representations the user must take care not to replicate any valid response or representation. This structure allows for specifying missing values, specific definition of missing values through the use of a CodeRepresentationBase, and the definition of a blank (null) as a missing value.

MissingValueRepresentationBase provides multiple means of describing missing values. They may contain any combination of a CodeRepresentationBase, NumericRepresentationBase, or TextRepresentationBase. In addition, the process of determining the how the missing value is assigned (generation instruction) may be referenced.

