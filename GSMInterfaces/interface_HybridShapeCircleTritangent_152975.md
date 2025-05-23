# HybridShapeCircleTritangent (Object)

**_Represents the hybrid shape circle object tangent to three curves._**

**Role** : To access the data of the hybrid shape circle object.

This data includes:

  * The three curves to which the circle is tangent
  * The surface that supports the circle
  * The orientation of each curve

Use the CATIAHybridShapeFactory to create a HybridShapeCircleTritangent object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **BeginOfCircle**(| ) As long

   Return or Set the number of the beginning curve of the circle. This parameter is used to stabilize the resulting circle

**Example:**      This example set the beginning wire index of the `hybShpcircle` hybrid shape circle

```VBScript
     hybShpcircle.BeginOfCircle = 1

```

### Property **Curve1**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first curve to which the circle is or will be tangent.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example retrieves in `HybShpCircleFirstCurve` the first curve to which the `HybShpCircle` hybrid shape circle is tangent.

```VBScript
     Dim HybShpCircleFirstCurve As Reference
     HybShpCircleFirstCurve = HybShpCircle.Curve1

```

### Property **Curve2**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the second curve to which the circle is or will be tangent.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example sets the second curve to which the `HybShpCircle` hybrid shape circle will be tangent to Crv5.

```VBScript
     HybShpCircle.Curve2 Crv5

```

### Property **Curve3**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the thirs curve to which the circle is or will be tangent.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example retrieves in `HybShpCircleThirsCurve` the third curve to which the `HybShpCircle` hybrid shape circle is tangent.

```VBScript
     Dim HybShpCircleThirdCurve As Reference
     HybShpCircleThirdCurve = HybShpCircle.Curve3

```

### Property **DiscriminationIndex**( ) As long

   Return or set the discrimination index of the current circle. Several resulting solutions produced by the operator can be same oriented regarding to the input wire bodies. In such a case, they are sorted in order to distinguish them. The Sequence FirstOrientation - SecondOrientation - DiscriminationIndex allows you to identifie a unique one-domain solution.

**Example:**      This example set the discrimination index of the `hybShpcircle` hybrid shape circle

```VBScript
     hybShpcircle.DiscriminationIndex = 2

```

### Property **Orientation1**( ) As long

   Returns or sets the orientation of the first curve to which the circle is tangent.

**Role** : The orientation of the first curve determines the side of this curve taken into account to find the point where the circle is tangent to the curve. This side is determined by the cross product of the normal to the support and a tangent to the curve oriented using the curve orientation.

**Legal values** : 1 to state that the side of the curve to be taken into account is the side shown by the vector resulting from this cross product, and -1 otherwise.

**Example** :      This example sets the orientation of the first curve to which the `HybShpCircle` hybrid shape circle is tangent to reverse.

```VBScript
     HybShpCircle.Orientation1 -1

```

### Property **Orientation2**( ) As long

   Returns or sets the orientation of the second curve to which the circle is tangent.

**Role** : The orientation of the second curve determines the side of this curve taken into account to find the point where the circle is tangent to the curve. This side is determined by the cross product of the normal to the support and a tangent to the curve oriented using the curve orientation.

**Legal values** : 1 to state that the side of the curve to be taken into account is the side shown by the vector resulting from this cross product, and -1 otherwise.

**Example** :      This example retrieves in `HybShpCircleOrientation` the orientation of the second curve to which the `HybShpCircle` hybrid shape circle is tangent.

```VBScript
     HybShpCircleOrientation = HybShpCircle.Orientation2

```

### Property **Orientation3**( ) As long

   Returns or sets the orientation of the third curve to which the circle is tangent.

**Role** : The orientation of the third curve determines the side of this curve taken into account to find the point where the circle is tangent to the curve. This side is determined by the cross product of the normal to the support and a tangent to the curve oriented using the curve orientation.

**Legal values** : 1 to state that the side of the curve to be taken into account is the side shown by the vector resulting from this cross product, and -1 otherwise.

**Example** :      This example sets the orientation of the third curve to which the `HybShpCircle` hybrid shape circle is tangent to reverse.

```VBScript
     HybShpCircle.Orientation3 -1

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle support surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `HybShpCircleSupportSurf` the support surface of the `HybShpCircle` hybrid shape circle.

```VBScript
     Dim HybShpCircleSupportSurf As Reference
     HybShpCircleSupportSurf = HybShpCircle.Support

```

### Property **TangentOrientation1**( ) As long

   Returns or sets the tangent orientation of the circle first reference element. compared to the circle itself

**Example:**      This example retrieves the tangent orientation of first reference element of the `hybShpcircle` hybrid shape circle in `firstOrient`.

```VBScript
     Dim firstOrient As long
     firstOrient = hybShpcircle.FirstTangentOrientation

```

### Property **TangentOrientation2**( ) As long

   Returns or sets the tangent orientation of the circle second reference element. compared to the corner itself

**Example:**      This example retrieves the tangent orientation of second reference element of the `hybShpcircle` hybrid shape circle in `secondOrient`.

```VBScript
     Dim secondOrient As long
     secondOrient = hybShpcircle.SecondTangentOrientation

```

### Property **TangentOrientation3**( ) As long

   Returns or sets the tangent orientation of the circle third reference element. compared to the corner itself

**Example:**      This example retrieves the tangent orientation of third reference element of the `hybShpcircle` hybrid shape circle in `thirdOrient`.

```VBScript
     Dim thirdOrient As long
     thirdOrient = hybShpcircle.ThirdTangentOrientation

```

### Property **TrimMode**( ) As long

   Returns or sets whether the circle reference curves are or should be trimmed.

**Legal values** : **0** if the circle reference curves are not or should not be trimmed, **1** if the circle reference curves are or should be trimmed, **2** if only the first circle reference curve is or should be trimmed, **3** if only the second circle reference curve is or should be trimmed,

**Example:**      This example sets that the reference curves of the `hybShpCircle` hybrid shape circle should be trimmed.

```VBScript
     hybShpCircle.TrimMode = 1

```