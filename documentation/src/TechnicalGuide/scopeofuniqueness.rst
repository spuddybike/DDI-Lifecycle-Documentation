Scope of Uniqueness
-------------------

DDI 3.2 supports scoping the uniqueness of identifier to the parent
Maintainable or to the Agency (subagency). This choice affects the
structure of the ID as it appears within the Canonical URN (see Type of
Identifier in this section). Essentially, when the ID is scoped to the
Agency the unique identification of an object requires the Agency, ID of
the object, and Version Number of the object. When the ID is scoped to
the Maintainable the unique identification of a non-Maintainable object
requires the Agency, ID of the parent Maintainable, the ID of the
object, and the Version Number of the object. The attribute
scopeOfUniqueness is required and must contain either “Agency” or
“Maintainable”. This attribute defines how the ID will be expressed in
the Canonical URN and what is required for a complete reference to the
object within the Maintaining Agency.
