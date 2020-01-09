Relationship to Other Standards
================================

In constructing DDI special care was taken to review related standards
as well as previous versions of DDI in order to provide clear mapping to
the contents of outside standards or to incorporate content where
appropriate. Over 25 standards were evaluated. DDI 3 currently has
mapped relationships to the following standards

DDI Codebook (DDI-C) and earlier versions
-----------------------------------------

After conceptualizing the lifecycle model and the design rules for
reuse, DDI-C content was distributed to the schemas comprising DDI-L.
Specific mapping of objects from DDI-C to DDI-L brought to light a
number of specific issues which were then addressed during DDI â€“L
revisions. While specific objects may not always have a specific 1:1
correlation in 3.0, the content of all 2.1 objects has been captured,
often in greater detail or a more consistent manner than in earlier DDI
versions. During the development of DDI 3.2 changes were made in DDI-C
to incorporate more content from the Generic Statistical Business
Process Model (GSBPM) and to add objects that would ease the translation
of DDI-C into DD-L. These objects were also added to DDI-L if not
already present.

Dublin Core and MARC
--------------------

All citations in DDI-L provide the option of entering a supplemental
citation in native qualified Dublin Core (DCTerms). In addition, the
contents of both qualified Dublin Core and the more extensive MARC
record can be mapped to objects in DDI-L. DDI-L has divided the contents
of these records to a number of complex element groups within DDI to
facilitate reuse of specific sub-structures. The major divisions
include:

-  Citation – This structure is used for both DDI content citations and
   citations for external materials.
-  Coverage – Temporal, Topical, and Spatial coverage map to content
   coverage dates, subject and keyword topics, and geographic coverage
   elements. They are held separately in DDI-L in order to allow
   coverage constraint for modules within a single StudyUnit or Group.
-  Location Specific Information – Some information such as acquisition
   date, call number, local identifiers, etc. are related to a specific
   holding and are therefore located in the ArchiveSpecific section of
   the ArchiveModule. This facilitates packaging for transfer and
   incorporation into a different archive.

GSIM (Generic Statistical Information Model)
--------------------------------------------

GSIM provides a standardized set of information objects that flow
through the process model in the creation of official statistics as
represented by the Generic Statistical Business Process Model (GSBPM).
GSBPM has been of interest to DDI since in conception. The DDI Generic
Longitudinal Business Process Model (GLBPM) is modeled on the GSBPM
which itself was informed by the DDI Lifecycle Model. DDI has worked
with the UNECE in the development of GSIM to ensure that these two
standards are compatible. In general, GSIM is a conceptual model whereas
DDI is an implementation model. There is a shared interest in ensuring
that DDI-L can be used as a means of implementing the GSIM conceptual
model.

Mapping work and the development of DDI profiles to support GSIM are
taking place within that community. A primary area for close mapping to
the GSIM structure lies in that areas that relate to their reflection of
the ISO/IEC 11179 Data Element Classification Structure. The terminology
for the objects as well as the documentation for the objects reflects
the GSIM model.

This standard describes the structure and content of a data element as
the basic building block of information. DDI -L is particularly
concerned with providing the information needed to populate an ISO/IEC
11179 data element and support a registry structure. The following
diagram provides the Data Element Structure.

**Figure 1.  ISO11179 Data Element Structure**

.. |figure1| image:: ../../images/iso_1179_data_element_structure.png

|figure1|

International Standard ISO/IEC 11179-1: Information technology –
Specification and standardization of data elements – Part 1: Framework
for the specification and standardization of data elements Technologies
de l’informatin – Spécifiction et normalization des elements de données
– Partie 1: Cadre pout la specification et la normalization des elements
de données. First edition 1999-12-01 (p26)
https://www.oasis-open.org/committees/download.php/6233/c002349_ISO_IEC_11179-1_1999%28E%29.pdf

In DDI terminology, the Object Class is defined by the universe, its
Property is the concept, and the Representation is the Representation
content used by the Variable that measures it.

ConceptualComponent contains Universe and Concept definitions while
Representation is described within the Variable. In most DDI instances
it is the Variable that ties the three sections of this definition
together. Note that if the Variable does not include a concept reference
the instance is not compliant with ISO/IEC 11179.

DDI 3.2 has added the ability to create the more abstract (or reusable)
descriptions of an ISO/IEC 11179 Data Element and Data Element Concept.
These have been structured to align with the GSIM description (see GSIM
in this section). The 3.1 element DataElementConcept has been replaced
by a ConceptualVariable located within ConceptualComponent. This object
links a Concept with a Universe creating the equivalent of the ISO/IEC
11179 Data Element Concept. A RepresentedVariable located in Logical
Product, adds the expression of the representation to the concept and
universe. This is the reusable set of information for a Variable which
is the implementation of a RepresentedVariable within a specific usage.
The underlying RepresentedVariable may be referenced from the Variable.

ISO/IEC 11179
-------------

DDI-L reflects ISO/IEC 11179 structure in several respects. First, it
maps the core structures Concept, Universe, ConceptualVariable, and
RepresentedVariable to the ISO/IEC 11179 Data Element Classification
Structure. The structure presented in DDI 3.2 aligns with the
representation of this ISO standard through the GSIM structure. (See
GSIM discussion within this section).

Secondly, DDI-L has adopted the combination of the Agency, ID, and
Version as the full unique identification of an object. This is
reflected in the identification model and content of the DDI URN.
Finally, DDI-L has incorporated the ISO/IEC 11179-5 structure of
providing a Name, Label, and Description for all primary objects
(maintainable and versionable) that are not considered publication
structures. Publication structures have complete citation information
plus an abstract. The objects with this common descriptive set are those
that are commonly managed with registries over time.

ISO 19115 - Geography
----------------------

The construction of geographic objects within DDI was done using the US
FGDC which is ISO 19115 compliant. The content of the following objects
map to these geographic standards:

In SpatialCoverage:

-  Bounding Box
-  Spatial Object (SpatialPrimative)
-  TopLevelReference
-  LowestLevelReference
-  BoundingPolygon
-  Point

In GeographicResponseDomain:

-  Datum
-  CoordianteSystem
-  CoordinateZone
-  ErrorCorrection
-  Offset
-  GeoreferencedObject
-  CoordinatePairs
-  SpatialPrimitive

The use of these fields provides search information for coordinate based
search systems and detailed information needed by the geographer to
determine the usefulness of a specific data set for geographic analysis.

SDMX
----

Careful comparison was made between DDI-C nCubes and SDMX structures. In
evaluating the structure and application of these two specifications it
was concluded that while basic SDMX structures could be described as
nCubes, not all nCubes could be described in SDMX. SDMX deals with well
structured, well defined data which contains a time dimension. Not all
legacy data contains well structured and well defined aggregate data and
nCubes provide support for these structures. SDMX contained a more
flexible approach to attaching information to regions of cells within
the matrix and used a standard attribute structure to define all aspects
of the matrix from the label to the cell content.

SDMX requires the data cell content to be within the structure while DDI nCubes allow for the
separation of metadata description and data content. In DDI-L the NCube
structure retains the specified objects for Label, Universe, Dimensions,
and Measure but adds the Attribute object and the ability to define
regions of the matrix and to attach attributes to these regions. DDI-L
NCubes were designed to map to both earlier nCube structures and to SDMX
providing support for using SDMX as a data transfer or storage
structure.

METS
----

METS is a standard developed as an initiative of the Digital Library
Federation and provides a consistent outer wrapper for digital objects
described by a variety of METS profiles. The METS structure was
consulted in developing the structure for the Collection and Item
objects in Archive and the intent is to write and register a METS
Profile for DDI.

PREMIS
-------

PREMIS is a common implementation of Open Archive Information System
(OAIS). There is a preliminary mapping of DDI-L to PREMIS objects. The
focus of PREMIS is preservation and there are several elements where
DDI-L does not provide controlled content. However, with the ability to
publish controlled vocabularies external to the DDI specification, we
should be able to address all but a few of the PREMIS objects. Further
alignment with OAIS requirements as expressed in PREMIS and other
preservation will take place as DDI-L expands into process models,
provenance, and archive management content.


