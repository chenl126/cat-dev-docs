# ArrangementRun (Object)

**_Use this object to access the properties and methods of an ArrangementRun object._**
**Role:** Use this interface to control the visualization mode, section parameters, nodes that define the ArrangementRun object.

## Properties

### Property **ArrangementNodes**( ) As [CATIAArrangementNodes](../CATArrangementInterfaces/interface_ArrangementNodes_54698.md) (Read Only)

Returns the ArrangementNodes that make up the ArrangementRun.

**Example:**      This example gets the ArrangementNodes for the `objRun1` object.

```VBScript
Dim objArrNodes   As ArrangementNodes
Set objArrNodes = objRun1.ArrangementNodes

```

### Property **Length**( ) As double (Read Only)

Returns the length of the ArrangementRun object.

**Example:**      This example retrieves the Length of the `objRun1` object.

```VBScript
Dim dblLength   As Double
dblLength  = objRun1.Length

```

### Property **SectionDiameter**( ) As double

Returns or sets the SectionDiameter for an ArrangementRun object.

**Example:**      This example retrieves the SectionDiameter for the `objRun1` object.

```VBScript
Dim dblSectionDia   As Double
dblSectionDia = objRun1.SectionDiameter

```

### Property **SectionHeight**( ) As double

Returns or sets the SectionHeight for an ArrangementRun object.

**Example:**      This example gets the SectionHeight for the `objRun1` object.

```VBScript
Dim dblSectionHeight   As Double
dblSectionHeight = objRun1.SectionHeight

```

### Property **SectionType**( ) As [CATArrangementRouteSection](../CATArrangementInterfaces/enum_CATArrangementRouteSection_141224.md)

Returns or sets the SectionType for an ArrangementRun object.

**Example:**      This example sets the SectionType for the `objRun1` object to `CatArrangementRouteSectionRectangular`.

```VBScript
objRun1.SectionType = CatArrangementRouteSectionRectangular

```

### Property **SectionWidth**( ) As double

Returns or sets the SectionWidth for an ArrangementRun object.

**Example:**      This example gets the SectionWidth for the `objRun1` object.

```VBScript
Dim dblSectionWidth   As Double
dblSectionWidth = objRun1.SectionWidth

```

### Property **VisuMode**( ) As [CATArrangementRouteVisuMode](../CATArrangementInterfaces/enum_CATArrangementRouteVisuMode_150809.md)

Returns or sets the Visualization Mode for an ArrangementRun object.

**Example:**      This example sets the Visualization Mode for the `objRun1` object to `CatArrangementRouteVisuModeSolid`.

```VBScript
objRun1.VisuMode = CatArrangementRouteVisuModeSolid

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns the applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objRun1` object.

```VBScript
Dim objProd   As Product
objProd  = objRun1.GetTechnologicalObject("Product")

```