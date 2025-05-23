# HybridShapeSplit (Object)

**_Represents the hybrid shape split feature object._**

**Role** : To access data of the hybrid shape split feature. This data includes:

  * The element to be cut (surface or curve)
  * The cutting element ( surface, curve or point)
  * An orientation to specify which side has to be kept

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect
Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **AutomaticExtrapolationMode**(| ) As boolean

   Gets or sets the automatic extrapolation mode status. AutomaticExtrapolationMode = TRUE : Automatic extrapolation mode is on. = FALSE : Automatic extrapolation mode is off. This example retrieves in `AutoExtrapolMode` the automatic extrapolation mode status for the `Split` hybrid shape feature.

```VBScript
     Dim AutoExtrapolMode As boolean
     AutoExtrapolMode = Split.AutomaticExtrapolationMode

```

### Property **BothSidesMode**( ) As boolean

   Gets or sets both sides computation mode. BothSidesMode = TRUE : Both sides are computed. = FALSE : Both sides are not computed. This example retrieves in `BothSides` the both sides computation mode for the `Split` hybrid shape feature.

```VBScript
     Dim BothSides As boolean
     BothSides = Split.BothSidesMode

```

### Property **CuttingElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the cutting element.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `CuttingElement` the cutting element for the `Split` hybrid shape feature.

```VBScript
     Dim CuttingElement As Reference
     Set CuttingElement = Split.CuttingElem

```

### Property **ElemToCut**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element to cut.

**Example** :      This example retrieves in `Element` the element to cut for the `Split` hybrid shape feature.

```VBScript
     Dim Element As Reference
     Set Element = Split.ElemToCut

```

### Property **IntersectionComputation**( ) As boolean

   Gets or sets Intersection computation mode. IntersectionComputation = TRUE : Intersection is computed. = FALSE : Intersection is not computed. This example retrieves in `Intersection` the Intersection computation mode for the `Split` hybrid shape feature.

```VBScript
     Dim Intersection As boolean
     Intersection = Split.IntersectionComputation

```

### Property **Orientation**( ) As long

   Returns or sets the orientation used to compute the split. **Role** :
Orientation specifies kept parts of cut feature.

When splitting a surface by a surface :
\- If orientation value is 1: kept parts are specified by the "natural" normal to the cutting feature
\- If orientation value -1: kept parts are specified by the inverse of the "natural" normal to the cutting feature

When splitting a surface by a curve :
\- If orientation value is 1: kept parts are specified by the result of the cross product : normal(surface)^tangent(curve)
\- If orientation value is -1: Kept parts are specified by the inverse of the result of the cross product : normal(surface)^tangent(curve)

When splitting a curve by a point or a curve (without support specified) :
\- If orientation value is 1: Kept parts are from beginning of the curve to the first intersection,
and, if there is one, from the second to the third intersection and so on until the end of the curve.
\- If orientation value is -1: Kept parts are from the first intersection to the second (if there is one),
and, if there is one, from the third to the fourth and so on until the end of the curve.

When splitting a curve on support:
\- If orientation value is 1: Kept parts are specified by the result of the cross product : normal(support surface)^tangent(cutting curve)
\- If orientation value is -1: Kept parts are specified by the inverse of the result of the cross product : normal(support surface)^tangent(cutting curve)

When splitting a curve by a surface:
\- If orientation value is 1: Kept parts are specified by the inverse of the normal to the surface
\- If orientation value is -1: Kept parts are specified by the normal to the surface

**Example**      This example retrieves in `OrientValue` the orientation value for the `Split` hybrid shape feature.

```VBScript
     Dim OrientValue As long
     Set OrientValue = Split.Orientation

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support element.
This support element may not exist.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `Element` the support element for the `Split` hybrid shape feature.

```VBScript
     Dim Element As Reference
     Set Element = Split.Support

```

### Property **VolumeResult**( ) As long

   Returns or sets the Result Type.
Result type:

  * : 0 -> Surface
  * : 1 -> Volume
, The resultant split will be volume. If input is element to cut is volume.

Note: Setting volume result requires GSO License.

**Example** : This example retrieves in `ResultType` the result type for the `Split` hybrid shape feature.

```VBScript
     Dim RType As long
     Set RType = Split.ResultType

```

Methods

### Sub **AddCuttingElem**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`,  long  `iOrientation`)

   Adds a cutting feature.

**Parameters:**

` iElem`      cutting feature
` iOrientation`      Orientation iOrientation = 1 : SameOrientation = -1 : InvertOrientation = 2 : KoOrientation

### Sub **AddElementToKeep**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

   Adds an element to specifications. This element will be kept.

**Parameters:**

` iElement`      Element to keep.

### Sub **AddElementToRemove**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

   Adds an element to specifications. This element will be removed.

**Parameters:**

` iElement`      Element to remove.

### Func **GetCuttingElem**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets the cutting feature at a given index (a point, a curve or a surface).

**Parameters:**

` oElem`      cutting feature
` iRank`      Index of one of the cutting features

### Func **GetIntersection**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets the intersection at a given index.

**Parameters:**

` oElem`      Intersection
` iRank`      Index of one of the intersection features

### Func **GetKeptElem**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets the kept feature at a given index.

**Parameters:**

` oElem`      Kept feature
` iRank`      Index of one of the kept features

### Func **GetNbCuttingElem**( ) As long

   Gets the number of cutting features.

**Parameters:**

` oNbCuttingElem`      Number of cutting features

### Func **GetNbElementsToKeep**( ) As long

   Gets the number of elements to keep.

**Parameters:**

` oNbElementsToKeep`      Number of elements to keep

### Func **GetNbElementsToRemove**( ) As long

   Gets the number of elements to remove.

**Parameters:**

` oNbElementsToRemove`      Number of elements to remove

### Func **GetOrientation**( long  `iRank`) As long

   Gets Orientation used to compute the split.

**Parameters:**

` oOrientation`      Orientation
` iRank`      index of the cutting feature oOrientation = 1 : SameOrientation = -1 : InvertOrientation = 2 : KoOrientation

### Func **GetOtherSide**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets the other side.

**Parameters:**

` oElem`      Other side

### Func **GetRemovedElem**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets the removed feature at a given index.

**Parameters:**

` oElem`      Removed feature
` iRank`      Index of one of the removed features

### Sub **InvertOrientation**( )

   Inverts the orientation used to compute the split.  
### Sub **RemoveCuttingElem**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`)

   Removes a cutting feature.

**Parameters:**

` iElem`      cutting feature

### Sub **RemoveElementToKeep**( long  `iRank`)

   Removes an element from specifications.

**Parameters:**

` iRank`      Index of the kept element.

### Sub **RemoveElementToRemove**( long  `iRank`)

   Removes an element from specifications.

**Parameters:**

` iRank`      Index of the removed element.

### Sub **SetOrientation**( long  `iRank`,  long  `iOrientation`)

   Sets the orientation used to compute the split.

**Parameters:**

` iOrientation`      Orientation
` iRank`      index of the cutting feature iOrientation = 1 : SameOrientation = -1 : InvertOrientation = 2 : KoOrientation