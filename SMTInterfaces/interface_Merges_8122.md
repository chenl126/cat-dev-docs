# Merges (Collection)

**_Interface to compute CATIAMerges_**

## Methods

### Sub **CleanUp**(| )

   Performs some clean-up.  
### Func **ComputeMerge**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  double  `iAccuracyForSimplification`,  long  `iKeepEdges`,  long  `iDecoration`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes the merge on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
` iAccuracyForSimplification`      Set this to a non null value to have the simplification activated.
` iKeepEdges`      Do you want edges in the result?
` iDecoration`      Do you want decorations in the result?

**Returns:**      MergeDocument: Document containing the result.  
### Func **MergeShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the name of the associated shape.