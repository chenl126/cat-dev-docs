# ManufacturingPattern (Object)

**_The Manufacturing Pattern is a specialized feature used to machine the same item several times at several positions._**

## Properties

### Property **ToolAxisStrategy**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Tool Axis Strategy of a Manufacturing Pattern.

**Legal values** : The parameter name can be

`Fixed`      `Variable`      `NormalToPS`      **Examples:**     The following example returns the Tool Axis Strategy `ThisToolAxisStrategy` of the manufacturing pattern `CurrentMfgPattern`

```VBScript
     Dim ThisToolAxisStrategy As CATBSTR
     ThisToolAxisStrategy = CurrentMfgPattern.ToolAxisStrategy

```

The next example sets the Tool Axis Strategy of the manufacturing pattern `CurrentMfgPattern`

```VBScript
     CurrentMfgPattern.ToolAxisStrategy = "Fixed"

```

Methods

### Sub **ActivatePoint**( short  `iPointNumber`)

   Activates a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point to activate.

**Example:**     The following example activates the point number 2 of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.ActivatePoint(2)

```

### Sub **AddPartSurface**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPartSurface`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  short  `iNotify`)

   Adds a Part Surface to the Manufacturing Pattern.

**Parameters:**

` iPartSurface`      The part surface to be added.
` iProduct`      The product containing the part surface to add.
` iNotify`      The flag to specify if a refresh of the visualization is needed. Usually, this parameter is set to 1. In the case of a loop, it should be set to 1 only on the last call of the method.

**Legal values** : The parameter can be

`0`      no notification is sent `1`      a notification is sent

**Example:**     The following example adds the part surface 'TopPlane' to the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.AddPartSurface(TopPlane,Product1,1)

```

### Sub **AddPosition**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPosition`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  short  `iNotify`)

   Adds a position to the Manufacturing Pattern.

**Parameters:**

` iPosition`      The position to be added.

**Legal values** : The position can be a

`Design Hole`      the point is the origin point of the hole `Design Pattern`      points are retrieved from the design pattern `Point`      the point coordinates are retrieved from the added point `Circle`      the point is the center of the circle
` iProduct`      The product containing the position to add.
` iNotify`      The flag to specify if a refresh of the visualization is needed. Usually, this parameter is set to 1. In the case of a loop, it should be set to 1 only on the last call of the method.

**Legal values** : The parameter can be

`0`      no notification is sent `1`      a notification is sent

**Example:**     The following example adds the position 'DesignPattern1' to the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.AddPosition(DesignPattern1,Product1,1)

```

### Sub **DeactivatePoint**( short  `iPointNumber`)

   Deactivates a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point to deactivate.

**Example:**     The following example deactivates the point number 2 of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.DeactivatePoint(2)

```

### Func **GetAnAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retreive the attribute of Manufacturing Pattern from its name.

**Parameters:**

` iAttribute`      The identifier of the attribute to be read.

**Legal values** : The identifier can be

`JumpDistance`      the jump distance of the pattern `TopMode`      the Top Mode of the pattern

**Example:**     The following example retrieves the attribute 'JumpDistance' of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.GetAnAttribute(JumpDistance,JumpParm)

```

### Sub **GetLocalToolAxis**( short  `iPointNumber`,  double  `oX`,  double  `oY`,  double  `oZ`)

   Retrieve the local tool axis of a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point on which the tool axis is set.
` oX`      The first coordinate of the tool axis.
` oY`      The second coordinate of the tool axis.
` oZ`      The third coordinate of the tool axis.

**Example:**     The following example retrieves the tool axis of the point number 3 of manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.GetLocalToolAxis(3,oX,oY,oZ)

```

### Sub **GetNumbers**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oNumbers`)

   Retrieve the number of the points of a Manufacturing Pattern.

**Parameters:**

` oNumbers`      The numbers of the points of the pattern.

**Example:**     The following example retrieves the numbers of the points of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.GetNumbers(oNumbers)

```

### Sub **RemovePartSurfaces**( )

   Remove the Part Surfaces of the Manufacturing Pattern.

**Example:**     The following example removes the part surfaces of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.RemovePartSurfaces()

```

### Sub **Reverse**( )

   Reverses the numbering of a Manufacturing Pattern.

**Example:**     The following example reverses the numbering of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.Reverse()

```

### Sub **SetItemToCopy**( [CATIABase](../System/interface_AnyObject_17321.md)  `iItem`)

   Sets the feature to be copied.

**Parameters:**

` iItemToCopy`      The feature to be copied. It may be a Design Hole or a Manufacturing Hole.

**Legal values** : The parameter name can be

`Diameter`     The hole diameter
` oParameter`      The value of the parameter

**Example:**     The following example sets the item to copy 'Hole1' to the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.SetItemToCopy(Hole1)

```

### Sub **SetLocalToolAxis**( short  `iPointNumber`,  double  `iX`,  double  `iY`,  double  `iZ`)

   Sets a local tool axis to a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point on which the tool axis is set .
` iX`      The first coordinate of the tool axis.
` iY`      The second coordinate of the tool axis.
` iZ`      The third coordinate of the tool axis.

**Example:**     The following example sets the Z axis as tool axis of the point number 3 of manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.SetLocalToolAxis(3,0,0,1)

```

### Sub **StartPoint**( short  `iPointNumber`)

   Sets a point of a Manufacturing Pattern as the start point.

**Parameters:**

` iPointNumber`      The number of the point to set as start point.

**Example:**     The following example sets the point number 2 as the start point of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.StartPoint(2)

```