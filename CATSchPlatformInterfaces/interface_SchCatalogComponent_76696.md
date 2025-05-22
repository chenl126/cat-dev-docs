# SchCatalogComponent (Object)

**_Manage a schematic component catalog._**

## Methods

### Func **QueryDropAbility**( boolean  `oBYes`) As [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)

Check to see if it is OK to be dropped to the current document.

**Parameters:**

` oBYes`      If TRUE, then it is OK to be dropped.
` oPointedToComp`      Graphical representation of a component pointed-to by the catalog description
**Example:**

```VBScript
Dim objThisIntf As SchCatalogComponent
Dim bVar1 As boolean
Dim objArg2 As SchGRRComp
 ...
Set objArg2 = objThisIntf.QueryDropAbility

```

### Func **QueryDropCompGroupAbility**( boolean  `oBYes`) As [CATIASchCompGroupExt](../CATSchPlatformInterfaces/interface_SchCompGroupExt_47737.md)

Check to see if it is OK to be dropped a component group to the current document.

**Parameters:**

` oBYes`      If TRUE, then it is OK to be dropped.
` oPointedToGroup`      Component group extension pointed-to by the catalog description
**Example:**

```VBScript
Dim objThisIntf As SchCatalogComponent
Dim bVar1 As boolean
Dim objArg2 As SchCompGroupExt
 ...
Set objArg2 = objThisIntf.QueryDropCompGroupAbility

```