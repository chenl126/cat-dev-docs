# AssemblyFeatures (Collection)

**_A collection of all the AssemblyFeature objects of a product._**

**See also:**      [AssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

## Methods

### Func **AddAssemblyAdd**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBody`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iBodyComp`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

Creates a new AssemblyBoolean object by adding a body to the assembly.

**Parameters:**

` iBody`      The body to add
` iBodyComp`      The component that contains the body to add
` iComponent`      The component with respect to which the AssemblyBoolean object to create will be positioned
**Returns:**      The created [AssemblyBoolean](../CATAssemblyInterfaces/interface_AssemblyBoolean_47926.md) object  **Example:**      This example creates the `addBody` AssemblyBoolean object in the `assemblyFeats` collection using a body referenced as `bodyToAdd` contained in the `bodyToAddComp` component, and positioned with respect to the `positioningComp` component.

```VBScript
Dim addBody As AssemblyBoolean
Set addBody = assemblyFeats.AddAssemblyAdd(bodyToAdd,     _
                                           bodyToAddComp, _
                                           positioningComp)

```

### Func **AddAssemblyHole**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSketchComp`,  double  `iDepth`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

Creates a new AssemblyHole object.

**Parameters:**

` iSketch`      The sketch defining the hole reference plane and anchor point.
This sketch must contain a single point that defines the hole axis: the hole axis in 3D passes through that point and is normal to the sketch plane.
` iSketchComp`      The component that contains the sketch
` iDepth`      The hole depth
` iComponent`      The component with respect to which the AssemblyHole object to create will be positioned
**Returns:**      The created [AssemblyHole](../CATAssemblyInterfaces/interface_AssemblyHole_30806.md) object  **Example:**      This example creates the `hole` AssemblyHole object in the `assemblyFeats` collection using a sketch referenced as `holeSketch` contained in the `holeSketchComp` component, with a depth of 60mm, and positioned with respect to the `positioningComp` component.

```VBScript
Dim hole As AssemblyHole
Set hole = assemblyFeats.AddAssemblyHole(holeSketch,     _
                                         holeSketchComp, _
                                         60,             _
                                         positioningComp)

```

### Func **AddAssemblyPocket**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSketchComp`,  double  `iDepth`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

Creates a new AssemblyPocket object.

**Parameters:**

` iSketch`      The sketch defining the pocket base
` iSketchComp`      The component that contains the sketch
` iDepth`      The pocket depth
` iComponent`      The component with respect to which the AssemblyPocket object to create will be positioned
**Returns:**      The created [AssemblyPocket](../CATAssemblyInterfaces/interface_AssemblyPocket_42326.md) object  **Example:**      This example creates the `pocket` AssemblyPocket object in the `assemblyFeats` collection using a sketch referenced as `pocketSketch` contained in the `pocketSketchComp` component, with a depth of 20mm, and positioned with respect to the `positioningComp` component.

```VBScript
Dim pocket As AssemblyPocket
Set pocket = assemblyFeats.AddAssemblyPocket(pocketSketch,     _
                                             pocketSketchComp, _
                                             20,               _
                                             positioningComp)

```

### Func **AddAssemblyRemove**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBody`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iBodyComp`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

Creates a new AssemblyBoolean object by removing a body from the assembly.

**Parameters:**

` iBody`      The body to remove
` iBodyComp`      The component that contains the body to remove
` iComponent`      The component with respect to which the AssemblyBoolean object to create will be positioned
**Returns:**      The created [AssemblyBoolean](../CATAssemblyInterfaces/interface_AssemblyBoolean_47926.md) object  **Example:**      This example creates the `removeBody` AssemblyBoolean object in the `assemblyFeats` collection using a body referenced as `bodyToRemove` contained in the `bodyToRemoveComp` component, and positioned with respect to the `positioningComp` component.

```VBScript
Dim removeBody As AssemblyBoolean
Set removeBody = assemblyFeats.AddAssemblyRemove(bodyToRemove,     _
                                                 bodyToRemoveComp, _
                                                 positioningComp)

```

### Func **AddAssemblySplit**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSplittingElement`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSplittingElemComp`,  [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)  `iSplitSide`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

Creates a new AssemblySplit object.

**Parameters:**

` iSplittingElement`      The face or plane that will split the current body
` iSplittingElemComp`      The component that contains the splitting element
` iSplitSide`      The specification for which side of the current body should be kept at the end of the split operation
` iComponent`      The component with respect to which the AssemblySplit object to create will be positioned
**Returns:**      The created [AssemblySplit](../CATAssemblyInterfaces/interface_AssemblySplit_37076.md) object  **Example:**      This example creates the `splitByPlane` AssemblySplit object in the `assemblyFeats` collection using a plane referenced as `splittingPlane` contained in the `splittingComp` component, in such a way that the material to remove be the one located in the direction of the `splittingPlane` normal vector, and positioned with respect to the `positioningComp` component.

```VBScript
Dim splitByPlane As AssemblySplit
Set splitByPlane = assemblyFeats.AddAssemblySplit(splittingPlane,  _
                                                  splittingComp,   _
                                                  catPositiveSide, _
                                                  positioningComp)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

Returns an AssemblyFeature object using its index or its name from the AssemblyFeatures collection.

**Parameters:**

` iIndex`      The index or the name of the AssemblyFeature object to retrieve from the AssemblyFeatures collection. As a numerics, this index is the rank of the AssemblyFeature object in the collection. The index of the first AssemblyFeature object in the collection is 1, and the index of the last AssemblyFeature object is Count. As a string, it is the name you assigned to the AssemblyFeature object using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved AssemblyFeature object  **Example:**      This example retrieves the last item in the `assemblyFeats` collection.

```VBScript
Dim lastAssemblyFeat As AssemblyFeature
Set lastAssemblyFeat = assemblyFeats.Item(assemblyFeats.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes an AssemblyFeature object from the AssemblyFeatures collection.

**Parameters:**

` iIndex`      The index or the name of the AssemblyFeature object to remove from the AssemblyFeatures collection. As a numerics, this index is the rank of the AssemblyFeature object in the collection. The index of the first AssemblyFeature object in the collection is 1, and the index of the last AssemblyFeature object is Count. As a string, it is the name you assigned to the AssemblyFeature object using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last AssemblyFeature object in the `assemblyFeats` collection.

```VBScript
assemblyFeats.Remove(assemblyFeats.Count)

```