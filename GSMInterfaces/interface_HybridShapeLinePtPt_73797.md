# HybridShapeLinePtPt (Object)

**_Represents the hybrid shape line between two points feature object._**

**Role** : To access the data of the line feature created between two points.

Use the CATIAHybridShapeFactory to create a HybridShapeLinePtPt object.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **BeginOffset**(| ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the start length of the line.
Start length : extension of the line, beginning at the starting point

**Example** :      This example retrieves in `oStart` the beginning offset length for the `LinePtPt` hybrid shape feature.

```VBScript
     Dim oStart As  CATIALength
     Set oStart = LinePtPt.BeginOffset

```

### Property **EndOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the end length of the line.
End length : extension of the line, beginning at the ending point

**Example** :      This example retrieves in `oEnd` the starting length for the `LinePtPt` hybrid shape feature.

```VBScript
     Dim oEnd As  CATIALength
     Set oEnd = LinePtPt.EndOffset

```

### Property **PtExtremity**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the extremity point of the LinePtPt(Second Point).
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `oPtExtremity` the ending point for the `LinePtPt` hybrid shape feature.

```VBScript
     Dim oPtExtremity As Reference
     Set oPtExtremity = LinePtPt.PtExtremity

```

### Property **PtOrigine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the origin point of the LinePtPt(First point).
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `oPtOrigine` the initial point for the `LinePtPt` hybrid shape feature.

```VBScript
     Dim oPtOrigine As Reference
     Set oPtOrigine = LinePtPt.PtOrigine

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the supporting surface.
Note: the support surface is not mandatory for LinePtPt

Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `oSurface` the supporting surface (if it exist) for the `LinePtPt` hybrid shape feature.

```VBScript
     Dim oSurface As Reference
     Set oSurface = LinePtPt.Surface

```

Methods

### Func **GetLengthType**( ) As long

   Gets the length type Default is 0.

**Parameters:**

` oType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point

### Func **GetSymmetricalExtension**( ) As boolean

   Gets whether the symmetrical extension of the line is active.

**Parameters:**

` oSym`      Symetry flag

### Sub **RemoveSupport**( )

   Removes the support surface.  
### Sub **SetLengthType**( long  `iType`)

   Sets the length type Default is 0.

**Parameters:**

` iType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point

### Sub **SetSymmetricalExtension**( boolean  `iSym`)

   Sets the symmetrical extension of the line (start = -end).

**Parameters:**

` iSym`      Symetry flag