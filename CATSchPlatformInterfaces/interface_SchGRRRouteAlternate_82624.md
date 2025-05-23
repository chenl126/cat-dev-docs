# SchGRRRouteAlternate (Object)

**_Manage the graphical styles for alternative route graphics._**

## Methods

### Sub **GetAlternateStyle**(| [CatSchIDLRouteAlternateGraphicStyle](../CATSchPlatformInterfaces/enum_CatSchIDLRouteAlternateGraphicStyle_250313.md) | `oEGraphicStyle`)

   Returns the graphicl style of the alternate graphic object.

**Parameters:**

` oEGraphicStyle`      Enum describing the graphic style of the object. (see CATSchGeneralEnum.h for descriptions)

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRouteAlternate

      ...
     objThisIntf.GetAlternateStyleCatSchIDLRouteAlternateGraphicStyle_Enum

```