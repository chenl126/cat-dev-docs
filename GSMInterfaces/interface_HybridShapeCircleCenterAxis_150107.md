# HybridShapeCircleCenterAxis (Object)

**_Represents the hybrid shape circle object defined using a point and axis/line._**

**Role** : To access the data of the hybrid shape circle center axis object.

This data includes:

  * Point
  * Axis/Line
  * Value of radius/diameter
  * Diameter Mode
  * Projection Mode

Use the CATIAHybridShapeFactory to create a HybridShapeCircleCenterAxis object.

**See also:**      [HybridShapeFactory.AddNewCircleCenterAxis](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewCircleCenterAxis)

## Properties

### Property **Axis**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the Axis of the circle.

**Example** :      This example retrieves in `CircleAxis` the Axis of plane in which circle is lying from `HybShpCircle` hybrid shape circle center axis feature

```VBScript
     Dim CircleAxis As Reference
     Set CircleAxis = HybShpCircle.Axis

```

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle diameter. It is expressed as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to True.  **Example** :      This example retrieves in `HybShpCircleDiameter` the diameter of the `HybShpCircle` hybrid shape circle center axis feature

```VBScript
     Dim HybShpCircleDiameter As Length
     HybShpCircleDiameter = HybShpCircle.Diameter

```

### Property **DiameterMode**( ) As boolean

   Returns or sets the DiameterMode.

**Legal values** : **True** implies diameter **False** implies radius (default). When DiameterMode is changed, Radius/Diameter value, which is stored will not be modified.

**Example:**      This example sets that the DiameterMode of the `HybShpCircle` hybrid shape circle center axis feature

```VBScript
      HybShpCircle.DiameterMode = True

```

### Property **Point**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the Point of the circle.

**Example** :      This example retrieves in `CirclePoint` the point used for center computation from `HybShpCircle` hybrid shape circle center axis feature

```VBScript
     Dim CirclePoint As Reference
     Set CirclePoint = HybShpCircle.Point

```

### Property **ProjectionMode**( ) As boolean

   Returns or sets the ProjectionMode.

**Legal values** : **True** (default) implies point will be projected on to axis/line **False** implies that point will be center of the circle.

**Example:**      This example sets that the ProjectionMode of the `HybShpCircle` hybrid shape circle center axis feature

```VBScript
      HybShpCircle.ProjectionMode = True

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle radius. It is expressed as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to False.  **Example** :      This example retrieves in `HybShpCircleRadius` the radius of the `HybShpCircle` hybrid shape circle center axis feature

```VBScript
     Dim HybShpCircleRadius As Length
     HybShpCircleRadius = HybShpCircle.Radius

```