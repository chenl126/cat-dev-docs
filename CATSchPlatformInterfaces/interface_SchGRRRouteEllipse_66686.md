# SchGRRRouteEllipse (Object)

**_Manage the graphical representation of a schematic route._**

## Methods

### Sub **GetSeedPoint**( [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb2XY`)

Get the seed point of the route graphic ellipse.

**Parameters:**

` oDb2XY`      X-Y coordinates of the seed point for the ellipse.
**Example:**

```VBScript
Dim objThisIntf As SchGRRRouteEllipse
Dim objArg1 As SchListOfDoubles
 ...
objThisIntf.GetSeedPointobjArg1

```

### Sub **HasSeedPoint**( boolean  `oBYes`)

Check to see if the Seed point has been set.

**Parameters:**

` oBYes`      TRUE if the seed point has been initialized.
**Example:**

```VBScript
Dim objThisIntf As SchGRRRouteEllipse
Dim bVar1 As boolean
 ...
objThisIntf.HasSeedPointbVar1

```

### Sub **SetSeedPoint**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2XY`)

Set the seed point of the route graphic ellipse.

**Parameters:**

` iDb2EndPt`      X-Y coordinates of the seed point for the ellipse.
**Example:**

```VBScript
Dim objThisIntf As SchGRRRouteEllipse
Dim dbVar1(2) As CATSafeArrayVariant
 ...
objThisIntf.SetSeedPointdbVar1

```