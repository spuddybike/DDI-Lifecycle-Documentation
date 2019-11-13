Versioning
----------

In general, once metadata is published (i.e. flagged as being stable for
referencing purposes) any change to the content should result in a
version change to the Versionable object containing the change. Note
that as Versionable objects are contained by Maintainable objects and
that Maintainable object may be contained in another Maintainable
object, a single change will generally trigger Versioning up the
containing tree of the metadata. The purpose of versioning is to ensure
that someone referencing a specific version of an object will always get
back the same information.

Versioning rules and Version Number structures differ between different
organizations and between different projects or products of the same
organization. DDI does not dictate this structure EXCEPT to specify that
it must be expressed as one or more integers separated by a “.” (dot).
The DDI Lifecycle specification uses a three part structure of a
Major.Minor.Sub-Minor version number. The Organization should describe
its versioning system or systems so that it is clear to the user when
and how versioning occurs. Versioning is “required” once a Maintainable
object is flagged isPublished=”true”. During production processes,
tracking version changes may be managed by other means such as Version
Date or an external subversion system.

Some organizations are stricter in their versioning rules than others.
For example, a typographical correction within a Description text which
is considered to have no impact on the intellectual content may trigger
a Minor or Sub-minor version change in one system while only result in
Version Date change in another. Because the impact of a change cannot be
easily predicted (it is dependent upon the use of the metadata) the
important thing is to capture that a change was made and to provide the
end user with a clear set of versioning rules that supports their
ability to evaluate the impact of the change for their particular use.
In addition, some metadata is considered local in nature, specific to
interaction with an identified system. This metadata is considered to be
Administrative in nature and is viewed by DDI as a set of metadata that
does not alter the intellection content (Payload) of the metadata and
does not need to drive a version change.
