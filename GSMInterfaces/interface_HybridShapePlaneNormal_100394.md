# HybridShapePlaneNormal (Object)

**_Normal plane._**
**Role** : Allows to access data of the plane feature normal to a curve at a given point.

## Properties

### Property **Curve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : Get the curve to which the plane is to be normal.

**Parameters:**

` oCurve`      reference curve.
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Point**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : Get the point where the plane is to be normal.

**Parameters:**

` oPoint`      point
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)