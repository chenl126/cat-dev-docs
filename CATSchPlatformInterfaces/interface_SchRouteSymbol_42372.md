# SchRouteSymbol (Object)

**_Manage a symbol placed on a route._**

## Methods

### Sub **FlipOverLine**( )

Mirror the symbol over the route segment line on which the symbol is positioned.

**Example:**

```VBScript
Dim objThisIntf As SchRouteSymbol
 ...
objThisIntf.FlipOverLine

```

### Sub **FlipOverOrthogonalLine**( )

Mirror the symbol over the line orthogonal to the route segment line on which the symbol is positioned and going through the symbol's position point on that segment line.

**Example:**

```VBScript
Dim objThisIntf As SchRouteSymbol
 ...
objThisIntf.FlipOverOrthogonalLine

```

### Func **GetGRRRoute**( ) As [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)

Get the graphical representation of a schematic route that owns this symbol.

**Parameters:**

` oGRRRoute`      The graphical representation that owns this symbol.
**Example:**

```VBScript
Dim objThisIntf As SchRouteSymbol
Dim objArg1 As SchGRRRoute
 ...
Set objArg1 = objThisIntf.GetGRRRoute

```

### Sub **GetPosition**( long  `oSegNum`,  double  `oSegParm`)

Get the symbol's position on the route that own it.

**Parameters:**

` oSegNum`      The route segment number.
` oSegParm`      The parameter along the segment.
**Example:**

```VBScript
Dim objThisIntf As SchRouteSymbol
Dim intVar1 As Integer
Dim dbVar2 As Double
 ...
objThisIntf.GetPositionintVar1,dbVar2

```

### Sub **Scale**( double  `iDbScaleFactor`)

Scale the symbol.

**Parameters:**

` iDbScaleFactor`      The scale factor to scale the symbol by.
**Example:**

```VBScript
Dim objThisIntf As SchRouteSymbol
Dim dbVar1 As Double
 ...
objThisIntf.ScaledbVar1

```

### Sub **SetPosition**( long  `iSegNum`,  double  `iSegParm`)

Set the symbol's position on the route that own it.

**Parameters:**

` iSegNum`      The route segment number (<= number of segments in the route).
` iSegParm`      The parameter along the segment (0.<=iSegParm<=1.).
**Example:**

```VBScript
Dim objThisIntf As SchRouteSymbol
Dim intVar1 As Integer
Dim dbVar2 As Double
 ...
objThisIntf.SetPositionintVar1,dbVar2

```