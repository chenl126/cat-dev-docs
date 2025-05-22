# AnalysisLocalSensor (Object)

**_Represent the analysis local sensor._**

This object is a kind of AnalysisSensor based on analysis feature results
based on a finite element selection. This sensor definition is based on an XML file
stored in the CATIARuntimeView.

## Properties

### Property **XMLName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the Identifier of the sensor as defined in the XML file.

**Example:**      This example retrieves in `MyXMLName` the identifier of the `AnalysisSensor1` object.

```VBScript
MyObjectName = AnalysisSensor1.XMLName

```