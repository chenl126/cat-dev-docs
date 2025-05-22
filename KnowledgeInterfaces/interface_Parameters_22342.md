# Parameters (Collection)

**_Represents the Parameters collection of the part or the product._**
The following example shows how to retrieve it:

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim parameterList As Parameters
 Set parameterList = part1.Part.Parameters

```

## Properties

### Property **RootParameterSet**( ) As [CATIAParameterSet](../KnowledgeInterfaces/interface_ParameterSet_31016.md) (Read Only)

Returns the root parameter set of a document. If it doesn't exist, it is created.  
### Property **Units**( ) As [CATIAUnits](../KnowledgeInterfaces/interface_Units_5973.md) (Read Only)

Returns the collection of units.  Methods

### Func **CreateBoolean**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  boolean  `iValue`) As [CATIABoolParam](../KnowledgeInterfaces/interface_BoolParam_17217.md)

Creates a boolean parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `checked` boolean parameter and adds it to the newly created part:

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim chk As BooleanParam
 Set chk = part1.Part.Parameters.CreateBoolean ("checked", False)

```

### Func **CreateDimension**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitude`,  double  `iValue`) As [CATIADimension](../KnowledgeInterfaces/interface_Dimension_18130.md)

Creates a user dimension and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The dimension name
` iMagnitude`      The dimension magnitude. Units are those of the IS system. Valid magnitudes are:

  * "LENGTH": the unit is the meter.
  * "ANGLE": the unit is the radian.
The
[Dimension](../KnowledgeInterfaces/interface_Dimension_18130.md) object provides the [Dimension.ValuateFromString](../KnowledgeInterfaces/interface_Dimension_18130.htm#ValuateFromString) method with which you may express the value in any unit for a given dimension (see the example below). ` iValue`      The dimension value provided as a real number  **Example:**      This example creates a `LENGTH` dimension and adds it to the newly created part. The initial value is expressed in meters. The new value is expressed in millimeters.

```VBScript
Dim depth As Dimension
Set depth = parameters.CreateDimension("depth", "LENGTH", 20)
depth.ValuateFromString("300mm");

```

### Func **CreateInteger**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  long  `iValue`) As [CATIAIntParam](../KnowledgeInterfaces/interface_IntParam_13730.md)

Creates an integer parameter** and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `RevisionNumber` integer parameter and adds it to the newly created part:

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim revision As IntParam
 Set revision = part1.Part.Parameters.CreateInteger ("RevisionRumber", 17)

```

### Func **CreateList**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAListParameter](../KnowledgeInterfaces/interface_ListParameter_36657.md)

Creates a list parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name  **Example:**      This example creates the `ListName` list parameter and adds it to the newly created part:

```VBScript
 Set CATDocs = CATIA.Documents
 Set part1   = CATDocs.Add("CATPart")
 Set list1 = part1.Part.Parameters.CreateList ("ListName")

```

### Func **CreateReal**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  double  `iValue`) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

Creates a real parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `ReliabilityRate` real parameter and adds it to the newly created part:

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim rate As RealParam
 Set rate = part1.Part.Parameters.CreateReal ("ReliabilityRate", 2.5 )

```

### Sub **CreateSetOfParameters**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFather`)

Creates a set of parameters and appends it to argument iFather.  
### Func **CreateString**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`) As [CATIAStrParam](../KnowledgeInterfaces/interface_StrParam_13874.md)

Creates a string parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `responsible` string parameter and adds it to the newly created part:

```VBScript
 Set CATDocs = CATIA.Documents
 Set part1   = CATDocs.Add("CATPart")
 Set density = part1.Part.Parameters.CreateString ("responsible", "The Boss")

```

### Func **GetNameToUseInRelation**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns a correct name of a feature to use it in a relation.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Retrieves a parameter using its index or its name from the from the Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the parameter to retrieve from the collection of parameters. As a numerics, this index is the rank of the parameter in the collection. The index of the first parameter in the collection is 1, and the index of the last parameter is Count. As a string, it is the name you assigned to the parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the parameter.  **Example:**      This example retrieves the last parameter in the `parameters` collection:

```VBScript
Set lastParameter = parameters.Item(parameters.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a parameter from the Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the parameter to remove from the collection of parameters. As a numerics, this index is the rank of the parameter in the collection. The index of the first parameter in the collection is 1, and the index of the last parameter is Count. As a string, it is the name you assigned to the parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the parameter.  **Example:**      This example removes the "depth" parameter from the `parameters` collection.

```VBScript
parameters.Remove("depth")

```

### Func **SubList**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`,  boolean  `iRecursively`) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md)

Returns a sub-collection of parameters aggregated to an object.

**Parameters:**

` iObject`      The object used to filter the whole parameter collection to get the resulting sub-collection.
` iRecursively`      A flag to specify if children parameters are to be searched for in the returned collection  **Example:**      This example shows how to retrieve a collection of parameters that are associated to a Pad.

```VBScript
Dim Parameters1 As Parameters
Set Parameters1 = CATIA.ActiveDocument.Part.Parameters gets the collection of parameters in the part
Dim Body0 As AnyObject
Set Body0 = CATIA.ActiveDocument.Part.Bodies.Item  ( "MechanicalTool.1" )
Dim Pad1 As AnyObject
Set Pad1 = Body0.Shapes.Item  ( "Pad.1" ) gets the pad Pad.1
Dim Parameters2 As Parameters
Set Parameters2 = Parameters1.SubList(Pad1,TRUE) gets the collection of parameters that are under the pad Pad.1

```