# SketchBasedShape (Object)

**_Represents the shapes based on sketched 2D geometry._**
It is the base object for prisms, holes, revolutions, stiffeners, and sweeps.

**See also:**      [Prism](../PartInterfaces/interface_Prism_5871.md), [Hole](../PartInterfaces/interface_Hole_3612.md), [Revolution](../PartInterfaces/interface_Revolution_22940.md), [Stiffener](../PartInterfaces/interface_Stiffener_17922.md), [Sweep](../PartInterfaces/interface_Sweep_5756.md)

## Properties

### Property **Sketch**(| ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

   Returns the sketch the shape is based on.

**Example:**     The following example returns the sketch a pad named `firstPad` is based on:

```VBScript
     Set sketchPad = firstPad.Sketch

```

Methods

### Sub **SetProfileElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileElement`)

   Returns or sets a profile element.