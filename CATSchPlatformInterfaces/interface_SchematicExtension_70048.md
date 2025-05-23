# SchematicExtension (Object)

**_Manage schematic extensions._**

## Methods

### Sub **AddExtension**(| [CATIABase](../System/interface_AnyObject_17321.md) | `iAppObjToBeExtended`,| | [CatSchIDLExtensionType](../CATSchPlatformInterfaces/enum_CatSchIDLExtensionType_99308.md) | `iExtensionType`,| | [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) | `iLGRR`)

   Adds a Schematic extension to an application object.

**Parameters:**

` iAppObjToBeExtended`      The application object to be extended.
` iExtensionType`      The extension type.
` iLGRR`      If iLGRR is not NULL, then its members will be linked to the extension as graphics

**Example:**

```VBScript
     Dim objThisIntf As SchematicExtension
     Dim objArg1 As AnyObject

     Dim objArg3 As SchListOfObjects
      ...
     objThisIntf.AddExtensionobjArg1,CatSchIDLExtensionType_Enum,objArg3

```

### Sub **RemoveExtension**( [CATIABase](../System/interface_AnyObject_17321.md)  `iAppExtendedObj`,  [CatSchIDLExtensionType](../CATSchPlatformInterfaces/enum_CatSchIDLExtensionType_99308.md)  `iExtensionType`)

   Removes a Schematic extension to an application object.

**Parameters:**

` iAppExtendedObj`      The application object to be have its extension removed.
` iExtensionType`      The extension type.

**Example:**

```VBScript
     Dim objThisIntf As SchematicExtension
     Dim objArg1 As AnyObject

      ...
     objThisIntf.RemoveExtensionobjArg1,CatSchIDLExtensionType_Enum

```