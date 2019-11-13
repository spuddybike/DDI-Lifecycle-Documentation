Structure of the URN
--------------------

Canonical URN
~~~~~~~~~~~~~

Each section of the Canonical URN is separated by a “:” (colon). Within
the ID section the Maintainable ID and Object ID are separated by a “.”
(dot).

urn:ddi:agency[.sub-agency]:ID:Version

If the scopeOfUniqueness equals “Agency” the ID is the ID of the object.

Example: Canonical URN with uniqueness scoped to the Agency.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Object V321 version 2 within the Minnesota Population Center (us.mpc)

urn:ddi:us.mpc:V321:2

Object V321 version 2 within the Minnesota Population Center, Project
IPUMS (listed as a sub-agency within us.mpc)

urn:ddi:us.mpc.ipums:V321:2

If the scopeOfUniqueness equals “Maintainable” the ID of a
non-Maintainable object is structured as follows:

urn:ddi:agency[.sub-agency]:MaintainableID.ObjectID:Version

Example: Canonical URN with uniqueness scoped to the Maintainable.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Variable V321 version 2 within VariableScheme VS1 at the Minnesota
Population Center (us.mpc)

urn:ddi:us.mpc:VS1.V321:2

Variable V321 version 2 within VariableScheme VS1 at the Minnesota
Population Center, Project IPUMS (listed as a sub-agency within us.mpc)

urn:ddi:us.mpc.ipums:VS1.V321:2

Deprecated URN
~~~~~~~~~~~~~~

Each section of the Deprecated URN is separated by a “:” (colon).

    “urn:ddi:agency[.subagency]:MaintainableObjectType:MaintainableID:ObjectType:ObjectID:ObjectVersion”

If the object itself is Maintainable the information on the parent
maintainable is not included:

urn:ddi:agency[.sub-agency]: ObjectType:ObjectID:ObjectVersion

If the scopeOfUniqueness equals “Agency” the ID is the ID of the object.

Example: Deprecated URN with uniqueness scoped to the Agency.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Object V321 version 2 within the Minnesota Population Center (us.mpc)

urn:ddi:us.mpc:Variable:V321:2

Object V321 version 2 within the Minnesota Population Center, Project
IPUMS (listed as a sub-agency within us.mpc)

urn:ddi:us.mpc.ipums:Variable:V321:2

If the scopeOfUniqueness equals “Maintainable” the ID of a
non-Maintainable object is structured as follows:

urn:ddi:agency[.subagency]:MaintainableObjectType:MaintainableID:ObjectType:ObjectID:ObjectVersion

Example: Deprecated URN with uniqueness scoped to the Maintainable.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Variable V321 version 2 within VariableScheme VS1 at the Minnesota
Population Center (us.mpc)

urn:ddi:us.mpc:VariableScheme:VS1:Variable:V321:2

Variable V321 version 2 within VariableScheme VS1 at the Minnesota
Population Center, Project IPUMS (listed as a sub-agency within us.mpc)

urn:ddi:us.mpc.ipums:VariableScheme:VS1:Variable:V321:2
