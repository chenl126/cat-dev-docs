# MfgAssembly (Object)

**_This Interface represents a Manufacturing Assembly._**

**Role** : It gives access to the C++ DNBIMfgAssembly interface methods Such as

  * set and get the Name and PartNumber
  * get the type [DNBIAMfgAssemblyType](../DNBDpmInterfaces/enum_DNBIAMfgAssemblyType_80340.md)
  * get the assigned parts
  * add and remove the assigned parts

**Example:**      This example fetches an instance of a Manufacturing Assembly from a selected Activity

```VBScript
     Dim myActivity As Activity
     myActivity =
     Dim myItem As Item
     Set myItem = myActivity.Items.Item(1)
     Dim obj As MfgAssembly
     Set obj = mySel.FindObject("DNBIAMfgAssembly")

```

## Properties

### Property **Count**(| ) As long (Read Only)

   Returns the number of assigned Parts (can be fetched via Item ).

**Example:**      This example fetches the Number of assigned Parts of a Manufacturing Assembly

```VBScript
     Dim Number As Long
     Number = obj.Count

```

### Property **MAName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Name of the Manufacturing Assembly.

**Example:**      This example fetches the Name of a Manufacturing Assembly

```VBScript
     Dim myName As String
     myName = obj.MAName

```

   This example sets the Name of a Manufacturing Assembly

```VBScript
     Dim newName As String
     newName = "NewMAName"
     obj.MAName = newName

```

### Property **MAPartNumber**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Part Number of the Manufacturing Assembly.

**Example:**      This example fetches the Part Number of a Manufacturing Assembly

```VBScript
     Dim myPart As String
     myPart = obj.MAPartNumber

```

   This example sets the Part Number of a Manufacturing Assembly

```VBScript
     Dim newPartNbr As String
     newPartNbr = "NewMAPartNumber"
     obj.MAPartNumber = newPartNbr

```

### Property **MAType**( ) As DNBIAMfgAssemblyType (Read Only)

   Returns the Type of the Manufacturing Assembly. It will be either a manufacturingAssembly or a manufacturingKit defined in [DNBIAMfgAssemblyType](../DNBDpmInterfaces/enum_DNBIAMfgAssemblyType_80340.md)

**Example:**      This example fetches the Type of a Manufacturing Assembly

```VBScript
     Dim MAtype As String
     If obj.MAType = manufacturingAssembly Then
       MAtype = "Manufacturing Assembly"
     Else
       MAtype = "Manufacturing Kit"
     End If

```

Methods

### Sub **AddPart**( [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)  `iItem`)

   Assignes a part (Product, Resource or other MA/MK) to the Manufacturing Assembly.

**Parameters:**

` iItem`      The item to be assigned

**Example:**      This example adds a product to the assigned Parts of a Manufacturing Assembly

```VBScript
     Dim myProducts As PPRProducts
     Set myProducts = DELMIA.ActiveDocument.PPRDocument.Products
     Dim Part As Item
     Set Part = myProducts.Item(2)
     obj.AddPart(Part)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

   Returns one assigned Part (Product, Resource or other MA/MK) of the Manufacturing Assembly.

**Parameters:**

` iIndex`      The index to the item to be returned

**Returns:**      The assigned item

**Example:**      This example cycles through the list of assigned Parts of a Manufacturing Assembly

```VBScript
     Dim j As Long
     For j = 1 To obj.Count
       Dim it As Item
       Set it = obj.Item(j)
       Dim ItemName As String
       ItemName = it.Name
     Next

```

### Sub **RemovePart**( [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)  `iItem`)

   Removes a part (Product, Resource or other MA/MK) from the Manufacturing Assembly.

**Parameters:**

` iItem`      The item to be removed

**Example:**      This example removes a product from the assigned Parts of a Manufacturing Assembly

```VBScript
     Dim myProducts As PPRProducts
     Set myProducts = DELMIA.ActiveDocument.PPRDocument.Products
     Dim Part As Item
     Set Part = myProducts.Item(2)
     obj.RemovePart(Part)

```