# ArrangementRectangle (Object)

**_Use this object to access the properties and methods of an ArrangementRectangle object._**

**Role** : The ArrangementRectangle object is a geometric shape used for defining Contours of Areas. The ArrangementRectangle is defined by width and length and its Product position (which is the min-x, min-y corner of the rectangle).

## Properties

### Property **XLength**(| ) As double

   Returns or sets the XLength of the ArrangementRectangle.

**Example:**      This example retrieves the XLength for the `objRectangle1` object.

```VBScript
     Dim dblXLength  As Double
     dblXLength = objRectangle1.XLength

```

### Property **YLength**( ) As double

   Returns or sets the YLength of the ArrangementRectangle.

**Example:**      This example retrieves the YLength for the `objRectangle1` object.

```VBScript
     Dim dblYLength  As Double
     dblYLength = objRectangle1.YLength

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objRectangle1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objRectangle1.GetTechnologicalObject("Product")

```