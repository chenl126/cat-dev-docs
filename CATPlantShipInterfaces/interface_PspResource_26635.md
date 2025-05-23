# PspResource (Object)

**_Represents the PspResource._**

**Role** : It is used to get application resources.

## Methods

### Func **GetResourcePath**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iResourceName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the path value defined for a resource.

**Parameters:**

` iResourceName`      Resource Name

**Returns:**      Resource Path  **Example:**

```VBScript
     Dim objThisIntf As PspResource
     Dim strResourcePath As String
     Dim iResourceName As String

      ...
     strResourcePath = objThisIntf.GetResourcePath (iResourceName)

```

### Func **GetResourceValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iResourceName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the value defined for a resource.

**Parameters:**

` iResourceName`      Resource Name

**Returns:**      Resource Value  **Example:**

```VBScript
     Dim objThisIntf As PspResource
     Dim strResourceVal As String
      ...
     strResourceVal = objThisIntf.GetResourceValue (iResourceName)

```