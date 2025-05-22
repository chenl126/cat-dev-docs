# Part (Object)

**_The root level object inside a PartDocument object._**
**Role** : It aggregates all the objects making up the part document.
It provides many factories and collections. The collections list only the direct children of the part. [Selection.Search](../InfInterfaces/interface_Selection_18040.htm#Search) allows to get all objects of one type.

**See also:**      [PartDocument](../MecModInterfaces/interface_PartDocument_31472.md)

## Properties

### Property **AnnotationSets**( ) As [CATIACollection](../System/interface_Collection_22150.md) (Read Only)

Returns the collection object containing the annotation sets. All the annotation sets that are aggregated in the part might be accessed thru that collection.

**Example:**     The following example returns in `annotationSets` the annotation sets of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim annotationSets As AnnotationSets
Set annotationSets = partRoot.AnnotationSets

```

### Property **AxisSystems**( ) As [CATIAAxisSystems](../MecModInterfaces/interface_AxisSystems_27251.md) (Read Only)

Returns the collection object containing the coordinate systems. All the coordinate systems that are aggregated in the part might be accessed thru that collection.

**Example:**     The following example returns in `axisSystems` the coordinate systems of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim axisSystems As AxisSystems
Set axisSystems = partRoot.AxisSystems

```

### Property **Bodies**( ) As [CATIABodies](../MecModInterfaces/interface_Bodies_7994.md) (Read Only)

Returns the collection object containing the bodies that are direct children of the part.
It does not return all the bodies of the part, particularly the bodies in a boolean operation.

**Example:**     The following example returns in `bodiesColl` the collection of the bodies of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Set bodiesColl = partRoot.Bodies

```

### Property **Constraints**( ) As [CATIAConstraints](../MecModInterfaces/interface_Constraints_27490.md) (Read Only)

Returns the collection object containing the part constraints. Only 3D constraints are concerned here, 2D constraints are managed in sketches.

**Example:**     The following example returns in `csts` the constraints of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Set csts = partRoot.Constraints

```

### Property **Density**( ) As double (Read Only)

Returns the part density.

**Example:**     The following example displays the density of the part:

```VBScript
Set partRoot = partDoc.Part
MsgBox "The density is " & partRoot.Density

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

Returns the collection object containing the part geometrical elements. Only 3D elements are concerned here, 2D elements are managed in sketches. The origin elements are also accessible thru that collection.

**Example:**     The following example returns in `geomElts` the 3D elements of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Set geomElts = partRoot.GeometricElements

```

### Property **HybridBodies**( ) As [CATIAHybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) (Read Only)

Returns the collection object containing the hybrid bodies that are direct children of the part.

**Example:**     The following example returns in `hybridBodiesColl` the collection of hybrid bodies of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Set hybridBodiesColl = partRoot.HybridBodies

```

### Property **HybridShapeFactory**( ) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md) (Read Only)

Returns the part hybrid shape factory. It allows the creation of hybrid shapes in the part.

**Example:**     The following example returns in `hybridShapeFact` the hybrid shape factory of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim hybridShapeFact As Factory
Set hybridShapeFact = partRoot.HybridShapeFactory

```

### Property **InWorkObject**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Returns or sets the in work object of the part. The in work object is the object after which a new object is added.

**Example:**

```VBScript
Set partRoot = partDoc.Part
Set partRoot.InWorkObject = cylindricPad
If ( partRoot.InWorkObject <> cylindricPad ) Then
     MsgBox "There is a big problem"
End If

```

### Property **MainBody**( ) As [CATIABody](../MecModInterfaces/interface_Body_3736.md)

Returns or sets the main body of the part.

**Example:**     The following example returns the main body of the part of the current document.

```VBScript
Dim mainBody As Body
Set mainBody=CATIA.ActiveDocument.Part.MainBody

```

### Property **OrderedGeometricalSets**( ) As [CATIAOrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) (Read Only)

Returns the collection object containing the ordered geometrical sets of the part.

**Example:**     The following example returns in `ogsColl` the collection of ordered geometrical sets of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Set ogsColl = partRoot.OrderedGeometricalSets

```

### Property **OriginElements**( ) As [CATIAOriginElements](../MecModInterfaces/interface_OriginElements_42458.md) (Read Only)

Returns the object defining the part 3D reference axis system.

**Example:**     The following example returns in `originElts` the origin of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Set originElts = partRoot.OriginElements

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

Returns the collection object containing the part parameters. All the parameters that are aggregated in the different objects of the part might be accessed thru that collection.

**Example:**     The following example returns in `params` the parameters of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim params As Parameters
Set params = partRoot.Parameters

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

Returns the collection object containing the part relations. All the relations that are used to valuate the parameters of the part might be accessed thru that collection.

**Example:**     The following example returns in `rels` the relations of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Set rels = partRoot.Relations

```

### Property **ShapeFactory**( ) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md) (Read Only)

Returns the part shape factory. It allows the creation of shapes in the part.

**Example:**     The following example returns in `shapeFact` the shape factory of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim shapeFact As Factory
Set shapeFact = partRoot.ShapeFactory

```

### Property **SheetMetalFactory**( ) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md) (Read Only)

Returns the sheet metal factory of the part. It allows the creation of sheet metal elements in the part.

**Example:**     The following example returns in `sheetMetalFact` the sheet metal factory of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim sheetMetalFact As Factory
Set sheetMetalFact = partRoot.SheetMetalFactory

```

### Property **SheetMetalParameters**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

Returns the sheet metal parameters of the part.

**Example:**     The following example returns in `sheetMetalParm` the sheet metal parameters of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim sheetMetalParm As SheetMetalParameters
Set sheetMetalFact = partRoot.SheetMetalParameters

```

### Property **UserSurfaces**( ) As [CATIACollection](../System/interface_Collection_22150.md) (Read Only)

Returns the collection object containing the user surfaces. All the user surfaces that are aggregated in the part might be accessed thru that collection.

**Example:**     The following example returns in `userSurfaces` the user surfaces of the `partRoot` part from the `partDoc` part document:

```VBScript
Set partRoot = partDoc.Part
Dim userSurfaces As UserSurfaces
Set userSurfaces = partRoot.UserSurfaces

```

Methods

### Sub **Activate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

Unsuppresses an object for the update process. A unsuppressed object is again taken into account for the calculation of the part.

**Parameters:**

` iObject`      The object to unsuppress for the update process  **Example:**     The following example unsuppresses the `pad1` pad:

```VBScript
Set partRoot = partDoc.Part
Set pad1 = partRoot.FindObjectByName("Pad.1")
partRoot.Activate(pad1)

```

### Func **CreateReferenceFromBRepName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iObjectContext`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Creates a reference from a GenericNaming label. This allows manipulation of B-Rep (Type Functinal and Relimited) that are not easy to access.

**Parameters:**

` iLabel`      The GenericNaming identification for an object. This is a cryptic form for "the edge surrounded by the face extruded from line.12 of sketch.4 and the face...")
` iObjectContext`      The Object Context of Resolution This is the feature used for label GenericNaming resolution
**Returns:**      The reference to a B-Rep sub-element such a face or an edge  
### Func **CreateReferenceFromName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Creates a reference from a GenericNaming label. This allows manipulation of B-Rep (type Functional Only) that are not easy to access.

**Parameters:**

` iLabel`      The GenericNaming identification for an object. This is a cryptic form for "the edge surrounded by the face extruded from line.12 of sketch.4 and the face...")
**Returns:**      The reference to a B-Rep sub-element such a face or an edge  
### Func **CreateReferenceFromObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Creates a reference from a operator. Use of reference allows a uniform handling of B-Rep and non B-Rep objects.

**Parameters:**

` iObject`      The geometric object to be referenced. It can be a plane, a line or a point.
**Returns:**      The reference to the object. This way, a direction can be either an edge of a pad or a 3D line.  
### Func **FindObjectByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iObjName`) As [CATIABase](../System/interface_AnyObject_17321.md)

Finds an object that is not a collection by its name. Scan in depth among all the direct and indirect children (expensive, but hard to escape).

**Parameters:**

` iObjName`      The name to be searched
**Returns:**      The object, if found  **Example:**     The following example tests if the object was found:

```VBScript
Set partRoot = partDoc.Part
Set obj = partRoot.FindObjectByName("Wrong name")
If TypeName(obj)="Nothing" Then
     MsgBox "Object not found"
End If

```

### Func **GetCustomerFactory**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFactoryIID`) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md)

Returns a customer factory from a code string defined by the customer. It allows a customer to define its own factory to create its own objects.

**Parameters:**

` iFactoryIID`      The code name of the factory

### Sub **Inactivate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

Suppresses an object from being updated. A suppressed object is not taken into account for the calculation of the part.

**Parameters:**

` iObject`      The object to suppress from being updated  **Example:**     The following example suppresses the `pad1` pad from being updated:

```VBScript
Set partRoot = partDoc.Part
Set pad1 = partRoot.FindObjectByName("Pad.1")
partRoot.Inactivate(pad1)

```

### Func **IsInactive**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As boolean

Indicates whether an object is deactivated. A deactivated object is not taken into account for the calculation of the part.

**Parameters:**

` iObject`      The object to examine  **Example:**     The following example returns in `isInactive` whether the `pad1` pad is deactivated:

```VBScript
Set partRoot = partDoc.Part
Set pad1 = partRoot.FindObjectByName("Pad.1")
isInactive = partRoot.IsInactive(pad1)

```

### Func **IsUpToDate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As boolean

Indicates whether an object needs to be updated. An object which is not up-to-date has not be calculated with the last specifications.

**Parameters:**

` iObject`      The object to examine  **Example:**     The following example returns in `isuptodate` whether the `pad1` pad is up-to-date:

```VBScript
Set partRoot = partDoc.Part
Set pad1 = partRoot.FindObjectByName("Pad.1")
isuptodate = partRoot.IsUpToDate(pad1)

```

### Sub **Update**( )

Updates of the part result with respect to its specifications. Any composing specification that hasn't its result up-to-date will recompute it, thus propagating changes to the whole part.

**Example:**     The following example update the part:

```VBScript
Set partRoot = partDoc.Part
partRoot.Update

```

### Sub **UpdateObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

Updates an object with respect to its specifications. Any composing specification of the object that hasn't its result up-to-date will recompute it, thus propagating changes to the object.

**Parameters:**

` iObject`      The object to be updated  **Example:**     The following example updates Pad.1:

```VBScript
Set partRoot = partDoc.Part
Set pad1 = partRoot.FindObjectByName("Pad.1")
partRoot.UpdateObject(pad1)

```