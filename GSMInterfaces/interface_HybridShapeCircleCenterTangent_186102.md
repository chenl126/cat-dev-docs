# HybridShapeCircleCenterTangent (Object)

**_Represents the hybrid shape circle object defined using a center, a curve and a support._**

**Role** : To access the data of the hybrid shape circle tangent object.

This data includes:

  * The center element
  * The tangent curve
  * The support
  * The value of the raduius
  * and also the type of solution index

Use the CATIAHybridShapeFactory to create a HybridShapeCircleCenterTangent object.

**See also:**      [HybridShapeFactory.AddNewCircleCenterTangent](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewCircleCenterTangent)

## Properties

### Property **BeginOfCircle**(| ) As long

   Return or Set the number of the beginning curve of the circle. This parameter is used to stabilize the resulting circle

**Example:**      This example set the beginning wire index of the `hybShpcircle` hybrid shape circle

```VBScript
     hybShpcircle.BeginOfCircle = 1

```

### Property **CenterElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the Center Element of the circle.

**Example** :      This example retrieves in `HybShpCircleCenterCurve` the first curve to which the `HybShpCircle` hybrid shape circle is Center curve.

```VBScript
     Dim HybShpCircleFirstCurve As Reference
     HybShpCircleFirstCurve = HybShpCircle.CenterElem

```

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle diameter. It is expressed as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to True.  **Example** :      This example retrieves in `HybShpCircleDiameter` the diameter of the `HybShpCircle` hybrid shape circle feature

```VBScript
     Dim HybShpCircleDiameter As Length
     HybShpCircleDiameter = HybShpCircle.Diameter

```

### Property **DiameterMode**( ) As boolean

   Returns or sets the DiameterMode.

**Legal values** : **True** implies diameter **False** implies radius (default). When DiameterMode is changed, Radius/Diameter value, which is stored will not be modified.

**Example:**      This example sets that the DiameterMode of the `HybShpCircle` hybrid shape circle feature

```VBScript
      HybShpCircle.DiameterMode = True

```

### Property **DiscriminationIndex**( ) As long

   Return or set the discrimination index of the current circle. Several resulting solutions produced by the operator can be same oriented regarding to the input wire bodies. In such a case, they are sorted in order to distinguish them. The Sequence FirstOrientation - SecondOrientation - DiscriminationIndex allows you to identifie a unique one-domain solution.

**Example:**      This example set the discrimination index of the `hybShpcircle` hybrid shape circle

```VBScript
     hybShpcircle.DiscriminationIndex = 2

```

### Property **Orientation1**( ) As long

   Returns or sets the orientation of the first curve to which the circle is tangent.

**Role** : The orientation of the first curve determines the side of this curve taken into account to find the point where the circle is tangent to the curve.

**Legal values** : To be provided by Claire (1/-1??)

**Example** :      This example sets the orientation of the first curve to which the `HybShpCircle` hybrid shape circle is tangent to reverse.

```VBScript
     Set HybShpCircle.Orientation1 -1

```

### Property **Orientation2**( ) As long

   Returns or sets the orientation of the second curve to which the circle is tangent.

**Role** : The orientation of the second curve determines the side of this curve taken into account to find the point where the circle is tangent to the curve.

**Legal values** : To be provided by Claire (1/-1??)

**Example** :      This example retrieves in `HybShpCircleOrientation` the orientation of the second curve to which the `HybShpCircle` hybrid shape circle is tangent.

```VBScript
     HybShpCircleOrientation = HybShpCircle.Orientation2

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle radius. It is expressed as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to False.  **Example** :      This example retrieves in `HybShpCircleRadius` the radius of the `HybShpCircle` hybrid shape circle.

```VBScript
     Dim HybShpCircleRadius As Length
     HybShpCircleRadius = HybShpCircle.Radius

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle support surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `HybShpCircleSupportSurf` the support surface of the `HybShpCircle` hybrid shape circle.

```VBScript
     Dim HybShpCircleSupportSurf As Reference
     Set HybShpCircleSupportSurf = HybShpCircle.Support

```

### Property **TangentCurve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the tangent curve to which the circle will be tangent.

**Example** :      This example sets the tangent curve to which the `HybShpCircle` hybrid shape circle will be tangent to TgtCrv.

```VBScript
     Set HybShpCircle.Tangent Curve TgtCrv

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