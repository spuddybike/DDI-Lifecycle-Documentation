
Structural Features
*******************

Exchange structures
---------------------

DDI Lifecycle instances are published and exchanged with one of two external wrappers, DDIInstance or FragmentInstance. 

The DDIInstance provides a consistent top-level publication wrapper and in addition to some basic information about itself serves as the publication wrapper 
for four primary documenttypes: StudyUnit, Group, ResourcePackage, and LocalHoldingPackage.

The FragmentInstance is a uniform package used to transfer maintainable or versionable objects plus any associated Notes or
OtherMaterial. These would be packets sent in response to system calls (external references, query calls, etc.).

DDI Instance:

.. image:: ../images/ddiinstance.png

The Citation, Coverage, OtherMaterial, DDIProfile, and TranslationInformation pertain to the DDI Instance as a whole. Note that the DDIInstance may be viewed as a temporary wrapper for publishing or transporting any of the major publication structures within DDI.

Fragment Instance:

.. image:: ../images/fragmentinstance.png

The FragmentInstance is a wrapper for transporting a response to a request for a specific set of information. Although Maintainable, Versionable, and Identifiable objects may be referenced, the FragmentInstance can only transport a Maintainable or Versionable object. 

If an Identifiable is the referenced object, its parent Versionable (or Maintainable) will be supplied. A FragmentInstance may
contain any number of Versionable or Maintainable ojbects. The objects that are the specific responses to the request are listed in the TopLevelReference. For example, a single CodeList (Versionable object) may be requested and the FragmentInstance sent in response may contain the CodeList, the containing CodeListScheme, the referenced Categories, and the containing CategoryScheme. The requested
CodeList would be noted in the TopLevelReference and the content of the returned objects would make up the Fragments.

Maintainable structures
------------------------

DDI has two types of maintainable structures; Modules and Schemes. Modules are conceptually related groups of metadata related to stages within a lifecycle. Schemes are maintainable lists of reusable objects of specified generic types (i.e., questions) and include a means of expressing groups of these objects for administrative purposes. 

The following is a list of Modules and Schemes available in DDI Lifecycle along with the namespace of the object, the object name, and a description.

Modules
________

+--------+-------------------------+-----------------------------------------------------------------------------------+
| Prefix | Module Name             | Description                                                                       |  
+--------+-------------------------+-----------------------------------------------------------------------------------+
| a      | Archive                 | Contains information concerning the organization providing archival functions,    |
|        |                         | the position of the related metadata and data within the organization, and        |
|        |                         | preservation/provenance information about the metadata and data including         | 
|        |                         | LifeCycleEvents.                                                                  |
+--------+-------------------------+-----------------------------------------------------------------------------------+
| l      | CodeList                | A special form of maintainable that allows a single codelist to be maintained     |
|        |                         | outside of a CodeListScheme.                                                      |
+--------+-------------------------+-----------------------------------------------------------------------------------+
| cm     | Comparison              | Contains information on comparison of similar metadata objects using mapping      |
|        |                         | between a source and target object.                                               | 
+--------+-------------------------+-----------------------------------------------------------------------------------+









