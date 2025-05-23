# HybridShapePlane2Lines (Object)

**_plane defined by two lines._**

**Role** : Allows to access data of the plane feature passing though two lines.

## Properties

### Property **First**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   **Role** : Get the first line.

**Parameters:**

` oLine1`      first line.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **ForbidNonCoplanarLines**( boolean  `iCoplanarLines`)

   if ForbidNonCoplanarLines = TRUE, both lines have to be on the same plane. if ForbidNonCoplanarLines = FALSE, both lines can be non coplanar.  
### Property **Second**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   **Role** : Get the second line.

**Parameters:**

` oLine2`      second line.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)