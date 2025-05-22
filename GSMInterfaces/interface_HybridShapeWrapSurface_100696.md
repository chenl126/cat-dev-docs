# HybridShapeWrapSurface (Object)

**_Represents the hybrid shape wrap surface object._**
**Role** : To access the data of the hybrid shape wrap surface object.

This data includes:

  * Two definition surfaces (refrence and target), who define the deformation

Use the CATIAHybridShapeFactory to create a HybridShapeWrapSurface object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **DeformationMode**( ) As long

Returns or sets whether the wrap surface is or should be created as a"Normal" or with a "3D" deformation mode.
**Legal values** : 2 for the normal solution and 1 for 3D solution.

**Example:**      This example sets the mode to create the wrap surface `hybWrapSurface` with a 3D deformation mode.

```VBScript
hybWrapSurface.3D deformation mode = 1

```

### Property **ReferenceSurface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference surface of the WrapSurface.

**Example** :      This example retrieves in `ReferenceSurface` the surface to deform of the `ShpWrapSurface` hybrid shape WrapSurface feature.

```VBScript
ReferenceSurface = ShpWrapSurface.Surface

```

### Property **Surface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference surface to deform of the WrapSurface.

**Example** :      This example retrieves in `SurfaceToDeform` the surface to deform of the `ShpWrapSurface` hybrid shape WrapSurface feature.

```VBScript
SurfaceToDeform = ShpWrapSurface.Surface

```

### Property **TargetSurface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the target surface of the WrapSurface.

**Example** :      This example retrieves in `TargetSurface` the surface to deform of the `ShpWrapSurface` hybrid shape WrapSurface feature.

```VBScript
TargetSurface = ShpWrapSurface.Surface

```