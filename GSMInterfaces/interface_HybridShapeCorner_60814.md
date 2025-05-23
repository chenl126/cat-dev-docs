# HybridShapeCorner (Object)

**_Represents the hybrid shape corner feature._**

**Role** : To access the data of the hybrid shape corner object. This data includes:

  * Two elements
  * Their orientations (same or inverse than the underlying curve)
  * A support for the hybrid shape corner on support feature
  * A direction for the hybrid shape 3D corner feature
  * A radius.

Use the [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) to create a HybridShapeCorner object.

## Properties

### Property **BeginOfCorner**(| ) As long

   Return or Set the number of the beginning curve of the corner. This parameter is used to stabilize the resulting corner

**Example:**      This example set the beginning wire index of the `hybShpCorner` hybrid shape corner

```VBScript
     hybShpCorner.BeginOfCorner = 1

```

### Property **CornerType**( ) As long

   Returns or sets the Corner Type.

**Example:**      This example retrieves the Corner Type the `hybShpCorner` hybrid shape corner in `CornerType`.

```VBScript
     Dim lCornerType As long
     lCornerType = hybShpCorner.CornerType

```

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the 3D corner direction.

**Legal values** : This can be a CATIAHybridShapeDirection.

**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) **Example:**      This example sets the direction of the `hybShpCorner` hybrid shape 3D corner as the existing direction `hybShpDirection`.

```VBScript
     hybShpCorner.Direction = hybShpDirection

```

### Property **DiscriminationIndex**( ) As long

   Returns or set the discrimination index of the current corner. Several resulting solutions produced by the operator can be same oriented regarding to the input wire bodies. In such a case, they are sorted in order to distinguish them. The Sequence FirstOrientation - SecondOrientation - DiscriminationIndex allows you to identifie a unique one-domain solution.

**Example:**      This example set the discrimination index of the `hybShpCorner` hybrid shape corner

```VBScript
     hybShpCorner.DiscriminationIndex = 2

```

### Property **FirstElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the corner first reference element.

**Legal values** : This can be a curve or a point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example:**      This example retrieves the first reference element of the `hybShpCorner` hybrid shape corner in `firstElt`.

```VBScript
     Dim fisrtElt As CATIAReference
     fisrtElt = hybShpCorner.FirstElem

```

### Property **FirstOrientation**( ) As long

   Returns or sets the orientation of the corner first reference element. The orientation specifies the corner center position. It is either the same of the inverse orientation than those of the cross product: Normal(Support) ^ Tangent(FirstElem)

**Legal values** : 1 if the orientation of the corner first reference element is the same than the cross product: Normal(Support) ^ Tangent(FirstElem), and -1 if it is the inverse.

**Example:**      This example retrieves the orientation of first reference element of the `hybShpCorner` hybrid shape corner in `firstOrient`.

```VBScript
     Dim firstOrient As long
     firstOrient = hybShpCorner.FirstOrientation

```

### Property **FirstTangentOrientation**( ) As long

   Returns or sets the tangent orientation of the corner first reference element. compared to the corner itself

**Example:**      This example retrieves the tangent orientation of first reference element of the `hybShpCorner` hybrid shape corner in `firstOrient`.

```VBScript
     Dim firstOrient As long
     firstOrient = hybShpCorner.FirstTangentOrientation

```

### Property **OnVertex**( ) As boolean

   Returns or sets the On Vertex mode off/on.

**Example:**      This example retrieves the OnVertex the `hybShpCorner` hybrid shape corner in `OnVertex`.

```VBScript
     Dim bOnVertex As boolean
     bOnVertex = hybShpCorner.OnVertex

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the corner radius.

**Example:**      This example retrieves the radius of the `hybShpCorner` hybrid shape corner in `radius`.

```VBScript
     Dim radius As CATIALength
     radius = hybShpCorner.Radius

```

### Property **SecondElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the corner second reference element.

**Legal values** : This is always a curve.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example:**      This example retrieves the second reference element of the `hybShpCorner` hybrid shape corner in `secondElt`.

```VBScript
     Dim secondElt As CATIAReference
     secondElt = hybShpCorner.SecondElem

```

### Property **SecondOrientation**( ) As long

   Returns or sets the orientation of the corner second reference element. The orientation specifies the corner center position. It is either the same of the inverse orientation than those of the cross product: Normal(Support) ^ Tangent(SecondElem)

**Legal values** : 1 if the orientation of the corner second reference element is the same than the cross product: Normal(Support) ^ Tangent(SecondElem), and -1 if it is the inverse.

**Example:**      This example sets the orientation of second reference element of the `hybShpCorner` hybrid shape corner to the inverse of the cross porduct Normal(Support) ^ Tangent(SecondElem).

```VBScript
     hybShpCorner.SecondOrientation = -1

```

### Property **SecondTangentOrientation**( ) As long

   Returns or sets the tangent orientation of the corner second reference element. compared to the corner itself

**Example:**      This example retrieves the tangent orientation of second reference element of the `hybShpCorner` hybrid shape corner in `secondOrient`.

```VBScript
     Dim secondOrient As long
     firstOrient = hybShpCorner.SecondTangentOrientation

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the corner support.

**Legal values** : This can be a plane or a surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example:**      This example sets the support of the `hybShpCorner` hybrid shape corner as the exisiting surgace `supportSurf`.

```VBScript
     hybShpCorner.Support = supportSurf

```

### Property **Trim**( ) As boolean

   Returns or sets whether the corner reference curves are or should be trimmed.

**Legal values** : **True** if the corner reference curves are or should be trimmed, and False otherwise.

**Example:**      This example sets that the corner reference curves of the `hybShpCorner` hybrid shape corner should be trimmed.

```VBScript
     hybShpCorner.Trim = True

```

### Property **TrimMode**( ) As long

   Returns or sets whether the corner reference curves are or should be trimmed.

**Legal values** : **1** if the corner reference curves are or should be trimmed, **0** if the corner reference curves are not or should not be trimmed, **2** if only the first corner reference curve is or should be trimmed, **3** if only the second corner reference curve is or should be trimmed,

**Example:**      This example sets that the corner reference curves of the `hybShpCorner` hybrid shape corner should be trimmed.

```VBScript
     hybShpCorner.TrimMode = 1

```

Methods

### Sub **InvertFirstOrientation**( )

   Inverts the first reference element orientation used to compute the corner.

**Example:**      This example inverts the first corner reference element orientation of the `hybShpCorner`.

```VBScript
     hybShpCorner.InvertFirstOrientation

```

### Sub **InvertSecondOrientation**( )

   Inverts the second reference element orientation used to compute the corner.

**Example:**      This example inverts the second corner reference element orientation of the `hybShpCorner`.

```VBScript
     hybShpCorner.InvertSecondOrientation

```