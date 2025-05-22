# HybridShapeTrim (Object)

**_Represents the hybrid shape trim object._**
**Role** : To access the data of the hybrid shape trim object. This data includes:

  * The first element (surface or curve) to be trimmed
  * The second element (surface or curve) to be trimmed
  * The orientation corresponding to the first element
  * The orientation corresponding to the second element

Use the CATIAHybridShapeFactory to create a HybridShapeTrim object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **AutomaticExtrapolationMode**( ) As boolean

Gets or sets the automatic extrapolation mode status. AutomaticExtrapolationMode = TRUE : Automatic extrapolation mode is on. = FALSE : Automatic extrapolation mode is off. This example retrieves in `AutoExtrapolMode` the automatic extrapolation mode status for the `Trim` hybrid shape feature.

```VBScript
Dim AutoExtrapolMode As boolean
AutoExtrapolMode = Trim.AutomaticExtrapolationMode

```

### Property **Connex**( ) As boolean

Gets or sets connected mode. Connex = TRUE : the check of connexity is enable. Connex = FALSE : the check of connexity is disable. This example retrieves in `Connex` the connected mode for the `Trim` hybrid shape feature.

```VBScript
Dim Connex As boolean
Connex = Trim.Connex

```

### Property **FirstElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Deprecated:**      V5R17 CATIAHybridShapeTrim#GetElem Returns or sets the first element to be trimmed.  **Example:**      This example retrieves in `Surface1` the first element to be trimmed for the `hybTrim` hybrid shape feature.

```VBScript
Dim Surface1 As Reference
Set Surface1 = hybTrim.FirstElem

```

### Property **FirstOrientation**( ) As long

**Deprecated:**      V5R17 CATIAHybridShapeTrim#GetPreviousOrientation Returns or sets the first orientation used to compute the trim.
**Role** : The orientation specifies the kept parts of the first element to be trimmed.

  * When trimming surfaces:
    * If orientation value is 1: kept parts are specified by the "natural" normal to the second object
    * If orientation value is -1: kept parts are specified by the inverse of the "natural" normal to the second object
  * When trimming curves:
    * If orientation value is 1: kept parts are from the beginning of the curve to the first intersection, and, if there is one, from the second to the third intersection and so on until the end of the curve
    * If orientation value is -1: kept parts are from the first intersection to the second (if there is one), and, if there is one, from the third to the fourth and so on until the end of the curve.

**Example:**      This example retrieves in `firstOrient` the orientation of the first element used by the `hybTrim` hybrid shape feature.

```VBScript
Dim firstOrient As long
Set firstOrient = hybTrim.FirstOrientation

```

### Property **IntersectionComputation**( ) As boolean

Gets or sets Intersection computation mode. IntersectionComputation = TRUE : Intersection is computed. = FALSE : Intersection is not computed. This example retrieves in `Intersection` the Intersection computation mode for the `Trim` hybrid shape feature.

```VBScript
Dim Intersection As boolean
Intersection = Trim.IntersectionComputation

```

### Property **Manifold**( ) As boolean

Gets or sets manifold mode. Manifold = TRUE : the check of manifold is enable. Manifold = FALSE : the check of manifold is disable. This example retrieves in `Manifold` the manifold mode for the `Trim` hybrid shape feature.

```VBScript
Dim Manifold As boolean
Connex = Trim.Manifold

```

### Property **Mode**( ) As long

Gets or sets Trim mode. Mode = 1 : Standard. = 2 : Pieces. This example retrieves in `Mode` the mode for the `Trim` hybrid shape feature.

```VBScript
Dim Mode As long
Mode = Trim.Mode

```

### Property **SecondElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Deprecated:**      V5R17 CATIAHybridShapeTrim#GetElem Returns or sets the second element to be trimmed.  **Example:**      This example retrieves in `Surface2` the second element to be trimmed for the `hybTrim` hybrid shape trim object.

```VBScript
Dim Surface2 As Reference
Set Surface2 = hybTrim.SecondElem

```

### Property **SecondOrientation**( ) As long

**Deprecated:**      V5R17 CATIAHybridShapeTrim#GetPreviousOrientation Returns or sets the second orientation used to compute the trim.
**Role** : The orientation specifies the kept parts of the second element to be trimmed.

  * When trimming surfaces:
    * If orientation value is 1: kept parts are specified by the "natural" normal to the first object
    * If orientation value is -1: kept parts are specified by the inverse of the "natural" normal to the first object
  * When trimming curves:
    * If orientation value is 1: kept parts are from the beginning of the curve to the first intersection, and, if there is one, from the second to the third intersection and so on until the end of the curve
    * If orientation value is -1: kept parts are from the first intersection to the second (if there is one), and, if there is one, from the third to the fourth and so on until the end of the curve.

**Example:**      This example retrieves in `secondOrient` the orientation of the second element used by the `hybTrim` hybrid shape trim object.

```VBScript
Dim secondOrient As long
Set secondOrient = hybTrim.SecondOrientation

```

### Property **Simplify**( ) As boolean

Returns or sets whether the simplification of the resulting topology is or should be activated.
**Legal values** : True to activate the simplification, and False otherwise.

**Example:**      This example activates the simplification of the resulting topology of the `hybTrim` hybrid shape trim object.

```VBScript
 hybTrim.Simplify = True

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support element.
This support element may not exist.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example:**      This example retrieves in `supportElement` the support element of the `hybTrim` hybrid shape trim object.

```VBScript
Dim supportElement As Reference
Set supportElement = hybTrim.Support

```

Methods

### Sub **AddElementToKeep**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

Adds an element to specifications. This element will be kept.

**Parameters:**

` iElement`      Element to keep.

### Sub **AddElementToRemove**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

Adds an element to specifications. This element will be removed.

**Parameters:**

` iElement`      Element to remove.

### Func **GetElem**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the trimmed feature at a given index.

**Parameters:**

` iRank`      Index of one of the trimmed features
` oElem`      trimmed feature

### Func **GetKeptElem**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the kept feature at a given index.

**Parameters:**

` oElem`      Kept feature
` iRank`      Index of one of the kept features

### Func **GetNbElem**( ) As long

Gets the number of elements: couple(element, index of portion to keep on element).

**Parameters:**

` oNbElem`      Number of elements

### Func **GetNbElementsToKeep**( ) As long

Gets the number of elements to keep.

**Parameters:**

` oNbElementsToKeep`      Number of elements to keep

### Func **GetNbElementsToRemove**( ) As long

Gets the number of elements to remove.

**Parameters:**

` oNbElementsToRemove`      Number of elements to remove

### Func **GetNextOrientation**( long  `iRank`) As long

Gets Orientation used to compute the feature, referring to the next trimmed element.

**Parameters:**

` oOrientation`      Orientation
` iRank`      index of the trimmed feature

### Func **GetPortionToKeep**( long  `iRank`) As long

Gets a portion to keep number, giving the index of the element.

**Parameters:**

` oPortionNumber`      Index of portion to keep on the element
` iRank`      Index of the trimmed element

### Func **GetPreviousOrientation**( long  `iRank`) As long

Gets Orientation used to compute the feature, referring to the previous trimmed element.

**Parameters:**

` iRank`      index of the trimmed feature
` oOrientation`      Orientation

### Func **GetRemovedElem**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the removed feature at a given index.

**Parameters:**

` oElem`      Removed feature
` iRank`      Index of one of the removed features

### Sub **InvertFirstOrientation**( )

**Deprecated:**      V5R17 CATIAHybridShapeTrim#SetPreviousOrientation Inverts the first orientation used to compute the trim.  **Example:**      This example inverts the first orientation to compute the `hybTrim` hybrid shape trim object.

```VBScript
hybTrim.InvertFirstOrientation

```

### Sub **InvertSecondOrientation**( )

**Deprecated:**      V5R17 CATIAHybridShapeTrim#SetPreviousOrientation Inverts the second orientation used to compute the trim. This example inverts the first orientation to compute the `hybTrim` hybrid shape trim object.

```VBScript
hybTrim.InvertSecondOrientation

```

### Sub **RemoveElementToKeep**( long  `iRank`)

Removes an element from specifications.

**Parameters:**

` iRank`      Index of the kept element.

### Sub **RemoveElementToRemove**( long  `iRank`)

Removes an element from specifications.

**Parameters:**

` iRank`      Index of the removed element.

### Sub **SetElem**( long  `iRank`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`)

Modifies the trimmed feature at a given index. Use AddElem method to specify a new trimmed element

**Parameters:**

` iRank`      Index of one of the trimmed features
` iElem`      trimmed feature

### Sub **SetNextOrientation**( long  `iRank`,  long  `iOrientation`)

Sets the orientation used to compute the feature, referring to the next trimmed element.

**Parameters:**

` iRank`      index of the feature
` iOrientation`      Orientation

### Sub **SetPortionToKeep**( long  `iRank`,  long  `iPortionNumber`)

Sets a portion to keep number in Pieces mode.

**Parameters:**

` iRank`      Index of the trimmed element
` iPortionNumber`      Index of portion to keep on the element

### Sub **SetPreviousOrientation**( long  `iRank`,  long  `iOrientation`)

Sets the orientation used to compute the feature, referring to the previous trimmed element.

**Parameters:**

` iRank`      index of the feature
` iOrientation`      Orientation