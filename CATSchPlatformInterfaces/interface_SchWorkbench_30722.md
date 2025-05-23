# SchWorkbench (Object)

**_Represents a workbench on a schematic document._**

**Role** :A workbench is a set of commands that can be used to create, modify and edit the objects making up the document.

**See also:**      [Document](../InfInterfaces/interface_Document_14456.md)

## Methods

### Func **FindInterface**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iInterfaceName`,| | [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md) | `iObject`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   This method returns an interface handle to an object.

**Parameters:**

` iInterfaceName`      interface name to search for ("CATIAxxxx")
` iObject`      The object to search for the required interface.
` oInterfaceFound`      interface handle found

**Example:**      The following example retrieves a `CATIAInterfaceNameToFind` handle to the `CATIAxxxx_iObject` in `interfaceFound` using the Schematics workbench object `schWorkbench`.

```VBScript
     Dim interfaceFound As AnyObject
     Set interfaceFound = CATIASchWorkbench.FindInterface("InterfaceNameToFind",CATIAProduct_iObject)

```