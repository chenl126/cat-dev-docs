# V4MasterModel (Object)

**_Represents the V4 Master Model._**
The Master is the root cotainer of a V4 Model.

## Properties

### Property **V4DocumentModel**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md) (Read Only)

Returns the V4 Document that contains the Master's Model.

**Example:**      This example retrieves in `V4Document` the document that contains the `V4Master`.

```VBScript
Dim V4Document As Document
Set V4Document = V4Master.V4DocumentModel

```