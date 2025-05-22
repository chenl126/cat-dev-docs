# HybridShapeSection (Object)

**_Interface to hybrid shape section feature._**
**Role** : Allows you to access data of the Hybrid Shape Section feature.

**See also:**      [HybridShapeFactory.AddNewSection](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewSection)

## Properties

### Property **SectionPlane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the section plane..

**Parameters:**

` oPlane`      The section oPlane

**Example** :      This example retrieves in `RefPlane` the plane of the section

```VBScript
Dim RefPlane As Reference
Set RefPlane = HybridShapeSection.SectionPlane

```