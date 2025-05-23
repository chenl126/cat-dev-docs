# HybridShapePlaneTangent (Object)

**_Tangency plane._**

**Role** : Allows to access data of the the plane feature tangent to a surface at a given point.

## Properties

### Property **Point**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   **Role** : Get the tangency point.

**Parameters:**

` oPoint`      tangency point.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Surface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   **Role** : Get the surface to which the plane is to be tangent.

**Parameters:**

` oSurface`      reference surface.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)