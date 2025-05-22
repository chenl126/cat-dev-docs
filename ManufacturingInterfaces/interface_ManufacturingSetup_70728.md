# ManufacturingSetup (Object)

**_A ManufacturingSetup for a Manufacturing Document._**

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Return the Default Comment of a Manufacturing Setup.

**Example:**     The following example return the comment `SetupComment` of to the manufacturing setup `CurrentSetup`

```VBScript
Set CurrentSetup.Comment= "SetupComment"

```

### Property **Machine**( ) As [CATIAManufacturingMachine](../ManufacturingInterfaces/interface_ManufacturingMachine_84488.md)

Give the Machine linked to a Manufacturing Setup.

**Example:**     The following example returns the `Machine` linked to the manufacturing setup `CurrentSetup`

```VBScript
Set Machine = CurrentSetup.Machine

```

### Property **MachiningAxisSystem**( ) As [CATIAManufacturingMachiningAxis](../ManufacturingInterfaces/interface_ManufacturingMachiningAxis_142294.md)

Retrieves the Machining Axis system from a Manufacturing Setup.

**Example:**     The following example retrieves the Machining Axis system `oMachiningAxis` from the manufacturing setup `CurrentSetup`

```VBScript
Set oMachiningAxis = CurrentSetup.MachiningAxisSystem

```

### Property **Product**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

Associate the Product to a Manufacturing Setup.

**Example:**     The following example associates the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
CurrentSetup.Product = iProduct

```

### Property **Programs**( ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md) (Read Only)

Give the List of Programs linked to a Manufacturing Setup.

**Example:**     The following example returns the list of Programs `ProgramsList` linked to the manufacturing Setup `CurrentSetup`

```VBScript
Set ProgramsList = CurrentSetup.Programs

```

Methods

### Func **CreateMachine**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMachine`) As [CATIAManufacturingMachine](../ManufacturingInterfaces/interface_ManufacturingMachine_84488.md)

Initialise the Manufacturing Machine linked to a Manufacturing Setup.

**Example:**     The following example initialise the machine `Mfg3AxisWithTableRotationMachine` as Manufacturing Machine in the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.CreateMachine(Mfg3AxisWithTableRotationMachine)

```

### Func **DesignGeometriesCount**( ) As long

Returns the number of design geometries from a Manufacturing Setup.

**Parameters:**

` oDesignGeometriesListSize`      The number of design geometries of this setup  **Example:**     The following example retrieves the number of design geometries of the setup `CurrentSetup` in `DesignGeometriesListSize`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim DesignGeometriesListSize As Long
DesignGeometriesListSize = CurrentSetup.DesignGeometriesCount

```

### Func **FixtureGeometriesCount**( ) As long

Returns the number of fixture geometries from a Manufacturing Setup.

**Parameters:**

` oFixtureGeometriesListSize`      The number of fixture geometries of this setup  **Example:**     The following example retrieves the number of fixture geometries of the setup `CurrentSetup` in `FixtureGeometriesListSize`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim FixtureGeometriesListSize As Long
FixtureGeometriesListSize = CurrentSetup.FixtureGeometriesCount

```

### Func **GetMachiningAxisSystemName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves the Name of the Machining Axis system from a Manufacturing Setup.

**Example:**     The following example retrieves the Name of the Machining Axis system`oMachiningAxisSystemName` from the manufacturing setup `CurrentSetup`

```VBScript
Set oMachiningAxisSystemName = CurrentSetup.GetMachiningAxisSystemName

```

### Func **GetManufacturingView**( ) As [CATIAManufacturingView](../ManufacturingInterfaces/interface_ManufacturingView_62589.md)

Retrieves the Manufacturing View from a Manufacturing Setup.

**Example:**     The following example retrievec the Manufacturing View `MfgView` from the manufacturing setup `CurrentSetup`

```VBScript
Set MfgView = CurrentSetup.GetManufacturingView

```

### Func **GetPartName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves the Name of the Design Part from a Manufacturing Setup.

**Example:**     The following example retrieves the Name of the Design Part`oPartName` from the manufacturing setup `CurrentSetup`

```VBScript
Set oPartName = CurrentSetup.GetPartName

```

### Func **GetProductInstance**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Give the Product of the ProductList linked to a Manufacturing Setup.

**Example:**     The following example returns the `Product` linked to the manufacturing setup `CurrentSetup`

```VBScript
Set Product = CurrentSetup.GetProductInstance

```

### Func **GetSafetyPlane**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Retrieves the Safety Plane from a Manufacturing Setup.

**Example:**     The following example retrieves the Safety Plane `oMathPLane` from the manufacturing setup `CurrentSetup` The size of oMathPlane is 9 (origin, first direction, second direction)

```VBScript
Set oMathPlane= CurrentSetup.GetSafetyPlane

```

### Sub **GetStockFromSetup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oStockPath`)

Retrieves the path of the Stock file from a Manufacturing Setup.

**Example:**     The following example retrieves the the path of the Stock file`oStockPath` from the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.GetStockFromSetup(oStockPath)

```

### Sub **GetToolChangePoint**( double  `oX`,  double  `oY`,  double  `oZ`)

Get the ToolChange point of the machine linked to a Manufacturing Setup.

**Example:**     The following example gets the point with coordinates `X,Y,Z` as ToolChangePoint in the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.GetToolChangePoint(X,Y,Z)

```

### Func **InProcessModelBodiesCount**( ) As long

Returns the number of In Process Model Bodies from a Manufacturing Setup.

**Parameters:**

` oIPMBodiesListSize`      The number of In Process Model Bodies of this setup  **Example:**     The following example retrieves the number of In Process Model Bodies of the setup `CurrentSetup` in `IPMBodiesListSize`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim IPMBodiesListSize As Long
IPMBodiesListSize = CurrentSetup.InProcessModelBodiesCount

```

### Sub **ListDesignGeometries**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfDesignGeometries`)

Retrieves the design geometries list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfDesignGeometries`      The retrieved list.
The array must be previously initialized using the
DesignGeometriesCount method.  **Example:**     The following example retrieves the design geometries list of the manufacturing setup `CurrentSetup` in `ListOfDesignGeometries`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim DesignGeometriesListSize As Long
DesignGeometriesListSize = CurrentSetup.DesignGeometriesCount
If DesignGeometriesListSize > 0 Then
  Dim ListOfDesignGeometries() As Variant
  Redim ListOfDesignGeometries(DesignGeometriesListSize-1)
  CurrentSetup.ListDesignGeometries(ListOfDesignGeometries)
End If

```

### Sub **ListDesignGeometriesProducts**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfDesignGeometriesProducts`)

Retrieves the design geometries products list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfDesignGeometriesProducts`      The retrieved list.
The array must be previously initialized using the
DesignGeometriesCount method.  **Example:**     The following example retrieves the design geometries list of the manufacturing setup `CurrentSetup` in `ListOfDesignGeometriesProducts`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim DesignGeometriesListSize As Long
DesignGeometriesListSize = CurrentSetup.DesignGeometriesCount
If DesignGeometriesListSize > 0 Then
  Dim ListOfDesignGeometries() As Variant
  Redim ListOfDesignGeometries(DesignGeometriesListSize-1)
  CurrentSetup.ListDesignGeometriesProducts(ListOfDesignGeometriesProducts)
End If

```

### Sub **ListFixtureGeometries**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfFixtureGeometries`)

Retrieves the fixture geometries list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfFixtureGeometries`      The retrieved list.
The array must be previously initialized using the
FixtureGeometriesCount method.  **Example:**     The following example retrieves the fixture geometries list of the manufacturing setup `CurrentSetup` in `ListOfFixtureGeometries`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim FixtureGeometriesListSize As Long
FixtureGeometriesListSize = CurrentSetup.FixtureGeometriesCount
If FixtureGeometriesListSize > 0 Then
  Dim ListOfFixtureGeometries() As Variant
  Redim ListOfFixtureGeometries(FixtureGeometriesListSize-1)
  CurrentSetup.ListFixtureGeometries(ListOfFixtureGeometries)
End If

```

### Sub **ListFixtureGeometriesProducts**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfFixtureGeometriesProducts`)

Retrieves the Fixture geometries products list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfFixtureGeometriesProducts`      The retrieved list.
The array must be previously initialized using the
FixtureGeometriesCount method.  **Example:**     The following example retrieves the Fixture geometries list of the manufacturing setup `CurrentSetup` in `ListOfFixtureGeometriesProducts`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim FixtureGeometriesListSize As Long
FixtureGeometriesListSize = CurrentSetup.FixtureGeometriesCount
If FixtureGeometriesListSize > 0 Then
  Dim ListOfFixtureGeometries() As Variant
  Redim ListOfFixtureGeometries(FixtureGeometriesListSize-1)
  CurrentSetup.ListFixtureGeometriesProducts(ListOfFixtureGeometriesProducts)
End If

```

### Sub **ListInProcessModelBodies**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfIPMBodies`)

Retrieves the In Process Model Bodies list from a Manufacturing Setup.

**Parameters:**

` oListOfIPMBodies`      The retrieved list.
The array must be previously initialized using the
InProcessModelBodiesCount method.  **Example:**     The following example retrieves the In Process Model Bodies list of the manufacturing setup `CurrentSetup` in `ListOfIPMBodies`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim IPMBodiesListSize As Long
IPMBodiesListSize = CurrentSetup.InProcessModelBodiesCount
If IPMBodiesListSize > 0 Then
  Dim ListOfIPMBodies() As Variant
  Redim ListOfIPMBodies(IPMBodiesListSize-1)
  CurrentSetup.ListInProcessModelBodies(ListOfIPMBodies)
End If

```

### Sub **ListStockGeometries**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfStockGeometries`)

Retrieves the stock geometries list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfStockGeometries`      The retrieved list.
The array must be previously initialized using the
StockGeometriesCount method.  **Example:**     The following example retrieves the stock geometries list of the manufacturing setup `CurrentSetup` in `ListOfStockGeometries`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim StockGeometriesListSize As Long
StockGeometriesListSize = CurrentSetup.StockGeometriesCount
If StockGeometriesListSize > 0 Then
  Dim ListOfStockGeometries() As Variant
  Redim ListOfStockGeometries(StockGeometriesListSize-1)
  CurrentSetup.ListStockGeometries(ListOfStockGeometries)
End If

```

### Sub **ListStockGeometriesProducts**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfStockGeometriesProducts`)

Retrieves the Stock geometries products list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfStockGeometriesProducts`      The retrieved list.
The array must be previously initialized using the
StockGeometriesCount method.  **Example:**     The following example retrieves the Stock geometries list of the manufacturing setup `CurrentSetup` in `ListOfStockGeometriesProducts`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim StockGeometriesListSize As Long
StockGeometriesListSize = CurrentSetup.StockGeometriesCount
If StockGeometriesListSize > 0 Then
  Dim ListOfStockGeometries() As Variant
  Redim ListOfStockGeometries(StockGeometriesListSize-1)
  CurrentSetup.ListStockGeometriesProducts(ListOfStockGeometriesProducts)
End If

```

### Sub **SetProductAndReconciliate**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

Associate the Product to a Manufacturing Setup and reconciliate links.

**Example:**     The following example associates the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.SetProductAndReconciliate(iProduct)

```

### Sub **SetSafetyPlane**( [CATIABase](../System/interface_AnyObject_17321.md)  `iSafetyPlane`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

Associates a Safety Plane to a Manufacturing Setup.

**Example:**     The following example associates the Safety Plane `iSafetyPlane` belonging to the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.SetSafetyPlane(iSafetyPlane,iProduct)

```

### Sub **SetStock**( [CATIABase](../System/interface_AnyObject_17321.md)  `iStock`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

Associates a stock to a Manufacturing Setup.
The stock must be either a Body feature (Geometrical Set, Ordered Geometrical Set, PartBody, Body.n) either a CGR product.

**Example:**     The following example associates the stock `iStock` belonging to the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.SetStock(iStock,iProduct)

```

### Sub **SetToolChangePoint**( double  `iX`,  double  `iY`,  double  `iZ`)

Initialise the ToolChange point of the machine linked to a Manufacturing Setup.

**Example:**     The following example initialise the point with coordinates `X,Y,Z` as ToolChangePoint in the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.SetToolChangePoint(X,Y,Z)

```

### Sub **SetToolChangePointByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPointName`)

Initialise the ToolChange point of the machine linked to a Manufacturing Setup.

**Example:**     The following example initialise the point `PT23` as ToolChangePoint in the manufacturing setup `CurrentSetup`

```VBScript
call CurrentSetup.SetToolChangePointByName(PT23)

```

### Func **StockGeometriesCount**( ) As long

Returns the number of stock geometries from a Manufacturing Setup.

**Parameters:**

` oStockGeometriesListSize`      The number of stock geometries of this setup  **Example:**     The following example retrieves the number of stock geometries of the setup `CurrentSetup` in `StockGeometriesListSize`.

```VBScript
Dim CurrentSetup As ManufacturingSetup
Set CurrentSetup = ...
Dim StockGeometriesListSize As Long
StockGeometriesListSize = CurrentSetup.StockGeometriesCount

```