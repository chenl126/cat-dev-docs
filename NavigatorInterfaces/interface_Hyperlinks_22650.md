# Hyperlinks (Collection)

**__**

## Methods

### Func **Add**(| [CATIABase](../System/interface_AnyObject_17321.md) | `iObject`) As [CATIAHyperlink](../NavigatorInterfaces/interface_Hyperlink_18250.md)

   Adds a Hyperlink to the Hyperlinks collection. Be careful: only one Hyperlink instance is allowed per object which supports the hyperlink. If one adds a Hyperlink on an object which already has a Hyperlink, the call fails. The Hyperlink name is internally generated. If one wants to manage Hyperlink using its name, he has to set it manually.

**Parameters:**

` iObject`      The object which supports the hyperlink.

**Example:**      The following example adds a Hyperlink

```VBScript
        Dim NewHyperlink As Hyperlink
        Set NewHyperlink = TheHyperlinks.Add(iObject)

```

### Func **GetHyperlink**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAHyperlink](../NavigatorInterfaces/interface_Hyperlink_18250.md)

   Retrieve an Hyperlink associated to an object

**Parameters:**

` iObject`      The object which supports the hyperlink. The call fails otherwise.

**Returns:**      The retrieved Hyperlink if it exists  **Example:**      This example retrieves an existing one in the `TheHyperlinks` collection.

```VBScript
        Dim NewHyperlink As Hyperlink
        Set NewHyperlink = TheHyperlinks.GetHyperlink(iObject)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAHyperlink](../NavigatorInterfaces/interface_Hyperlink_18250.md)

   Returns an Hyperlink using its index from the Hyperlinks collection.

**Parameters:**

` iIndex`      The index or the name of the hyperlink to retrieve from the collection of Hyperlinks. As a numerics, this index is the rank of the Hyperlink in the collection. The index of the first Hyperlink in the collection is 1, and the index of the last Hyperlink is Count. As a string, it is the name you assigned to the Hyperlink.

**Returns:**      The retrieved Hyperlink  **Example:**      This example retrieves in `ThisHyperlink` the ninth Hyperlink , and in `ThatHyperlink` the Hyperlink named ` Hyperlink3` from the `TheHyperlinks` collection.

```VBScript
        Dim ThisHyperlink As Hyperlink
        Set ThisHyperlink = TheHyperlinks.Item(9)
        Dim ThatHyperlink As Hyperlink
        Set ThatHyperlink = TheHyperlinks.Item("Hyperlink3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Hyperlink from the Hyperlinks collection.

**Parameters:**

` iIndex`      The index or the name of the Hyperlink to retrieve from the collection of Hyperlinks. As a numerics, this index is the rank of the Hyperlink in the collection. The index of the first Hyperlink in the collection is 1, and the index of the last Hyperlink is Count. As a string, it is the name you assigned to the Hyperlink.

**Example:**      The following example removes the tenth Hyperlink and the Hyperlink named ` Hyperlink 2` from the `TheHyperlinks` collection.

```VBScript
        TheHyperlinks.Remove(10)
        TheHyperlinks.Remove("Hyperlink2")

```