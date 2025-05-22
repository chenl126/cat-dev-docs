# Windows (Collection)

**_A collection of all the Window objects currently managed by the application._**

## Methods

### Sub **Arrange**( [CatArrangeStyle](../InfInterfaces/enum_CatArrangeStyle_47743.md)  `iStyle`)

Arranges all the windows of the collection.

**Parameters:**

` iStyle`      The arrangement style to take into account to arrange the windows  **Example:**      The following example arranges all the windows in the `Windows` collection, according to the `catArrangeCascade` style.

```VBScript
CATIA.Windows.Arrange(catArrangeCascade)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAWindow](../InfInterfaces/interface_Window_8384.md)

Returns a window using its index or its name from the Windows collection.

**Parameters:**

` iIndex`      The index or the name of the window to retrieve from the collection of windows. As a numerics, this index is the rank of the window in the collection. The index of the first window in the collection is 1, and the index of the last window is Count. As a string, it is the name you assigned to the window using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved window  **Example:**      This example returns in `ThisWindow` the third window in the collection, and in `ThatWindow` the window named `MyWindow`.

```VBScript
Dim ThisWindow As Window
Set ThisWindow = CATIA.Windows.Item(3)
Dim ThatWindow As Window
Set ThatWindow = CATIA.Windows.Item("MyWindow")

```