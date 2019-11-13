Statistical Summary
--------------------
StatisticalSummary provides a set of summary statistics calculated for the variables in a data set and is
located in PhysicalInstance as it reflects the contents of a specific data file. The summary statistics may
be provided in one of three ways; in-line using the VariableStatistics, by referencing a related
PhysicalInstance containing the VaraibleStatistics for the same data file content, or by referencing a
related PhysicalInstance for a data file that contains the summary statistics as a separate object set. The
second two options use the structure StatisticalDataLocation which is a reference to the
PhysicalInstance plus a Boolean attribute "isInline". If set to "true" this indicates that the summary
statistics are contained in the data file associated with the referenced PhysicalInstance.

VariableStatistics supports the following information for any variable: the total responses, a choice of
weights applied when calculating the summary statistics, identification of missing values, the summary
statistics for the variable, and category statistics with an optional filter. Category statistics may be
filtered by a single variable (i.e., filtering the category statistics in a multinational data file by country)
using FilteredCategoryStatistics. Expressing statistics that require the use of multiple filters should be
handled as a cross-tabulation and captured in an NCube structure.

Note that while a number of statistical summaries may be included within a single VariableStatistics
object, you cannot use more than a single weight (either a standard weight or a weight variable).
However you are able to provide both weighted and unweighted values for each statistic. If a complex
weighting structure is used based on multiple weights, a virtual variable should be created that
expresses the combined use of the weights involved. The virtual variable would reference a generation
instruction containing the process.



