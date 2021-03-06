
Structural Features
====================

Exchange structures
---------------------

DDI Lifecycle instances are published and exchanged with one of two external wrappers, DDIInstance or FragmentInstance. 

The DDIInstance provides a consistent top-level publication wrapper and in addition to some basic information about itself serves as the publication wrapper 
for four primary documenttypes: StudyUnit, Group, ResourcePackage, and LocalHoldingPackage.

The FragmentInstance is a uniform package used to transfer maintainable or versionable objects plus any associated Notes or
OtherMaterial. These would be packets sent in response to system calls (external references, query calls, etc.).

DDI Instance:

.. image:: ../images/ddiinstance.png
   :width: 400px

The Citation, Coverage, OtherMaterial, DDIProfile, and TranslationInformation pertain to the DDI Instance as a whole. Note that the DDIInstance may be viewed as a temporary wrapper for publishing or transporting any of the major publication structures within DDI.

Fragment Instance:

.. image:: ../images/fragmentinstance.png
   :width: 400px

The FragmentInstance is a wrapper for transporting a response to a request for a specific set of information. Although Maintainable, Versionable, and Identifiable objects may be referenced, the FragmentInstance can only transport a Maintainable or Versionable object. 

If an Identifiable is the referenced object, its parent Versionable (or Maintainable) will be supplied. A FragmentInstance may
contain any number of Versionable or Maintainable ojbects. The objects that are the specific responses to the request are listed in the TopLevelReference. For example, a single CodeList (Versionable object) may be requested and the FragmentInstance sent in response may contain the CodeList, the containing CodeListScheme, the referenced Categories, and the containing CategoryScheme. The requested
CodeList would be noted in the TopLevelReference and the content of the returned objects would make up the Fragments.

Maintainable structures
------------------------

DDI has two types of maintainable structures; Modules and Schemes. 

Modules
________

Modules are conceptually related groups of metadata related to stages within a lifecycle. 

.. table
   ::widths |15|30|55|
   
+----------+-----------------------+--------------------------------------------+
| Schema   | Module Name           | Description                                |  
| Prefix   |                       |                                            |  
+==========+=======================+============================================+
| a        | Archive               | Contains information concerning the        |
|          |                       | organization providing archival functions, |
|          |                       | the position of the related metadata and   |
|          |                       | data within the organization, and          |
|          |                       | preservation/provenance information about  |
|          |                       | the metadata and data including            | 
|          |                       | LifeCycleEvents.                           |
+----------+-----------------------+--------------------------------------------+
| l        | CodeList              | A special form of maintainable that allows |
|          |                       | a single codelist to be maintained         |
|          |                       | outside of a CodeListScheme.               |
+----------+-----------------------+--------------------------------------------+
| cm       | Comparison            | Contains information on comparison of      |
|          |                       | similar metadata objects using mapping     |
|          |                       | between a source and target object.        | 
+----------+-----------------------+--------------------------------------------+
| c        | ConceptualComponent   | Contains descriptions of Concepts,         | 
|          |                       | Universes,  DataElements,                  |
|          |                       | ographicStructures,and GeographicLocations |
+----------+-----------------------+--------------------------------------------+
| d        | DataCollecttion       | Contains information on data collection,   |
|          |                       | capture, methodology, and processing of    |
|          |                       | data.                                      |
+----------+-----------------------+--------------------------------------------+
| pr       | DDIProfile            | A specialized meta-model structure that    |
|          |                       | specifies the elements in DDI used by an   |
|          |                       | application, organization, or project and  |
|          |                       | how they are used.                         |
+----------+-----------------------+--------------------------------------------+
| g        | Group                 | A publication module that pulls together   |
|          |                       | multiple StudyUnits with either an         |
|          |                       | intended relationship (i.e., longitudinal  | 
|          |                       | study) or an ad-hoc relationship  (i.e.,   |
|          |                       | studies on aging used within an            |  
|          |                       | instructional package).                    |
+----------+-----------------------+--------------------------------------------+
| g        | LocalHoldingPackage   | A publication structure that allows an     |
|          |                       | archive or library to bind locally         | 
|          |                       | produced metadata to deposited metadata    |
|          |                       | without altering the original metadata set | 
+----------+-----------------------+--------------------------------------------+
| g        | LocalGroupContent     | Locally produced Group content within a    |
|          |                       | LocalHoldingPackage.                       |
+----------+-----------------------+--------------------------------------------+
| g        | LocalResourcePackage  | Locally produced ResourcePackage content   |
|          | Content               | within a LocalHoldingPackage.              |
+----------+-----------------------+--------------------------------------------+
| g        | LocalStudyUnitContent | Locally produced StudyUnit content within  | 
|          |                       | a LocalHoldingPackage.                     |
+----------+-----------------------+--------------------------------------------+
| l        | LogicalProduct        | Contains information on the intellectual   |
|          |                       | structure of the data (i.e., Variables,    |
|          |                       | NCubes), including CategorySchemes,        |
|          |                       | CodeListSchemes, and information on how    |
|          |                       | the data are organized into LogicalRecords | 
|          |                       | and the Relationship of those records to   |
|          |                       | each other.                                |
+----------+-----------------------+--------------------------------------------+
| p        | PhysicalDataProduct   | Contains information on the physical       | 
|          |                       | structure of the data including file       |
|          |                       | structures and RecordLayout structures.    |
|          |                       | Links to the LogicalRecord.                |
+----------+-----------------------+--------------------------------------------+
| pi       | PhysicalInstance      | A metadata record for a datafile providing | 
|          |                       | identification information for the         | 
|          |                       | data file, a link to the RecordLayouts     |
|          |                       | found in the data file, and summary        |
|          |                       | statistics for the data file.              |
+----------+-----------------------+--------------------------------------------+
| g        | ResourcePackage       | A publication structure that allows any    |
|          |                       | maintainable object that is not a          | 
|          |                       | publication package to be published as a   |
|          |                       | reusable resource outside of the context   | 
|          |                       | of a specific study.                       |
+----------+-----------------------+--------------------------------------------+
| s        | StudyUnit             | A publication structure for a specific     |
|          |                       | study. Structures identification           |
|          |                       | information, full bibliographic and        |
|          |                       | discovery information, administrative      |
|          |                       | information, all of the reusable           |  
|          |                       | delineations used for response domains and |
|          |                       | variable representations, and modules      |
|          |                       | covering different points in the lifecycle |
|          |                       | of the study (DataCollection,              |
|          |                       | LogicalProduct, PhysicalDataProduct,       |
|          |                       | PhysicalInstance, Archive, and DDIProfile) |
+----------+-----------------------+--------------------------------------------+

Schemes
________

Schemes are maintainable lists of reusable objects of specified generic types (i.e., questions) and include a means of expressing groups of these objects for administrative purposes. 

.. table
   ::widths |15|30|55|

+----------+-----------------------+--------------------------------------------+
| Schema   | Module Name           | Description                                |  
| Prefix   |                       |                                            |  
+==========+=======================+============================================+
| l        | CategoryScheme        | Categories provide enumerated              |
|          |                       | representations for concepts and are used  |
|          |                       | by questions, code lists, and variables    |
+----------+-----------------------+--------------------------------------------+
| l        | CodeListScheme        | Code lists link a specific value with a    |
|          |                       | category and are used by questions and     |
|          |                       | variables                                  |
+----------+-----------------------+--------------------------------------------+
| c        | ConceptScheme         | Concepts express ideas associated with     |
|          |                       | objects and means of representing the      |
|          |                       | concept                                    |
+----------+-----------------------+--------------------------------------------+
| c        | ConceptualVariable    | Links a concept with a specific object     |
|          | Scheme                |                                            |
+----------+-----------------------+--------------------------------------------+
| d        | ControlConstruct      | Control constructs represent types of      |
|          | Scheme                | constructs used  to represent a process or |
|          |                       | questionnaire flow (Sequence, Statement,   |
|          |                       | IfThenElse, question construct, Loop, etc) |
+----------+-----------------------+--------------------------------------------+
| c        | GeographicLocation    | Locations are specified by type of         |
|          | Scheme                | structure, name, codification, and         | 
|          |                       | definition of physical location            |
+----------+-----------------------+--------------------------------------------+
| c        | GeographicStructure   | Define the structure of geographic         |
|          | Scheme                | hierarchies used to describe geographic    |
|          |                       | area types (States, Cities, Tracts,  etc.) |
+----------+-----------------------+--------------------------------------------+
| d        | InstrumentScheme      | Instruments include any physical means of  |
|          |                       | capturing data                             |
+----------+-----------------------+--------------------------------------------+
| d        | Interviewer           | Instructions related to the interpretation |
|          | Instructionscheme     | or process of capturing data (Interviewer  |
|          |                       | may be an individual or agent, such as a   |
|          |                       | computer, or the interviewee in the case   |
|          |                       | of a self administered survey).            |
+----------+-----------------------+--------------------------------------------+
| l        | NCubeScheme           | NCubes are dimensional data where there is |
|          |                       | a relationship between the individual      |
|          |                       | cells of data (i.e. statistical table,     |
|          |                       | correlation table, etc.)                   |
+----------+-----------------------+--------------------------------------------+
| r        | ManagedRepresentation | Reusable representations of numeric,       |
|          | Scheme                | textual, datetime, scale or missing values |
|          |                       | types.                                     |
+----------+-----------------------+--------------------------------------------+
| a        | OrganizationScheme    | Descriptions of organizations and          |
|          |                       | individuals and their relationships.       |
+----------+-----------------------+--------------------------------------------+
| p        | PhysicalStructure     | Describes the overall physical structure   |
|          | Scheme                | of data records (i.e., storage formats,    |
|          |                       | record parts, default values and types)    |
+----------+-----------------------+--------------------------------------------+
| d        | ProcessingEventScheme | Processing events covering cleaning        |
|          |                       | operations, control operations, data       |
|          |                       | appraisal, weighting, and the applied use  |
|          |                       | of processing instructions.                | 
+----------+-----------------------+--------------------------------------------+
| d        | ProcessingInstruction | General and Generation Instructions used   |
|          | Scheme                | in processing events, data capture, and    |
|          |                       | generation of variables.                   |
+----------+-----------------------+--------------------------------------------+
| r        | QualityStatement      | Statements providing information on        |
|          | Scheme                | standards and/or actions taken to ensure   |
|          |                       | of data, metadata, and processes.          |
+----------+-----------------------+--------------------------------------------+
| d        | QuestionScheme        | Contains Question Items, Question Grids,   |
|          |                       | and Question Blocks used by Control        |
|          |                       | Constructs in creating questionnaires.     |
+----------+-----------------------+--------------------------------------------+
| p        | RecordLayoutScheme    | Record Layouts provide the specific link   |
|          |                       | between the description of a variable or   |
|          |                       | NCube cell with the physical storage       |
|          |                       | location in a data file type.              |
+----------+-----------------------+--------------------------------------------+
| l        | RepresentedVariable   | The core reusable content of a variable    |
|          | Scheme                | providing the concept, object (universe),  |
|          |                       | and representation description.            |
+----------+-----------------------+--------------------------------------------+
| c        | UniverseScheme        | A hierarchical representation of the       |
|          |                       | universes (populations) represented within |
|          |                       | a data collection                          |
+----------+-----------------------+--------------------------------------------+
| l        | VariableScheme        | A list of the variables, their structure,  |
|          |                       | representation, source information,        |
|          |                       | and expression.                            |
+----------+-----------------------+--------------------------------------------+

Organizing Publication Package Contents
----------------------------------------

The major publication packages (StudyUnit, Group, ResourcePackage, and LocalHoldingPackage) organize their contents 
in a set order or sequence. Although all objects may not be available in each publication structure, the order of 
all the included non-maintainable objects remains the same. The maintainable objects in Group and StudyUnit follow the same order. 
In ResourcePackage all maintainable modules fall before the DDI Schemes within the content sequence. 

Note that within the list of maintainable Modules and maintainable DDI Schemes, the ordering is consistent with Group and
StudyUnit. 

The table in **Appendix A** lists the content and order of the three primary publication packages. LocalHoldingPackage is a specialized structure that bundles together a publication package from an external agency (StudyUnit, Group, or ResourcePackage) with similarly structure locally added materials. 

Further information on LocalHoldingPackage structure and usage is found in 3.10 DDI and OAIS – Archives and provenance.
All maintainable objects published within StudyUnit and Group and all non-DDI scheme maintainable objects in ResourcePackage may be included in-line or by reference. DDI Schemes that are included in a ResourcePackage as separate items (i.e., not included within another Module) must be in-line.

ResourcePackage is intended as a means of publishing metadata intended for reuse outside of a single study therefore it is the primary publishing structure for DDI Schemes with content that is used by multiple studies.

How an organization decides to structure its publication packages depends on how they intend to organize, manage, and reuse their metadata. Some organizations publish all their potentially reusable metadata as ResourcePackages with in-line content. StudyUnits and Groups are composed as a set of object specific metadata (Citation through Embargo content) followed by a stack of references. Others
prefer to manage all metadata that is not specifically reused in-line within the context of the StudyUnit or Group. There are advantages and disadvantages to both approaches depending upon User Story in question. 

Both approaches will be discussed within the context of each User Story **[3 User Stories – Applying DDI]**. If an organization uses one extreme or the other for all or a class of metadata, this should be noted within the organization’s DDIProfile. For example, noting that the in-line option is not used for specific objects where there is a choice.

Managing Metadata Over Time
----------------------------

Organizing metadata for the purposes of long-term management may be different than how it is organized for document presentation. DDI 3.2 has provided additional features, such as the ability to include Maintainable objects and most Versionable objects either in-line or by reference, that facilitate the management of metadata outside of specific publication packages. Consider how metadata may be
used in the future to facilitate the following activities: 

- Reuse of metadata such as questions or variables within a series
- Common metadata that can support comparison between studies within a larger collection
(Geographic Structures, Geographic Locations, Concepts, Universe hierarchies, Organizations
and Individuals, etc.)
- Metadata that will be maintained and versioned over time (Categories, Concepts, Geographic
Locations, etc.)

Separating these schemes of metadata from their applied use within as specific study facilitates reuse and comparison. For example, a study that uses a subset of concepts by reference retains information regarding the relationship of those concepts to a broader conceptual model. In organizing metadata for long-term management and broad reuse, consider how the metadata will be reused, in particular making use of nested schemes to facilitate the reuse of common subsets.

Versioning
___________

DDI has a basic rule regarding versioning. If the isPublished of the Maintainable object is set to “true” any change in the content should result in a new version. The exception to this is changes in Administrative Metadata (pt1: Identification, Versioning, Maintenance, and Reference / Administrative and Payload Metadata) which do not trigger versioning. Version numbers follow a specific structure but DDI does not support any specific versioning rules aside from the basic rule. Maintenance organizations
should determine their own versioning rules which may vary by project or over time. 

These should describe the decision rules regarding when an change results in a new version of an object or a new object, level of change (major, minor, sub-minor) and how those are expressed in the version number. These versioning rules should be expressed within the description of the Maintenance organization, project, or individual in the Organization Scheme. This allows users to understand any underlying logic in the versioning system used by the metadata. Completing the field VersionRationale is also an aid to a
future user in determining whether the change will affect their research results. 

Prior to setting the isPublished flag to “true” it is a common practice to leave the version number at 1 (or similar base level) and indicate changes using the version date. Changes in the version date do not affect references to the object yet allow for object level tracking of changes during development periods.

DDI Scheme Groups
__________________

All schemes in DDI have a scheme group structure that allows users to identify sets of scheme objects and scheme groups that have specific relationships to each other. These may be related by subject, concept, universe, usage, or any relationship defined by the user. Because these groups are created by referencing the objects and groups they contain a single object can move into and out of multiple groupings over time. 

These groups are administrative in nature and cannot be used to include a set of objects in another scheme or usage. For example, a QuestionGroup cannot be referenced by a QuestionConstruct as a set of objects.

