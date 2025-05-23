# SchRouteAlternateGraphic (Object)

**_Manage alternative graphical primitives of a schematic route._**

## Methods

### Sub **AddAlternateGraphic**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iInitialXYPosition`,| | [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `oAddedGRR`)

   Add an alternate graphical primitive to a route. The alternate graphical style is determined by the application. on the Schematic component in order to specify the graphic style. on the Schematic component in order to identify the component as an assembly.

**Parameters:**

` iInitialXYPosition`      The initial position for calculating the display of the graphic. If NULL, the start point will be calculated based on the route graphic path of the first assembly member to this Schematic component.
` oAddedGRR`      The route alternate graphical primitive that is added to the route.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteAlternateGraphic
     Dim dbVar1(x) As CATSafeArrayVariant
     Dim objArg2 As SchGRR
      ...
     objThisIntf.AddAlternateGraphicdbVar1,objArg2

```

### Func **ListAlternateGraphics**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Lists the alternate graphics of a route. The list contains all objects of the same alternate graphic style. The style is determined must be implemented on the Schematic component in order to specify the graphic style.

**Parameters:**

` oLGRR`      A list of the alternate graphic objects.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteAlternateGraphic
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListAlternateGraphics

```

### Sub **RemoveAllAlternateGraphics**( )

   Removes all alternate graphical primitives.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteAlternateGraphic
      ...
     objThisIntf.RemoveAllAlternateGraphics

```

### Sub **RemoveAllAlternateGraphicsOfStyle**( [CatSchIDLRouteAlternateGraphicStyle](../CATSchPlatformInterfaces/enum_CatSchIDLRouteAlternateGraphicStyle_250313.md)  `iStyle`)

   Removes all alternate graphical primitives of the given style.

**Parameters:**

` iStyle`      An enum of the style of alternate graphic to remove.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteAlternateGraphic

      ...
     objThisIntf.RemoveAllAlternateGraphicsOfStyleCatSchIDLRouteAlternateGraphicStyle_Enum

```

### Sub **RemoveAlternateGraphic**( [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRRToBeRemoved`)

   Remove an alternate graphical primitive from a route.

**Parameters:**

` iGRRToBeRemoved`      The route alternate graphic to be removed from the route. The input graphic will be removed as long as there are at least two alternate graphics of that style on the route.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteAlternateGraphic
     Dim objArg1 As SchGRR
      ...
     objThisIntf.RemoveAlternateGraphicobjArg1

```