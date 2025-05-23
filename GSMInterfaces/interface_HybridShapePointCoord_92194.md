# HybridShapePointCoord (Object)

**_Point defined by coordinates._**

**Role** : To access data of the point feature created with its cartesian coordinates.

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **PtRef**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the reference point for PointCoord feature.
This data is not mandatory, if element is null, the origin point is taken.
When an element is given, X, Y and Z are measured starting from this point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

Example
:      This example retrieves in `oPtRef` the reference point for `PointCoord` feature.

```VBScript
     Dim oPtRef As CATIAReference
     Set oPtRef  = PointCoord.PtRef

```

### Property **RefAxisSystem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the reference Axis System for PointCoord feature.
This data is not mandatory, if element is null, the absolute axis system is taken.
When an element is given, X, Y and Z are considered in this Axis system.
If reference point is not specified, X,Y and Z are measured from origin of this axis system. *

Example
:      This example retrieves in `oRefAxis` the reference Axis System for `PointCoord` feature.

```VBScript
     Dim oRefAxis As CATIAReference
     Set oRefAxis  = PointCoord.RefAxisSystem

```

### Property **X**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns X coordinate of the point.

Example
:      This example retrieves in `oX` the X coordinate for the `PointCoord` hybrid shape feature.

```VBScript
     Dim oX As CATIALength
     Set oX = PointCoord.X

```

### Property **Y**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns Y coordinate of the point.

Example
:      This example retrieves in `oY` the Y coordinate for the `PointCoord` hybrid shape feature.

```VBScript
     Dim oY As CATIALength
     Set oY = PointCoord.Y

```

### Property **Z**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns Z coordinate of the point.

Example
:      This example retrieves in `oZ` the Z coordinate for the `PointCoord` hybrid shape feature.

```VBScript
     Dim oZ As CATIALength
     Set oZ = PointCoord.Z

```