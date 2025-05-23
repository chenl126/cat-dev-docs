# HybridShapeInverse (Object)

**_The Inverse feature : an Inverse is made up of a face to process and one Inverse parameter._**

## Properties

### Property **Element**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   **Role** : To get the element inverted.

**Parameters:**

` oElem`      Element inverted return value for CATScript applications, with (IDLRETVAL) function type

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Orientation**( ) As long

   Gets or sets the element's orientation. Orientation = 1 : the element is not inverted. = -1 : the element is inverted, = 2 : the element can not be inverted. Orientation can not be set to 2.