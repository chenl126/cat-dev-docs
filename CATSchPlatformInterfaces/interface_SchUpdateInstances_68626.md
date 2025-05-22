# SchUpdateInstances (Object)

**_Interface to update all component instances when the catalog reference component has been changed._**

## Methods

### Sub **UpdateAllInstancesFromReference**( [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)  `iCompLocalRef`)

Update all the instances of a given local reference in a document. Both the local reference and all its instances will be updated to account for any changes in the corresponding catalog reference.

**Example:**      This example illustrates how to update all the schematic component instances in the active document by selecting any one of the instances or their local reference.

```VBScript
' --- get SchUpdateInstances interface
Dim objCurrentDoc As Document
Dim objPrdRoot As Product
Dim objSchRoot As SchematicRoot
Dim objUpdateInstances As SchUpdateInstances
Set objCurrentDoc = CATIA.ActiveDocument
Set objPrdRoot = objCurrentDoc.Product
Set objSchRoot = objPrdRoot.GetTechnologicalObject ("SchematicRoot")
Set objUpdateInstances = objSchRoot.GetInteface ("CATIASchUpdateInstances",objCurrentDoc)

' --- get the local reference
Dim objPrdInst As Product
Dim objPrdRef As Product
Dim objCompRef As SchComponent
' --- get an instance, objPrdInst from the selected set of objects
Set objPrdInst = objCurrentDoc.Selection.FindObject("CATIAProduct")
Set objPrdRef = objPrdInst.ReferenceProduct
Set objCompRef = objSchRoot.GetInterface ("CATIASchComponent",objPrdRef)

' --- update all the instances
objUpdateInstances.UpdateAllInstancesFromReference objCompRef

```