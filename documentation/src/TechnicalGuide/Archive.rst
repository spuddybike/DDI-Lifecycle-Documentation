Archive
--------

When DDI talks of archive it is referring to specific activities that take place for the purpose of organizing and preserving the metadata and related data files. Archive activities are performed by the individual or organization responsible for maintaining and preserving the metadata. This could be the individual researcher, a data production organization, or a formal archive dedicated to the preservation of metadata and data. It focuses on the information related to management, preservation, and access.

Archive is a module which contains two types of information. The first is information specific to the instance of the metadata in a specific location. This “ArchiveSpecific” information may have no relevance outside of a specific location. For example, information on the physical storage location of the metadata parts, how they fit into a local collection, or what related materials the archive may contain. In addition to the “ArchiveSpecific” information, the Archive module contains a record of events that are significant in the life of the metadata and houses the OrganizationScheme which describes the organizations and individuals related to the metadata. 

OrganizationScheme and its contents are described in “Organizations, Individuals, and Relations” (xx.xx.xx). An OrganizationScheme may be included in-line or by reference. This allows for the maintenance of a master OrganizationScheme as a ResourcePackage and the inclusion of the relevant sections in individual Archive modules.

The Archive section describes the overall structure of the module, describes the ArchiveSpecific information and provides details on AccessType which is used to describe both default and specific access restrictions at the level of the archive, the collection, or an item.

The Archive contains an ArchiveModuleName, Label, and Description to support its maintenance within a registry system. The purpose of the module is to organize the information about the location, management, and important events surrounding the metadata to which it belongs. ArchiveSpecific information is discussed below and the details of the OrganizationScheme are found in “Organizations, Individuals, and Relations” (xx.xx) . A key feature in Archive is the LifeCycleInformation object which contains an unsorted stack of LifecycleEvents. These events are identifiable and may have Note or OtherMaterials attached to them. These should all be contained within the Archive module so they do not risk becoming disassociated with the related object.

LifeCycle Information 
______________________

A LifecycleEvent is any event that the user decides has value to the archive or the end user. Capturing data and metadata processing information related to ingest and management of metadata within an archive or similar organization is a common use of this section. 

The LifecycleEvent contains a label for the event, specifies the type of event being captured (supports the use of a controlled vocabulary for this object), specifies the date of the event, the organizations or individuals involved by reference to their description in an OrganizationScheme, and describes the event. The event may be attached to one or more identifiable objects within the metadata by use of Relationship. This is the same structure as used in Note(xxx.xx) and OtherMaterial (xxx.xx).

Archive specific
________________

ArchiveSpecific focuses on the place of the metadata within the collections of the organization which maintains the original or a local depository copy. The first object in ArchiveSpecific is a reference to the description of the ArchiveOrganization itself. This description within an OrganizationScheme should contain all of the relevant contact information for the Archive Organization, any special identifiers such as its DDI Agency identification, information on how it handles versioning, and any other information that would be useful to anyone needing to interact with the agency. Item and Collection, both of which can internally nested objects of the same type, provide flexibility for the archive to describe its holdings. 

At the level of ArchiveSpecific you can describe the general or DefaultAccess rules and processes for the Archive (these may be superseded by rules for specific items or collections), FundingInformation for archival processing or collection and Budget information. QualityStatements, such as adherence to OAIS or various certification programs, are included here by reference. A statement of the overall coverage of the archive may be described in spatial, temporal, and topical terms.

Item and Collection are similar in structure. Archives deal with addressable byte streams, files, representations (objects collectively representing an intellectual entity), as well as collections and sub- collections of those objects. An archive should be internally consistent in how it organizes this information about the objects it contains, but DDI does not dictate the organization structure. For example, a Representation may be described as an Item containing several sub-items each representing a file and/or byte stream. Others may define a Representation a form of Collection with an Item used to define individual files and byte streams.

Both Item and Collection capture the following information about a digital object: a citation for the object, it’s physical location in the archive such as a remote or offline storage location, a CallNumber (internal identification number), the URI, the StudyClass which is used to represent any processing or other non-topical means of classification within the archive, a reference to the original archive organization (where did it come from), availability status, quantity of related data files, a statement concerning the completeness of the collection, and a recursive object (Item or Collection) used to create nested hierarchies.

The unique objects in Item refer to the physical manifestation of a single item including the ItemFormat, Media, and Access restrictions/permissions specific to the Item. The unique objects in Collection reflect its description of a set of objects including, ItemQuantity (a check sum), and DefaultAccess providing restrictions/permissions for the set (these can be overridden at the item level).

AccessType is used by both Access and DefaultAccess to describe the details of any permissions or restrictions related to a specific object or a set of objects. In general, default access specifications at the archive or collection level are applied to their contained objects unless overridden by conflicting Access information lower down. For example, an archive may have a policy of open access to all users, but a specific collection may require registration, or an individual object may be private and inaccessible to any users outside of the research project that created it.
AccessType is identifiable so that external documents may be associated with it. It contains a Name, Label, and Description to assist in managing multiple access statements. Note that while the term “restriction” is used the content may be captured as descriptions of specific restrictions or permissions, whichever is clearer.

- AccessRestrictionDate provides a timeframe for the access description. 
- ContactOrganizationReference provides a reference to the organization or individual to contact for further information regarding access. If an organization or sub-organization is referenced, changes in personnel or contact numbers can be captured in the 
- OrganizationScheme. The following descriptive content are all of type StructuredStringType supporting both language replication and structured content for clarity: 
  - ConfidentialityStatement, 
  - Restrictions, 
  - CitationRequirement, 
  - DepositRequirement, 
  - AccessConditions, and 
  - Disclaimer. 
- AccessPermission is a reference to a specific form, either physical or digital, used to arrange for access to an item. It contains a form number, a URI, a Statement relaying the use and purpose of the access form (InternationalStringType), and a Boolean attribute indicating whether completion of the form is required for access.
