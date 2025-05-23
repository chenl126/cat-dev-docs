# SchCatalogRoute (Object)

**_Manage a schematic route catalog._**

## Methods

### Sub **QueryDropAbility**(| boolean | `oBYes`,| | [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md) | `oRouteRef`,| | [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `oPointedToGRR`)

   Check to see if it is OK to be dropped to the current document.

**Parameters:**

` oBYes`      If TRUE, then it is OK to be dropped.
` oRouteRef`      Route reference.
` oPointedToGRR`      Graphical representation of a route pointed-to by the catalog component

**Example:**

```VBScript
     Dim objThisIntf As SchCatalogRoute
     Dim bVar1 As boolean
     Dim objArg2 As SchRoute
     Dim objArg3 As SchGRR
      ...
     objThisIntf.QueryDropAbilitybVar1,objArg2,objArg3

```