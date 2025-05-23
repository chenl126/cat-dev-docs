# CATReporterInterfaces Framework

## Object Index

  * [RpmReport](CATReporterInterfaces/interface_RpmReport_18193.md)

---

# RpmReport (Object)

**__**

## Methods

### Sub **GenerateReport**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iXMLFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iReportFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iReportType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iOutDTDFileName`)

   This method generates a report to an output file. The definition of the report content is specified by an input XML file.

**Parameters:**

` iXMLFileName`      XML file name for report definition.
` iReportFileName`      The file name to output the report to.
` iReportType`      The report type. The following list represents acceptable values: "Web Page (*.md)" "Text (*.txt)" "Text (Tab delimited) (*.txt)" "CSV (Comma delimited) (*.csv)" "XML (*.xml)" "Excel Workbook (*.xls)"
` iOutDTD`      If iReportType is an XML file, then a .dtd file name is needed. Else send in a null string.