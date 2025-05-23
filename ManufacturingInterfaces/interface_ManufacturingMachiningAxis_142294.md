# ManufacturingMachiningAxis (Object)

**_ManufacturingMachiningAxis defines a set of methods to manage a Machining Axis System or an Origin._**

## Properties

### Property **Origin**(| ) As short

   This property returns the interface which manages if instruction os used as an Origin or as a Machining Axis System. If instruction is an Origin, Origin is set to 1, 0 otherwise.

**Example:**     The following example returns in `origin` the attribute to provide if instruction is used as a Machining Axis System or an Origin :

```VBScript
     ...
     Set myInstruction  = ...
     Set MyOrigin = myInstruction.Origin

```

### Property **OriginGroup**( ) As short

   This property returns the interface which determines the origin group of the instruction if used a an Origin.

**Example:**     The following example set the Origin Group to 5.

```VBScript
     ...
     Set myInstruction  = ...
     Set myInstruction.OriginGroup = 3

```

### Property **OriginNumber**( ) As short

   This property returns the interface which manages the origin number of the instruction if used a an Origin.

**Example:**     The following example set the Origin Number to 3.

```VBScript
     ...
     Set myInstruction  = ...
     Set myInstruction.OriginNumber = 3

```

Methods

### Sub **GetOriginPoint**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with PointOrigin as an Origin Point and with ProductOrigin a belonging product.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     Dim PointOrigin As CATSafeArrayVariant
     Dim ProductOrigin As Product
     MfgAxisSystem.GetOriginPoint (PointOrigin)

```

### Sub **GetOriginXDirection**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin X direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with origin X direction in DblMathDirection.

```VBScript
     Dim DlbMathDirection As Double(3)
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.GetOriginXDirection (DblMathDirection)

```

### Sub **GetOriginYDirection**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin Y direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with origin Y direction in DblMathDirection.

```VBScript
     Dim DlbMathDirection As Double(3)
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.GetOriginYDirection (DblMathDirection)

```

### Sub **GetOriginZDirection**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin Z direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with origin Z direction in DblMathDirection.

```VBScript
     Dim x,y,z As Double
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.GetOriginZDirection (x,y,z)

```

### Sub **SetOriginPoint**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPoint`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`)

   Sets the Origin of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example sets `MfgAxisSystem` with PointOrigin as an Origin Point and with ProductOrigin a belonging product.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     Dim PointOrigin As AnyObject
     Dim ProductOrigin As Product
     MfgAxisSystem.SetOriginPoint (PointOrigin,ProductOrigin)

```

### Sub **SetOriginPointByCoordinates**( double  `x`,  double  `y`,  double  `z`)

   Sets the Origin of a Manufacturing Machining Axis System used as Origin by coordinates.

**Example:**     The following example sets the Origin `MfgAxisSystem` at coordinates x,y,z.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.SetOriginPointByCoordinates(x,y,z)

```

### Sub **SetOriginXDirection**( double  `x`,  double  `y`,  double  `z`)

   Sets the Origin X direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example sets `MfgAxisSystem` with origin X direction in DblMathDirection.

```VBScript
     Dim DlbMathDirection As Double(3)
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.SetOriginXDirection (DblMathDirection)

```

### Sub **SetOriginZDirection**( double  `x`,  double  `y`,  double  `z`)

   Sets the Origin Z direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example sets `MfgAxisSystem` with origin Y direction in DblMathDirection.

```VBScript
     Dim x,y,z As Double
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.SetOriginZDirection (x,y,z)

```

### Sub **SetPartAxisSystem**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPAS`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`)

   Sets the Part Axis System of a Manufacturing Machining Axis System.

**Example:**     The following example sets `MfgAxisSystem` with PAS as a Part Axis System and with ProductPAS a belonging product.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     Dim PAS As AxisSystem
     Dim PASProduct As Product
     MfgAxisSystem.SetMachiningAxisSystem (PAS,PASProduct)

```