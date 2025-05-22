# Sketches (Collection)

**_The body's collection of sketches not yet used by any shape._**

## Methods

### Func **Add**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)

Creates a new sketch and adds it to the sketch collection. The sketch creation implies to specify a supporting plane. Once created, the sketch exists, but is empty. You must use the [Sketch.OpenEdition](../SketcherInterfaces/interface_Sketch_8026.htm#OpenEdition) method to begin to edit it.

**Parameters:**

` iPlane`      The sketch supporting plane
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  **Returns:**      oNewSketch The created sketch  **Example:**      This example creates the `newSketch` sketch on the XY plane of the `myPart` part:

```VBScript
Set XYPlane = myPart.OriginElements.PlaneXY()
Set newSketch = myPart.Sketches.Add(XYPlane)

```

### Func **GetBoundary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIABoundary](../MecModInterfaces/interface_Boundary_14542.md)

Returns a boundary using its label.

**Parameters:**

` iLabel`      Identification of the
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. See [Reference.DisplayName](../InfInterfaces/interface_Reference_17481.htm#DisplayName).  **Returns:**      The retrieved boundary  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)

Returns a sketch using its index or its name from the Sketches collection.

**Parameters:**

` iIndex`      The index or the name of the sketch to retrieve from the collection of sketches. As a numerics, this index is the rank of the sketch in the collection. The index of the first sketch in the collection is 1, and the index of the last sketch is Count. As a string, it is the name you assigned to the sketch using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved sketch  **Example:**      This example retrieves the last item in the collection sketches.

```VBScript
Set lastSketch = sketchList.Item(sketchList.Count)

```