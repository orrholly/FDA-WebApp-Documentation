
##Data Download
The FDA makes its inspection data available here:    
  * http://www.fda.gov/ICECI/EnforcementActions/WarningLetters/Tobacco/default.htm      
  * http://www.accessdata.fda.gov/scripts/oce/inspections/oce_insp_searching.cfm  
  * Links to compliance and warning letters are supplied in urls in the data above.  

##Data Cleaning

###From http://fdainspections.info/
The data was downloaded from FDA (see above) in CSV (Commma-Separated Values), cleaned (there are some formatting issues in the data), and imported into a relational database.

The cleaned data was then exported in run through geocoding software to get the latitude and longitude. Although this wasn't critical at this step, it was important for later integration with our Streetview project.

Next, a "screen scraping" program was used to download the violation letters, basicially accomplishing the same thing as visiting each url for the violation letter, and saving the HTML (the letter with its formatting). Finally, another program was run that looked for certain patterns -- mostly the sections that were mentioned. The results were stored in a separate table, linked to the letter, which in turn was linked to the inspection and the store.

###From National Enforcement of the FSPTCA at Point-of-Sale
Raw data on compliance checks completed since 2010 are publicly available for download from an FDA website, as well as a map
feature that can display local compliance check outcomes: US Food and Drug Administration.  Available at: http://www.accessdata.fda.gov/scripts/oce/inspections/oce_insp_searching.cfm

The data are imported as comma-separated values to the Legacy GIS platform from the FDA Center for Tobacco Products website. Each line of data describes either a single compliance check or a notification of a Civil Monetary Penalty.

The FDA continuously updates its compliance check database, making all new data available for download once a month.
Unlike these violation documents, the raw data do not include a unique identifier for each store, nor the date the inspection was completed; only the date that a decision was made about the inspection is provided. To track repeat inspections, each line of data was read into a separate record and unique store names were created from the name and address provided.

**Compliance Check Warning Letter Documents**  
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

**Compliance Check Civil Monetary Penalty Documents**    
Civil Money Penalties are issued after a second
compliance check violation, but not necessarily for
repeated infringement of the same statute(s). Civil
Monetary Penalty letters often included details on
statute violations identified at the first violation
(ie, in the initial warning letter), as well as violations
that were observed at subsequent compliance
checks. This required that each Civil Monetary
Penalty document be scanned for statute violations,
to differentiate between repeat versus new offenses noted only in the Civil Monetary Penalty document.
Unlike the URL links to the warning letters,
Civil Monetary Penalty documents are provided as
PDF files. A script was written to download these
files and convert the PDF into a text document,
extracting relevant data via text analysis similar to
that used for the warning letters. In addition to the
data collected from the warning letter files, data extracted
from Civil Monetary Penalty documents included
recent violations and the amount of the fine.

**Violations of Statute 1140.14e**  
Any warning letter that referenced a violation of
statute 1140.14e required further review, as multiple
violation subtypes fell under this statute (Table
1). The many combinations of the violation subtypes
that could be found in any single letter precluded
development of a reliable pattern-matching
script to extract this information. Thus, each letter
needed to be reviewed by a person who could identify
each of the specific violation subtypes listed in
the letter under 1140.14e (ie, advertising, labeling,
and other items; Table 1). To accomplish this, a
custom crowdsourcing platform based on Amazon’s
Mechanical Turk system was employed.20 A
pattern-matching script highlighted text relevant
to 1140.14(e) within these letters and this text
was displayed to multiple independent raters who
were each asked to identify the violation subtypes
cited in the text, with check-boxes for each subtype
provided to the right of the relevant passage. This
task was run repeatedly until there was at least 90%
consensus among the raters as to the subtype.

**Geographic Location of Each Compliance Check**  
The addresses for all FDA compliance checks (N
= 189,594) were batch geocoded by utilizing the
street address locator in Environmental Systems
Research Institute’s (ESRI) ArcGIS Online geocoding
services.21 A batch geocoding match was obtained
for approximately 90% (N = 170,963) of
the FDA compliance check addresses. All tied and
unmatched addresses were manually geocoded following
the batch geocoding results to ensure the
completeness of the spatial dataset. To ensure the
spatial accuracy of the dataset, all matched addresses
that received a score < 85 (N = 149) during
the batch geocoding processes were ortho-verified
to ensure their spatial accuracy. Any addresses that
were not accurately located (N = 226) were orthorectified
to their correct spatial location. The final
spatial dataset of FDA compliance checks was imported
into the GIS database.
The data used in these analyses is publicly available
via the Legacy Tobacco Viewer, a tool that
allows for the examination of changes in FDA
compliance check inspections over time. The tool
is integrated with Legacy’s GIS portal, which allows
users to explore how compliance check inspections
may be associated with a range of other factors. Users
can quickly zoom to their local area and bookmark
their preferences as they overlay various data
sources and visualize the results.
