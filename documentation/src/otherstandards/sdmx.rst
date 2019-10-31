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
