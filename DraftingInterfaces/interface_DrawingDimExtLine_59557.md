# DrawingDimExtLine (Object)

**_Manages extension lines of a dimension in drawing view._**

This interface is obtained from [DrawingDimension.GetExtLine](../DraftingInterfaces/interface_DrawingDimension_55138.htm#GetExtLine) method.

## Properties

### Property **Color**(| ) As long

   Returns or sets color of extension line.

**Example:**      This example retrieves color of extension line `MyExtLine` drawing dimension.

```VBScript
     oColorExtLine = MyExtLine.Color

```

### Property **ExtLineSlant**( ) As double

   Returns or sets slant angle of extension line.

**Example:**      This example retrieves slant angle of extension line `MyExtLine` drawing dimension.

```VBScript
     oExtLineSlant = MyExtLine.ExtLineSlant

```

### Property **ExtLineType**( ) As long (Read Only)

   Returns extension line type of dimension.

**Example:**      This example retrieves extension line type of dimension `MyExtLine` drawing dimension.

```VBScript
     oExtLineType = MyExtLine.ExtLineType

```

### Property **Thickness**( ) As double

   Returns or sets thickness of extension line.

**Example:**      This example retrieves thickness of extension line `MyExtLine` drawing dimension.

```VBScript
     oThickExtLine = MyExtLine.Thickness

```

Methods

### Sub **AddInterrupt**( long  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTwoPoints`)

   Add an interrupt to an extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` iTwoPoints`      Defines the first and second point of the gap to create.  **Example:**      This example adds an interrupt to `MyExtLine` path.

```VBScript
     MyExtLine.AddInterrupt(iIndex, iTwoPoints)

```

### Sub **GetFunnel**( long  `iIndex`,  long  `oMode`,  double  `oAngle`,  double  `oHeight`,  double  `oWidth`)

   Get funnel infomation of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` oMode`      funnel inside/outside mode.
` oAngle`      funnel angle.
` oHeight`      funnel height.
` oWidth`      funnel width.  **Example:**      This example gets funnel infomation of `MyExtLine` path.

```VBScript
     MyExtLine.GetFunnel(iIndex, oMode, oAngle, oHeight, oWidth)

```

### Func **GetGap**( long  `iIndex`) As double

   Get gap of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` oGap`      Gap.  **Example:**      This example gets gap of `MyExtLine` path.

```VBScript
     Gap = MyExtLine.GetGap(iIndex)

```

### Sub **GetGeomInfo**( long  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oGeomInfos`)

   Get geometrical infomation of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` oGeomInfos`      List of geometric coordinates (X1,Y1,X2,Y2,X3,Y3).  **Example:**      This example gets geometrical infomation of `MyExtLine` path.

```VBScript
     MyExtLine.GetGeomInfo(iIndex, oGeomInfos)

```

### Func **GetInterrupt**( long  `iIndex`) As long

   Get the number of interruptions stored in each extension lines.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` oNbIntOnExtLine`      The number of interruptions.  **Example:**      This example gets the number of interruptions of `MyExtLine` path.

```VBScript
     NbIntOnExtLine = MyExtLine.GetInterrupt(iIndex)

```

### Func **GetOverrun**( long  `iIndex`) As double

   Get overrun of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` oOverrun`      Overrun  **Example:**      This example gets overrun of `MyExtLine` path.

```VBScript
     Overrun = MyExtLine.GetOverrun(iIndex)

```

### Func **GetVisibility**( long  `iIndex`) As long

   Get visivility of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` oGap`      Gap.  **Example:**      This example gets visivility of `MyExtLine` path.

```VBScript
     ExtlineVisibility = MyExtLine.GetVisibility(iIndex)

```

### Sub **RemoveInterrupt**( long  `iIndex`)

   Remove interruption on extension lines.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line  **Example:**      This example Remove interruption on `MyExtLine` path.

```VBScript
     MyExtLine.RemoveInterrupt(iIndex)

```

### Sub **SetFunnel**( long  `iIndex`,  long  `iMode`,  double  `iAngle`,  double  `iHeight`,  double  `iWidth`)

   Set funnel infomation of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` iMode`      funnel inside/outside mode.
` iAngle`      funnel angle.
` iHeight`      funnel height.
` iWidth`      funnel width.  **Example:**      This example sets funnel infomation of `MyExtLine` path.

```VBScript
     MyExtLine.SetFunnel(iIndex, iMode, iAngle, iHeight, iWidth)

```

### Sub **SetGap**( long  `iIndex`,  double  `iGap`)

   Set gap of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` iGap`      gap  **Example:**      This example sets gap of `MyExtLine` path.

```VBScript
     MyExtLine.SetGap(iIndex, iGap)

```

### Sub **SetOverrun**( long  `iIndex`,  double  `iOverrun`)

   Set overrun of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` iOverrun`      Overrun  **Example:**      This example sets overrun of `MyExtLine` path.

```VBScript
     MyExtLine.SetOverrun(iIndex, iOverrun)

```

### Sub **SetVisibility**( long  `iIndex`,  long  `iExtlineVisibility`)

   Set visivility of dimension extension line.

**Parameters:**

` iIndex`      1: first extension line 2: second extension line
` iExtlineVisibility`      visivility  **Example:**      This example sets visivility of `MyExtLine` path.

```VBScript
     MyExtLine.SetVisibility(iIndex, iExtlineVisibility)

```