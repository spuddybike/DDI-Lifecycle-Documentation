Identifiable, Versionable, and Maintainable
-------------------------------------------

DDI differentiates between a set of element types. Not all objects are
individually identifiable, i.e. some objects only have meaning within
the context of an identifiable object such as a Label or Description.
The remaining objects are Identifiable, Versionable or Maintainable in
order to support different levels of metadata management.

*Identifiable objects* are those that can be referenced directly either
for inclusion in another object or for the purpose of attaching Other
Material or a Note to the object. Identifiable objects have a unique ID
within the context of their specified scope of uniqueness (see Scope of
Uniqueness discussion within this section). Their Agency Identification
and Version Number match those of the object’s immediate parent
Versionable (or Maintainable if there is not a parent Versionable) at
the point of creation. This means that if an Identifiable object is
created within a version 1 of a parent Versionable and does NOT change
its content over time it will retain its Version Number of 1 until the
identifiable object itself is altered. It will then change its Version
Number to that of its parent Versionable at the time of the alteration.
In other words an Identifiable could go from a Version 1 to a Version 4
without ever having a Version 2 or 3 if the cause for versioning did not
involve any change in the Identifiable object within Version 2 and 3 of
the parent Versionable.

A *Versionable object* has the characteristics of an Identifiable object
but may be managed over time. DDI has determined that being able to
track change within the object over time is a requirement, either to
understand the relationship to earlier objects of a similar type or to
track provenance. Note that it is up to the individual content provider
to determine whether an object is essentially new or is a modification
(version) of an earlier object. Versionable objects have a unique ID
within the context of their specified scope of uniqueness (see Scope of
Uniqueness discussion within this section). Their Agency identification
matches that of the object’s immediate parent Maintainable at the point
of creation. In other words the Agency of an object does not change
simply because it is included by reference in a Maintainable managed by
a different agency. The Version number of the object changes each time
its content changes. See Versioning for a discussion of when and how
this may be implanted within different organizations or projects.

A *Maintainable object* is a type of packaging and generally takes the
form of either a module or scheme. Modules package metadata focused on
specified segments of the Lifecycle for which context is important for
understanding. Schemes are similar to data base tables, containing a
stack of similar type objects that many have important contextual
relevance to each other, i.e. a classification scheme captured in a DDI
Category Scheme. There is one unique form of a Maintainable which is the
CodeList. A CodeList is a Maintainable in its own right for the purpose
of supporting the statistical production process. However it can only be
published within the context of a parent Maintainable Scheme. All
Schemes and Modules may be published within the context of a Study Unit
or Group (a collection of Study Units) or as a separate Resource Package
item primarily for the purpose of reuse.
