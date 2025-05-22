# HybridShapeSphere (Object)

**_Represents the hybrid shape sphere feature object._**
**Role** : To access the data of the hybrid shape sphere explicit feature object.
The Sphere feature : a Sphere is made up of 4 angles parameters.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Axis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets axis on the object.

**Parameters:**

` oDir`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **BeginMeridianAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns BeginMeridianAngle on the object.

**Parameters:**

` oAngle`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **BeginParallelAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns BeginParallelAngle on the object.

**Parameters:**

` oAngle`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Center**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sphere center.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `HybShpSphereCenter` the center of the `HybShpSphere` hybrid shape sphere.

```VBScript
Dim HybShpSphereCenter As Reference
HybShpSphereCenter = HybShpSphere.Center

```

### Property **EndMeridianAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns EndMeridianAngle on the object.

**Parameters:**

` oAngle`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **EndParallelAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns EndParallelAngle on the object.

**Parameters:**

` oAngle`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Limitation**( long  `iLimitationType`)

Returns whether the sphere is created as a whole sphere or not.
**Legal values** : 0 for a sphere with angles and 1 for a whole sphere.

**Example:**      
### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

**Role** : Get sphere radius.

**Parameters:**

` oRadius`      Sphere radius return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) Methods

### Sub **SetBeginMeridianAngle**( double  `iAngle`)

Sets BeginMeridianAngle on the object.

**Parameters:**

` iAngle`
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetBeginParallelAngle**( double  `iAngle`)

Sets BeginParallelAngle on the object.

**Parameters:**

` iAngle`
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetEndMeridianAngle**( double  `iAngle`)

Sets EndMeridianAngle on the object.

**Parameters:**

` iAngle`
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetEndParallelAngle**( double  `iAngle`)

Sets EndParallelAngle on the object.

**Parameters:**

` iAngle`
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetRadius**( double  `iRadius`)

Sets Radius on the object.

**Parameters:**

` iAngle`
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)