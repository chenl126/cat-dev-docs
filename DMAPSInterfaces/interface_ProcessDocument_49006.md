# ProcessDocument (Object)

**_This interface is used to access the PPRDocument and to add a new library._**

## Properties

### Property **PPRDocument**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md) (Read Only)

Retrieves the interface which manages the PPRDocument.

**Returns:**      The PPRDocument corresponding to the current Process document.  Methods

### Sub **AddLibrary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`)

Adds a new library to the current Process document.

**Parameters:**

` iFileName`      The name of the library to be added.