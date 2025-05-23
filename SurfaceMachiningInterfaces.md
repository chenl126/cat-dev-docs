# SurfaceMachiningInterfaces Framework

## Object Index

  * [ManufacturingSurfaceGeomArea](SurfaceMachiningInterfaces/interface_ManufacturingSurfaceGeomArea_161338.md)
  * [ManufacturingSurfaceMachiningArea](SurfaceMachiningInterfaces/interface_ManufacturingSurfaceMachiningArea_224490.md)

---

# ManufacturingSurfaceGeomArea (Object)

**_Represents the Manufacturing Surface NCGeometry._**

**Role** : Allows you to associate geometries with a NCGeometry.

## Methods

### Sub **RemoveAllGeometry**( )

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

---

# ManufacturingSurfaceMachiningArea (Object)

**_Represents the Manufacturing Surface Machining Area._**

**Role** : Allows you to associate NCGeometries with a Machining Area.

## Methods

### Sub **RemoveNCGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`)

   Removes all the NCGeometry of a specified type linked to a Manufacturing Surface Machining Area.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be

`GuidingElements`      to remove the limiting contour `Parts`      to remove the part to machine `Checks`      to remove the check elements

**Example:** The following example removes the part of the manufacturing surface machining area `CurrentSMA`

```VBScript
     Call CurrentSMA.RemoveNCGeometry("Parts")

```

### Sub **SetNCGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iNCGeometry`)

   Sets a NCGeometry of a specified type to a Manufacturing Surface Machining Area.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be

`GuidingElements`      to set the limiting contour `Parts`      to set the part to machine `Checks`      to set a check element
` iNCGeometry`      The NCGeometry to be set.

**Example:** The following example sets the NCGeometry `NCGeomPart` to the manufacturing surface machining area `CurrentSMA`

```VBScript
     Call CurrentSMA.SetNCGeometry("Parts",NCGeomPart)

```