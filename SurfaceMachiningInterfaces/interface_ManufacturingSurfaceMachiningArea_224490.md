# ManufacturingSurfaceMachiningArea (Object)

**_Represents the Manufacturing Surface Machining Area._**

**Role** : Allows you to associate NCGeometries with a Machining Area.

## Methods

### Sub **RemoveNCGeometry**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iGeometryType`)

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