# ManufacturingSurfaceGeomArea (Object)

**_Represents the Manufacturing Surface NCGeometry._**

**Role** : Allows you to associate geometries with a NCGeometry.

## Methods

### Sub **RemoveAllGeometry**(| )

   Removes all the geometry linked to a Manufacturing Surface NCGeometry feature.

**Example:** The following example removes the geometry of the manufacturing surface NCGeometry feature `CurrentNCGeomArea`

```VBScript
     Call CurrentNCGeomArea.RemoveAllGeometry()

```

### Sub **SetGeometry**( [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`)

   Sets a geometry of a Manufacturing Surface NCGeometry feature.

**Parameters:**

` iReference`      The geometry to be set.
` iProduct`      The product containing the geometry to be set.

**Example:** The following example sets a geometry `Geometry1` to the manufacturing surface NCGeometry feature `CurrentNCGeomArea`

```VBScript
     Call CurrentNCGeomArea.SetGeometry(Geometry1,PartMachined)

```