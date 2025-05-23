# ArrangementProduct (Object)

**_Use this object as a factory for Arrangement collection objects._**

**Role:** Use this interface to get access to the Arrangement collections (Areas, Rectangles, ItemReservations, Runs, Pathways, Boundaries) aggregated a given Product.

## Properties

### Property **ArrangementAreas**(| ) As [CATIAArrangementAreas](../CATArrangementInterfaces/interface_ArrangementAreas_54164.md) (Read Only)

   Returns the collection of ArrangementAreas under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementAreas collection, `oArrAreas `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrAreas As ArrangementAreas
     Set oArrAreas = objArrProd1.Areas

```

### Property **ArrangementBoundaries**( ) As [CATIAArrangementBoundaries](../CATArrangementInterfaces/interface_ArrangementBoundaries_94314.md) (Read Only)

   Returns the collection of ArrangementBoundaries under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementBoundaries collection, `oArrBoundaries `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrBoundaries As ArrangementBoundaries
     Set oArrBoundaries = objArrProd1.oArrObjType

```

### Property **ArrangementItemReservations**( ) As [CATIAArrangementItemReservations](../CATArrangementInterfaces/interface_ArrangementItemReservations_156900.md) (Read Only)

   Returns the collection of ArrangementItemReservations under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementItemReservations collection, `oArrItemReservations `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrItemReservations As ArrangementItemReservations
     Set oArrItemReservations = objArrProd1.ItemReservations

```

### Property **ArrangementPathways**( ) As [CATIAArrangementPathways](../CATArrangementInterfaces/interface_ArrangementPathways_78543.md) (Read Only)

   Returns the collection of ArrangementPathways under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementPathways collection, `oArrPathways `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrPathways As ArrangementPathways
     Set oArrPathways = objArrProd1.Pathways

```

### Property **ArrangementRectangles**( ) As [CATIAArrangementRectangles](../CATArrangementInterfaces/interface_ArrangementRectangles_94094.md) (Read Only)

   Returns the collection of ArrangementRectangles under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementRectangles collection, `oArrRectangles `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrRectangles As ArrangementRectangles
     Set oArrRectangles = objArrProd1.Rectangles

```

### Property **ArrangementRuns**( ) As [CATIAArrangementRuns](../CATArrangementInterfaces/interface_ArrangementRuns_49110.md) (Read Only)

   Returns the collection of ArrangementRuns under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementRuns collection, `oArrRuns `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrRuns As ArrangementRuns
     Set oArrRuns = objArrProd1.Runs

```

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the Type of the ArrangementProduct in the form of a String.

**Example:**      This example retrieves the type information as a string for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrObjType  As String
     oArrObjType  = objArrProd1.Type

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the product's applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objArrProd1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objArrProd1.GetTechnologicalObject("Product")

```

### Sub **SetArrangementNomenclature**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNomenclature`)

   Sets the nomenclature of the ArrangementProduct.

**Returns:**      An HRESULT value.

**Legal values** :

S_OK
    operation is successful
E_FAIL
    operation failed

**Example:**      This example sets the ArrangementNomenclature for `objArrProd1` ArrangementProduct object.

```VBScript
     objArrProd1.SetArrangementNomenclature = "Building"

```

### Sub **SetAutoName**( )

   Causes the name of the ArrangementProduct automatically.

**Returns:**      An HRESULT value.

**Legal values** :

S_OK
    operation is successful
E_FAIL
    operation failed

**Example:**      This example shows how the automatic naming of the `objArrProd1` ArrangementProduct object can be done.

```VBScript
     objArrProd1.SetAutoName

```