Quality Descriptions
---------------------

DDI addresses descriptions of quality at three levels, the quality of the metadata as captured, means of ensuring policy for processing, and the quality of the data. Statements regarding the quality standards used for processing or measuring the quality of the data related to the metadata may be referenced from the following areas: study unit, group, sub-group, resource package, methodology, various descriptions of data processing, data file creation or copying, and archival processing.

Metadata Quality
_________________

Metadata quality is captured at the level of the Maintainable object and refers to the metadata contained in that object. It is held in the complex element MetadataQuality which is found in AbstractMaintainable. It is a relatively simple statement of quality such as completeness, transcription of content from the original source, level of review or verification, etc.

Both TypeOfMetadataQuality and MeasureValue are CodeValueType and support the use of an external controlled vocabulary. These are the two primary pieces of information needed to track metadata quality internally within an organization. TypeOfMetadataQuality identifies the measure being tracked and MeasureValue provides a specific value for that measure. For example, an organization may have a number of measures one of which rates its transcription quality. 

It may have various values for this including: 

- 1) Tagging and transfer of a digital content, 
- 2) double entry, 
- 3) single entry direct transcription, 
- 4) selected transcription, and 
- 5) summarization. T

he purpose for capturing the measure is held in MeasurePurpose (StructuredStringType) and other descriptive information that is useful to the organization or in particular a user, is held in Description (StructuredStringType).

Quality Statement
__________________

Quality statements are compiled in a QualityStatementScheme which may be published within a StudyUnit, Group, or ResourcePackage. Quality statements primarily address processes and steps that are taken to ensure quality within those processes. A QualityStatement allows for either the identification of an external standard plus a statement regarding compliance with that standard, or a general statement of steps taken to ensure quality for a given process or activity. A QualityStatement is attached to a processing area by reference from the description of the process/activity itself.

StandardsCompliance consists of a reference to the Standard using the structure of OtherMaterial. This could reference a document, web site, or other source containing a formal standard for processing, best practice, internal protocol, or other statement of quality. ComplianceDescription (StructuredStringType) provides details on how this standard or protocol was applied, in particular noting any deviations or issues that would have an impact on the quality factors being assessed. 

When no formal standard or protocol exists, use OtherQualityStatement (StructuredStringType to describe steps taken to ensure quality. Quality statements can be referenced from the following locations and should relate quality assessment information focused on the process activity or general coverage area where the reference is included.

Data Quality
_________________

The quality of the data collected is addressed in the ProcessingEvent containing DataAppraisalInformation. This contains two common measures of data quality from survey methodology, ResponseRate and SamplingError. It also allows for the description of other quality measures in OtherAppraisalProcess. Note that ProcessingEvent also contains a QualityStatementReference. This should be used to relay information on process quality. DataAppraisalInformation is used primarily to capture the results of data appraisal measures.

The response rate can be repeated to express differing response rates by mode of deliver, location, etc. The individual response rates may be expressed as a total sample size with number of responses and/or as a specific response rate. The description should be used to differentiate when multiple response rates are provided. SamplingError (StructuredStringType) is intended to contain a discussion of the sampling error. It may be structured to differentiate between the statement of the error itself, how it was calculated, etc. OtherAppraisalProcess allows for the description of other measures of data appraisal as needed.

