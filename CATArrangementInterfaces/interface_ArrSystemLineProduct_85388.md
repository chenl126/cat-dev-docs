# ArrSystemLineProduct (Object)

**_The interface to access a CATIAArrSystemLineProduct

Using this prefered syntax will enable mkdoc to document your class._**

## Methods

### Func **GetSubItem**( long  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

Allows the user to get the item at a specific index location.  
### Func **GetSubProductsCount**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIntfId`) As long

Returns the count of the sub-products that make up the System-Line Arrangement Product and that match a specifc interface id. If the interface Id is NULL, then it searches for CATIAProduct objects by default.