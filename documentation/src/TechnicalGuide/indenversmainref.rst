Identification, Versioning, Maintenance and Reference
-----------------------------------------------------

The identification structure of DDI objects is core to the functioning of the standard. The purpose of the DDI identification structure is to:

-  Uniquely identify major objects in a persistent manner to ensure
   accurate reference and retrieval of the object content

-  Provide context for objects where an understanding of related object
   types within a packaging structure is essential to the understanding
   of the object (i.e., a specific classification within a
   classification scheme)

-  Manage metadata object change over time

-  Support the range of object management used by different
   organizations

-  Support early and late binding of references

-  Support interaction with closely related standards, in particular
   ISO/IEC 11179 and SDMX

The identification structure is based on the ISO/IEC 11179 structure
that requires a three-part means of unique identification.

+---------------------+----------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| OBJECT              | ISO/IEC 11179                                                        | DDI                                                                                                                                                                                                                                      |
+=====================+======================================================================+==========================================================================================================================================================================================================================================+
| Agency Identifier   | A unique identifier for the agency managing the object               | A unique identifier for an agency registered with the DDI Alliance. The agency may have multiple sub-agency extensions managed within the DDI Registry or within the primary agency. An agency and sub-agency are separated by an “.”.   |
+---------------------+----------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Unique ID           | A unique identifier of the object within the context of the agency   | An identification which is unique within                                                                                                                                                                                                 |
|                     |                                                                      |                                                                                                                                                                                                                                          |
|                     |                                                                      | a) the agency (sub-agency), or                                                                                                                                                                                                           |
|                     |                                                                      |                                                                                                                                                                                                                                          |
|                     |                                                                      | b) within the parent maintainable. If the context is the parent maintainable the Unique ID is the ID of the parent maintainable plus the ID of the object within that maintainable separated by a “.”.                                   |
+---------------------+----------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Version Number      | A version number of the object to track change over time             | A version number with any number of extensions separated by a “.”.                                                                                                                                                                       |
+---------------------+----------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

This three part structure is the equivalent of a unique persistent identifier for an object, such as described by DOIs and other similar
structures. Note that while use of a version number with a DOI is  optional, based on local practice, the Version Number in DDI is required
due to the need to manage metadata within a dynamic workflow over time.
