
###From National Enforcement of the FSPTCA at Point-of-Sale

Raw data on compliance checks completed since 2010 are publicly available for download from an FDA website, as well as a map
feature that can display local compliance check outcomes: US Food and Drug Administration.  Available at: http://www.accessdata.fda.gov/scripts/oce/inspections/oce_insp_searching.cfm

The data are imported as comma-separated values to the Legacy GIS platform from the FDA Center for Tobacco Products website. Each line of data describes either a single compliance check or a notification of a Civil Monetary Penalty.

The FDA continuously updates its compliance check database, making all new data available for download once a month.
Unlike these violation documents, the raw data do not include a unique identifier for each store, nor the date the inspection was completed; only the date that a decision was made about the inspection is provided. To track repeat inspections, each line of data was read into a separate record and unique store names were created from the name and address provided.

*Compliance Check Warning Letter Documents*
Warning letters issued to retailers following their
first compliance check violation are provided as a
URL linking the data record to an HTML warning
letter. All links were validated and manually corrected
when necessary. Once validated, a custom script
was used to automatically download each HTML
document. Once each warning letter was downloaded,
a customized text analysis script was used
to extract dates and statutes violated. Several variations
of this script were developed to accommodate
individual styles of bullet points, paragraphs and
phrasing, apparently due to manual production of
each letter via word processing software.
