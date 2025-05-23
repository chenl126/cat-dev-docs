# HybridShapeTransfer (Object)

**_Represents the hybrid shape Transfer feature object._**

**Role** : To access the data of the hybrid shape Transfer feature object. This data includes:

  * The element to transfer
  * The surface to unfold
  * The unfolded surface

Use the CATIAHybridShapeFactory to create a HybridShapeTransfer object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **ElementToTransfer**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element to transfer.  
### Property **SurfaceToUnfold**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the surface to unfold.  
### Property **TypeOfTransfer**( ) As long

   Returns or sets the type of transfer.

  * 0= The type of surface is not defined
  * 1= The type of transfer is folded to unfolded
  * 2= The type of surface is unfolded to folded

### Property **UnfoldType**( ) As long

   Returns or sets the type of unfold to take into account during transfer.

  * 0= The type is undefined
  * 1= The surface to unfold is ruled,
  * 2= the surface to unfold is all

### Property **UnfoldedSurface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the unfolded surface.