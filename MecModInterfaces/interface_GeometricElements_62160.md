# GeometricElements (Collection)

**_A collection of all geometric elements contained in a part or a sketch._**
Geometric elements are created with the 2D factory for the sketch and with the 3D factory for the part. Geometric elements thus created are then aggregated either in the sketch or as part of the geometric element collection.

**See also:**      [Factory2D](../SketcherInterfaces/interface_Factory2D_15860.md), [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAGeometricElement](../SketcherInterfaces/interface_GeometricElement_54654.md)

Returns a geometric element using its index or its name from the GeometricElements collection.

**Parameters:**

` iIndex`      The index or the name of the geometric element to retrieve from the collection of geometric elements. As a numerics, this index is the rank of the geometric element in the collection. The index of the first geometric element in the collection is 1, and the index of the last geometric element is Count. As a string, it is the name you assigned to the geometric element using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved geometric element  **Example:**      This example retrieves the last item in the geometric element collection.

```VBScript
Set lastCst = cstList.Item(cstList.Count)

```