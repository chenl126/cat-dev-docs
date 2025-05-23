# HybridShapeBoundary (Object)

**_Represents the hybrid shape boundary feature object._**

**Role** : To access the data of the hybrid shape boundary feature object. This data includes:

  * The boundary propagation
  * The initial element used for the boundary propagation
  * The boundary support

Use the CATIAHybridShapeFactory to create a HybridShapeBoundary object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **From**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Removes or sets the ending limit(i.e Limit2) of the boundary  
### Property **FromOrientation**( ) As long

   Gets or sets the Ending Limit Orientation (i.e same or inverse)  
### Property **InitialElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element used to initialize the boundary propagation.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example retrieves in `InitElem` the initial element of the `ShpBoundary` hybrid shape boundary feature.

```VBScript
     Dim InitElem As Reference
     InitElem = ShpBoundary.InitialElement

```

### Property **Propagation**( ) As long

   Returns or sets the boundary propagation.

**Legal values** : xxxxxxxxxx

**Example** :      This example retrieves in `Prop` the boundary propagation of the `ShpBoundary` hybrid shape boundary feature.

```VBScript
     Prop = ShpBoundary.Propagation

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support surface around which the boundary is computed.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `SupSurf` the initial element of the `ShpBoundary` hybrid shape boundary feature.

```VBScript
     Dim SupSurf As Reference
     SupSurf = ShpBoundary.Support

```

### Property **To**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Removes or sets the starting limit(i.e Limit1) of the boundary  
### Property **ToOrientation**( ) As long

   Gets or sets the Starting Limit Orientation (i.e same or inverse)