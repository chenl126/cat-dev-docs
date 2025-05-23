# HybridShapeAssemble (Object)

**_Represents the hybrid shape assemble feature object._**

**Role** : To access the data of the hybrid shape assemble feature object. This data includes:

  * A list of the assembled elements
  * Some methods to access this data

Use the CATIAHybridShapeFactory to create a HybridShapeAssemble object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Invert**(| ) As boolean

   Returns or sets the invert mode.

**Legal values** : **True** the result is inverted. **False** the result is not inverted.

**Example:**      This example sets the invert mode of the `HybShpAssemble` hybrid shape assemble feature to True.

```VBScript
     HybShpAssemble.Invert = True

```

Methods

### Sub **AddElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

   Adds an element to the hybrid shape assemble feature object.

**Parameters:**

` iElement`      The element to add to the hybrid shape assemble feature object.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  **Examples** :      The following example adds the `iElement` feature object to the `HybridShapeAssemble` object.

```VBScript
     HybridShapeAssemble.AddElement iElement

```

### Sub **AddSubElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSubElement`)

   Adds a sub element to the hybrid shape assemble feature object.

**Parameters:**

` iSubElement`      The sub element to remove to the hybrid shape assemble feature object.

### Sub **AppendFederatedElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

   Appends an init to the list of elements to federate.

**Parameters:**

` iElement`      Element to append.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) 
### Func **GetAngularTolerance**( ) As double

   Get the anglular tolerance.

**Parameters:**

` oValue`      The anglular tolerance.

### Func **GetAngularToleranceMode**( ) As boolean

   Get the anglular tolerance mode.

**Parameters:**

` oValue`      The anglular tolerance mode.

### Func **GetConnex**( ) As boolean

   Get the connex checker flag.

**Parameters:**

` oConnex`

### Func **GetDeviation**( ) As double

   Get the deviation value.

**Parameters:**

` odeviation`      The deviation.

### Func **GetElement**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Retrieves an element used by the hybrid shape assemble feature object.

**Parameters:**

` iRank`      The rank of the element to read.  **Examples** :      The following example gets the `oElement` feature object of the `HybridShapeAssemble` object at the position `iRank`.

```VBScript
     Dim oElement As Reference
     Set oElement = HybridShapeAssemble.GetElement (iRank).

```

### Func **GetElementsSize**( ) As long

   Returns the size of the list of elements to assemble in the hybrid shape assemble feature object.

**Parameters:**

` oSize`      Number of elements in the Assemble.

**Example** :      This example retrieves the number of elements in the `HybShpAssemble` hybrid shape assemble.

```VBScript
     Dim oSize As  long
     oSize = HybShpAssemble.GetElementsSize

```

### Func **GetFederatedElement**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Retrieves an federated inits used by the hybrid shape assemble feature object.

**Parameters:**

` iRank`      The rank of the element to read.
` oElement`      The federated element.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) 
### Func **GetFederatedElementsSize**( ) As long

   Gets the number of federated inits.

**Parameters:**

` Size`      Number of elements.

### Func **GetFederationPropagation**( ) As long

   Gets the propagation mode of the federation.

**Parameters:**

` i`      type of propagation (0: No, 1: All, 2: Continuity, 3:Tangency).

### Func **GetManifold**( ) As boolean

   Get the manifold checker flag.

**Parameters:**

` oManifold`

### Func **GetSimplify**( ) As boolean

   Get the simplify flag.

**Parameters:**

` oSimplify`

### Func **GetSubElement**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Retrieves a sub element used by the hybrid shape assemble feature object.

**Parameters:**

` iRank`      The rank of the subelement to read.

### Func **GetSubElementsSize**( ) As long

   Returns the size of the list of sub-elements to remove in the hybrid shape assemble feature object.

**Parameters:**

` oSize`      Number of sub elements in the Assemble.

**Example** :      This example retrieves the number of sub elements in the `HybShpAssemble` hybrid shape assemble.

```VBScript
     Dim oSize As  long
     oSize = HybShpAssemble.GetSubElementsSize

```

### Func **GetSuppressMode**( ) As boolean

   Get the SuppressMode flag.

**Parameters:**

` oSuppressMode`

### Func **GetTangencyContinuity**( ) As boolean

   Get the tangency continuity checker flag.

**Parameters:**

` oTangencyContinuity`

### Sub **RemoveElement**( long  `iRank`)

   Removes an element used by the hybrid shape assemble feature object.

**Parameters:**

` iRank`      The rank of the element to remove.  **Examples** :      The following example removes the feature object from the `HybridShapeAssemble` object at the position `iRank`.

```VBScript
     HybridShapeAssemble.RemoveElement iRank.

```

### Sub **RemoveFederatedElement**( long  `iRank`)

   Removes an element to the list of elements to federate.

**Parameters:**

` iRank`      Position of the element to remove.

### Sub **RemoveSubElement**( long  `iRank`)

   Removes a sub element used by the hybrid shape assemble feature object.

**Parameters:**

` iRank`      The rank of the element to remove.

### Sub **ReplaceElement**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

   Replaces the element at specified position in the hybrid shape assemble feature object.

**Parameters:**

` iPos`      Position at which the element should be replaced.
` iElement`      Reference of the element to be inserted.

**Example** :      This example replaces the element in the `HybShpAssemble` assemble feature at specified position `iPos`

```VBScript
     HybShpAssemble.ReplaceElement iPos,iElement

```

### Sub **SetAngularTolerance**( double  `iValue`)

   Set the anglular tolerance.

**Parameters:**

` iValue`      The anglular tolerance.

### Sub **SetAngularToleranceMode**( boolean  `iValue`)

   Set the anglular tolerance mode.

**Parameters:**

` iValue`      The anglular tolerance mode.

### Sub **SetConnex**( boolean  `iConnex`)

   Set the connex checker flag.

**Parameters:**

` iConnex`

### Sub **SetDeviation**( double  `ideviation`)

   Set the deviation value.

**Parameters:**

` ideviation`      The deviation.

### Sub **SetFederationPropagation**( long  `iMode`)

   Sets the propagation mode of federation.

**Parameters:**

` i`      type of propagation (0: No, 1: All, 2: Continuity, 3:Tangency).

### Sub **SetManifold**( boolean  `iManifold`)

   Set the manifold checker flag.

**Parameters:**

` iManifold`

### Sub **SetSimplify**( boolean  `iSimplify`)

   Set the simplify flag.

**Parameters:**

` iSimplify`

### Sub **SetSuppressMode**( boolean  `iSuppressMode`)

   Set the SuppressMode flag.

**Parameters:**

` iSuppressMode`

### Sub **SetTangencyContinuity**( boolean  `iTangencyContinuity`)

   Set the tangency continuity checker flag.

**Parameters:**

` iTangencyContinuity`