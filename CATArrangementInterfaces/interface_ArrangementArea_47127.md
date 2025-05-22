# ArrangementArea (Object)

**_Use this object to access an ArrangementArea object's properties and functions._**
**Role:** The ArrangementArea object is a type of Arrangement Object defining an area containing other objects.

## Properties

### Property **ArrangementContours**( ) As [CATIAArrangementContours](../CATArrangementInterfaces/interface_ArrangementContours_79187.md) (Read Only)

Returns the ArrangementContours collection object associated with an ArrangementArea object.

**Example:**      This example retrieves the ArrangementContours collection object for the `objArea1` object.

```VBScript
Dim objArrContours   As ArrangementContours
Set objArrContours  = objArea1.ArrangementContours

```

### Property **Height**( ) As double

Returns or sets the Height of an ArrangementArea object.

**Example:**      This example retrieves the Height for the `objArea1` object.

```VBScript
Dim dblAreaHeight   As Double
dblAreaHeight  = objArea1.Height

```

### Property **Size**( ) As double (Read Only)

Returns the Size of the ArrangementArea.

**Example:**      This example retrieves the Size of the `objArea1` object.

```VBScript
Dim dblAreaSize   As Double
dblAreaSize  = objArea1.Size

```

### Property **VisuMode**( ) As [CATArrangementAreaVisuMode](../CATArrangementInterfaces/enum_CATArrangementAreaVisuMode_137110.md)

Returns or sets the Visualization Mode for an ArrangementArea object.

**Example:**      This example sets the Visualization Mode for the `objArea1` object to `CatArrangementAreaVisuModeVolume`.

```VBScript
objArea1.VisuMode = CatArrangementAreaVisuModeVolume

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns the applicative data whose type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
**Returns:**      oApplicativeObj The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objArea1` object.

```VBScript
Dim objProd   As Product
objProd  = objArea1.GetTechnologicalObject("Product")

```