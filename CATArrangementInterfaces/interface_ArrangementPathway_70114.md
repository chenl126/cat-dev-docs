# ArrangementPathway (Object)

**_Use this object to access properties and methods of an ArrangementPathway object._**
**Role:** Use this interface to control the visualization mode, section parameters, nodes that define the ArrangementPathway object.

## Properties

### Property **ArrangementNodes**( ) As [CATIAArrangementNodes](../CATArrangementInterfaces/interface_ArrangementNodes_54698.md) (Read Only)

Returns the ArrangementNodes that make up the ArrangementPathway.

**Example:**      This example gets the ArrangementNodes for the `objPathway1` object.

```VBScript
Dim objArrNodes   As ArrangementNodes
Set objArrNodes = objPathway1.ArrangementNodes

```

### Property **Length**( ) As double (Read Only)

Returns the length of the ArrangementPathway object.

**Example:**      This example retrieves the Length of the `objPathway1` object.

```VBScript
Dim dblLength   As Double
dblLength  = objPathway1.Length

```

### Property **SectionDiameter**( ) As double

Returns or sets the SectionDiameter for an ArrangementPathway object.

**Example:**      This example retrieves the SectionDiameter for the `objPathway1` object.

```VBScript
Dim dblSectionDia   As Double
dblSectionDia = objPathway1.SectionDiameter

```

### Property **SectionHeight**( ) As double

Returns or sets the SectionHeight for an ArrangementPathway object.

**Example:**      This example gets the SectionHeight for the `objPathway1` object.

```VBScript
Dim dblSectionHeight   As Double
dblSectionHeight = objPathway1.SectionHeight

```

### Property **SectionType**( ) As [CATArrangementRouteSection](../CATArrangementInterfaces/enum_CATArrangementRouteSection_141224.md)

Returns or sets the Section for an ArrangementPathway object.

**Example:**      This example sets the SectionType for the `objPathway1` object to `CatArrangementRouteSectionRectangular`.

```VBScript
objPathway1.SectionType = CatArrangementRouteSectionRectangular

```

### Property **SectionWidth**( ) As double

Returns or sets the SectionWidth for an ArrangementPathway object.

**Example:**      This example gets the SectionWidth for the `objPathway1` object.

```VBScript
Dim dblSectionWidth   As Double
dblSectionWidth = objPathway1.SectionWidth

```

### Property **VisuMode**( ) As [CATArrangementRouteVisuMode](../CATArrangementInterfaces/enum_CATArrangementRouteVisuMode_150809.md)

Returns or sets the Visualization Mode for an ArrangementPathway object.

**Example:**      This example sets the Visualization Mode for the `objPathway1` object to `CatArrangementRouteVisuModeSolid`.

```VBScript
objPathway1.VisuMode = CatArrangementRouteVisuModeSolid

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns the applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objPathway1` object.

```VBScript
Dim objProd   As Product
objProd  = objPathway1.GetTechnologicalObject("Product")

```