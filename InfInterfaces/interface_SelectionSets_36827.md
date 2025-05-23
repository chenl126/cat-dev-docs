# SelectionSets (Object)

**_Interface to manage the Selection Sets in a document._**

## Methods

### Sub **AddCSOIntoSelectionSet**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iSelSetName`)

   Adds CSO's content in a Selection Set.

**Parameters:**

` iSelSetName`      The name of the Selection Set in wich the CSO has to be added.

**Returns:**      The error code of function :

  * S_OK if the content of the CSO is added
  * E_FAIL if the content of the CSO is not added

### Sub **CreateSelectionSet**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSelSetName`)

   Creates a new Selection Set.

**Role:** This method creates a new Selection Set.

**Parameters:**

` iSelSetName`      The name of Selection Set to create.

**Returns:**      The error code of function :

  * S_OK if the Selection Set is created
  * E_FAIL if a problem occurred

### Sub **DeleteSelectionSet**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSelSetName`)

   Deletes a Selection Set.

**Role:** This method removes a Selection Set and all its content.

**Parameters:**

` iSelSetName`      The Selection Set to delete.

**Returns:**      The error code of function :

  * S_OK if the method succeeded
  * E_FAIL if a problem occurred

### Sub **GetListOfSelectionSet**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfSelectionSet`)

   Retrieves the list of Selection Sets in the document.

**Parameters:**

` oListOfSelectionSet`      The list of Selection Sets in the document

**Returns:**      The error code of function :

  * S_OK if the method succeeded
  * E_FAIL if an error occurred

### Sub **PutSelectionSetIntoCSO**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSelSetName`)

   Puts Selection Set's content in the CSO.

**Parameters:**

` iSelSetName`      The name of the Selection Set to put in the CSO.

**Returns:**      The error code of function :

  * S_OK if the content of the Selection Set is added in the CSO
  * E_FAIL if the content of the Selection Set is added in the CSO

### Sub **RenameSelectionSet**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iOldSelSetName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNewSelSetName`)

   Renames a Selection Set.

**Parameters:**

` iOldSelSetName`      The original name of the Selection Set.
` iNewSelSetName`      The new name of the Selection Set.

**Returns:**      The error code of function :

  * S_OK if the name is changed
  * E_FAIL if the name is not changed