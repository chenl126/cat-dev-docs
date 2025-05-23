# HybridShapeAxisLine (Object)

**_Represents the hybrid shape axis line feature object._**

**Role** : To access the data of the hybrid shape axis line feature object. This data includes:

  * The element used to compute the axis
  * The direction used in orientation of axis
  * AxisLineType to change the axis type

Use the CATIAHybridShapeFactory to create a HybridShapeAxisLine object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **AxisLineType**(| ) As long

   Returns or sets the axis line type.

**Legal values** :

1
    This option creates Axis along major axis if element is ellipse or oblong, Axis is aligned with direction specified if input is circle and coincides with revolution axis if element is revolution surface
2
    This option creates Axis along minor axis if element is ellipse or oblong, Axis is normal to direction specified if input is circle
3
    This option creates Axis normal to the element if it is circle, ellipse or oblong

**Example** :      This example retrieves in `oType` the axis line type for the `AxisLine` hybrid shape feature.

```VBScript
     Dim oType
     Set oType = AxisLine.AxisLineType

```

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Gets the reference direction used in computation of axis.
This is useful only if the element selected is circle, arc or sphere. If the element is circle or arc Axis may be normal to reference direction or aligned with reference direction

**Example** :      This example retrieves in `oDir` the direction for the `AxisLine` hybrid shape feature.

```VBScript
     Dim oDir As CATIAHybridShapeDirection
     Set oDir = AxisLine.Direction

```

### Property **Element**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element from which axis is computed.

**Example** :      This example retrieves in `Element` the element from which axis is computed for the `AxisLine` hybrid shape feature.

```VBScript
     Dim Element As Reference
     Set Element = AxisLine.Element

```