# ArrangementItemReservation (Object)

**_Use this object to access the ArrangementItemReservation properties and methods._**
**Role:** Use this object to control the visualization mode, dimensions of the ArrangementItemReservation.

## Properties

### Property **Height**( ) As double

Returns or sets the height of the ArrangementItemReservation.

**Example:**      This example retrieves the Height of the `objItemRes1` object.

```VBScript
Dim dblHeight   As Double
dblHeight  = objItemRes1.Height

```

### Property **VisuMode**( ) As [CATArrangementItemResVisuMode](../CATArrangementInterfaces/enum_CATArrangementItemResVisuMode_171619.md)

Returns or set the Visualization Mode for the ArrangementItemReservation.

**Example:**      This example Sets the Visualization Mode of the `objItemRes1` object to ` CatArrangementItemReservationVisuModeBox `.

```VBScript
objItemRes1.VisuMode = CatArrangementItemReservationVisuModeBox

```

### Property **XLength**( ) As double

Returns or sets the XLength of the ArrangementItemReservation.

**Example:**      This example retrieves the XLength of the `objItemRes1` object.

```VBScript
Dim dblXLength   As Double
dblXLength  = objItemRes1.XLength

```

### Property **YLength**( ) As double

Returns or sets the YLength of the ArrangementItemReservation.

**Example:**      This example retrieves the YLength of the `objItemRes1` object.

```VBScript
Dim dblYLength   As Double
dblYLength  = objItemRes1.YLength

```

Methods

### Sub **GetDimension**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioItemResDimensions`)

Returns the Dimensions of the ArrangementItemReservation.

**Parameters:**

` ioItemResDimensions`      The output array initialized with the dimensions that make up the ArrangementItemReservation. The first three components represent the Minimum XCoord, YCoord and Z Coord while the remaining three components represent the Maximum XCoord, YCoord and Z Coord respectively.

**Example:**      This example retrieves the coordinate dimensions of the `objItemRes1` object.

```VBScript
Dim dblDimension(6)   As Double
objItemRes1.GetDimension(dblDimension)

```

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns the applicative data whose type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objItemRes1` object.

```VBScript
Dim objProd   As Product
objProd  = objItemRes1.GetTechnologicalObject("Product")

```

### Sub **SetDimension**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iItemResDimensions`)

Sets the Dimensions of the ArrangementItemReservation.

**Parameters:**

` iItemResDimensions`      The input array initialized with the dimensions that make up the ArrangementItemReservation. The first three components represent the Minimum XCoord, YCoord and Z Coord while the remaining three components represent the Maximum XCoord, YCoord and Z Coord respectively.

**Example:**      This example sets the coordinate dimensions of the `objItemRes1` object.

```VBScript
Dim dblDimension(6)   As Double
dblDimension(0)       = 300.0 '//XMin
dblDimension(1)       = 500.0 '//YMin
dblDimension(2)       = 300.0 '//ZMin
dblDimension(3)       = 500.0 '//XMax
dblDimension(4)       = 0.0   '//YMax
dblDimension(5)       = 300.0 '//ZMax
objItemRes1.SetDimension(dblDimension)

```