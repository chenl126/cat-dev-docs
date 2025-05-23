# ReplaceFace (Object)

**_Represents the Replace Face operation._**
It replaces a face or a set of faces obtained by tangency continuity by a replacing element, such as a surface or a face or a skin.

## Properties

### Property **RemoveFace**(| ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Returns the face to be removed.  
### Property **SplittingSide**( ) As [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)

   Returns or sets the splitting side . The splitting side is the side of the body kept after the splitting. A positive side refers to the same orientation than the splitting element normal vector.  Methods

### Sub **AddRemoveFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemoveFace`)

   Sets the face to be removed.  
### Sub **AddSplitPlane**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSplitPlane`)

   Sets the replacing element.  
### Sub **DeleteRemoveFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemoveFace`)

   Remove the face to be removed.