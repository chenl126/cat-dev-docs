# BooleanShape (Object)

**_Represents the shapes based on boolean operations on other shapes._**
It is the base object for add, assemble, intersect, remove, and split shapes.

**See also:**      [Add](../PartInterfaces/interface_Add_1925.md), [Assemble](../PartInterfaces/interface_Assemble_13978.md), [Intersect](../PartInterfaces/interface_Intersect_18201.md), [Remove](../PartInterfaces/interface_Remove_8234.md), [Split](../PartInterfaces/interface_Split_5882.md), [Trim](../PartInterfaces/interface_Trim_3774.md)

## Properties

### Property **Body**( ) As [CATIABody](../MecModInterfaces/interface_Body_3736.md) (Read Only)

Returns the inserted body.  Methods

### Sub **SetOperatedObject**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReferenceObject`)

Modifies the Second Operand. input object to replace with Body or Volume  
### Sub **SetOperatingVolume**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReferenceObject`)

Swaps the operands. Both the Operands must be Volume. This is available only for Volume Add and Volume UnionTrim Operations