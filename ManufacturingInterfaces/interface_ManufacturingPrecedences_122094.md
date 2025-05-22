# ManufacturingPrecedences (Collection)

**_Interface that manage the precedences for an object of type @ CATIAManufacturingActivity._**
If an object A has objects B and C as precedence constraints, it means that B and C have to be performed before A.

## Methods

### Sub **AddOperation**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iObject`,  [CatManufacturingPrecedenceType](../ManufacturingInterfaces/enum_CatManufacturingPrecedenceType_188280.md)  `iType`)

Adds a new precedence in the collection of precedences. The type of added object is a CATIAManufacturingActivity.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAManufacturingPrecedence](../ManufacturingInterfaces/interface_ManufacturingPrecedence_111444.md)

Returns a precedence object from the precedence collection.  
### Sub **Remove**( long  `iIndex`)

Removes an object from the precedences collection. The removed precedence will be deleted, but not the referenced object attach to this precedence.  
### Sub **RemoveAll**( )

Removes all objects from the precedences collection.