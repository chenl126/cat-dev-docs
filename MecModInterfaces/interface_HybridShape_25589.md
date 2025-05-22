# HybridShape (Object)

**_Represents the hybrid shape object._**

## Properties

### Property **Thickness**( ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

Returns the thickness of the hybrid shape.
The thickness is a CATIAHybridShapeThickness.

**Example:**     The following example returns the thickness `ExtrudeThickness` of the extrude `Extrude.1` as the origin point of the axis system `AxisSystem0`:

```VBScript
Dim Extrude1 As AnyObject
Set Extrude1 = HybridBody1.HybridShapes.Item  ( "Extrude.1" )
Dim Thickness1 As HybridShapeThickness
Set Thickness1 = Extrude1.Thickness

```

Methods

### Sub **AppendHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

Appends a hybrid shape to another hybrid shape.

**Parameters:**

` iHybridShape`      The hybrid shape to append.  **Example:**      This example appends the hybrid shape `newHybridShape` to the hybrid shape `oldHybridShape`:

```VBScript
oldHybridShape.AppendHybridShape (newHybridShape)

```

### Sub **Compute**( )

Computes the result of the hybrid shape.