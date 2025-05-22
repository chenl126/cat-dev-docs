# ArrangementBoundary (Object)

**_Access properties and functions of an ArrangementBoundary object._**
**Role:** Use this interface to control the visualization mode, section parameters, nodes that define the ArrangementBoundary object.

## Properties

### Property **ArrangementNodes**( ) As [CATIAArrangementNodes](../CATArrangementInterfaces/interface_ArrangementNodes_54698.md) (Read Only)

Returns the collection of ArrangementNodes that make up the ArrangementBoundary.

**Example:**      This example gets the ArrangementNodes for the `objBoundary1` object.

```VBScript
Dim objArrNodes   As ArrangementNodes
Set objArrNodes = objBoundary1.ArrangementNodes

```

### Property **Length**( ) As double (Read Only)

Returns the length of the ArrangementBoundary object.

**Example:**      This example retrieves the Length of the `objBoundary1` object.

```VBScript
Dim dblBoundaryLength   As Double
dblBoundaryLength  = objBoundary1.Length

```

### Property **SectionHeight**( ) As double

Returns or sets the SectionHeight for an ArrangementBoundary object.

**Example:**      This example gets the SectionHeight for the `objBoundary1` object.

```VBScript
Dim dblSectionHeight   As Double
dblSectionHeight = objBoundary1.SectionHeight

```

### Property **SectionType**( ) As [CATArrangementRouteSection](../CATArrangementInterfaces/enum_CATArrangementRouteSection_141224.md)

Returns or sets the SectionType for an ArrangementBoundary object.
**Legal values** :

CatArrangementRouteSectionNone
CatArrangementRouteSectionRectangular

**Example:**      This example sets the SectionType for the `objBoundary1` object to `CatArrangementRouteSectionRectangular`.

```VBScript
objBoundary1.SectionType = CatArrangementRouteSectionRectangular

```

### Property **SectionWidth**( ) As double

Returns or sets the SectionWidth for an ArrangementBoundary object.

**Example:**      This example gets the SectionWidth for the `objBoundary1` object.

```VBScript
Dim dblSectionWidth   As Double
dblSectionWidth = objBoundary1.SectionWidth

```

### Property **VisuMode**( ) As [CATArrangementRouteVisuMode](../CATArrangementInterfaces/enum_CATArrangementRouteVisuMode_150809.md)

Returns or sets the Visualization Mode for an ArrangementBoundary object.

**Example:**      This example sets the Visualization Mode for the `objBoundary1` object to `CatArrangementRouteVisuModeSolid`.

```VBScript
objBoundary1.VisuMode = CatArrangementRouteVisuModeSolid

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns the applicative data whose type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objBoundary1` object.

```VBScript
Dim objProd   As Product
objProd  = objBoundary1.GetTechnologicalObject("Product")

```