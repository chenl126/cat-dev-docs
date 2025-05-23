# HybridShapePlaneEquation (Object)

**_Plane define by an equation plane._**

**Role** : Allows to access data of the plane feature created by its cartesian equation. Plane equation is Ax+By+Cz = D.

## Properties

### Property **A**(| ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Gets A coefficient for plane equation.

**Parameters:**

` oA`      A Coefficient of cartesian plane

**See also:**      [RealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **B**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Gets B coefficient for plane equation.

**Parameters:**

` oB`      B Coefficient of cartesian plane

**See also:**      [RealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **C**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Gets C coefficient for plane equation.

**Parameters:**

` oC`      C Coefficient of cartesian plane return value for CATScript applications, with (IDLRETVAL) function type

**See also:**      [RealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **D**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Gets D coefficient for plane equation.

**Parameters:**

` oD`      D Coefficient of cartesian plane

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **RefAxisSystem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the reference Axis System for PlaneEquation feature.
This data is not mandatory, if element is null, the absolute axis system is taken.
When an element is given, X, Y and Z are considered in this Axis system.
If reference point is not specified, X,Y and Z are measured from origin of this axis system.

Example
:      This example retrieves in `oRefAxis` the reference Axis System for `PlaneEquation` feature.

```VBScript
     Dim oRefAxis As CATIAReference
     Set oRefAxis  = PlaneEquation.RefAxisSystem

```

Methods

### Func **GetReferencePoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets the reference point.

**Parameters:**

` oReferencePoint`      reference point

### Sub **SetReferencePoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReferencePoint`)

   Sets the reference point.

**Parameters:**

` iReferencePoint`      reference point