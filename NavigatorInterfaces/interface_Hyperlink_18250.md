# Hyperlink (Object)

**_Represents a hyperlink marker._**

## Methods

### Sub **AddUrl**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iUrl`)

   Adds a url to an Hyperlink.

**Parameters:**

` iUrl`      The URL to be added to the Hyperlink.

**Example:**      This example links `TheUrl` to the `NewHyperlink` Hyperlink.

```VBScript
        NewHyperlink.AddUrl(TheUrl)

```

### Func **CountObject**( ) As long

   Returns the number of Url which are linked to the Hyperlink.

**Example:**      This example reads the number of Url in the Hyperlink `NewHyperlink `.

```VBScript
        Dim number As Integer
        number = NewHyperlink.CountObject

```

### Func **ItemObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns an Url which is linked to the Hyperlink using its index.

**Parameters:**

` iIndex`      The index of the Url in the Hyperlink. The index of the first object is 1, and the index of the last object is CountObject.

**Returns:**      The retrieved Url  **Example:**      This example retrieves in `ThisUrl` the ninth object from the `NewHyperlink ` Hyperlink.

```VBScript
        Dim ThisUrl As String
        Set ThisUrl = NewHyperlink.ItemObject(9)

```

### Sub **RemoveObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an Url which is linked to the Hyperlink using its index.

**Parameters:**

` iIndex`      The index of the object in the Hyperlink. The index of the first object is 1, and the index of the last object is CountObject.

**Example:**      This example removes the ninth Url from the `NewHyperlink ` Hyperlink.

```VBScript
        NewHyperlink.RemoveObject(9)

```