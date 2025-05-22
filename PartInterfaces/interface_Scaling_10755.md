# Scaling (Object)

**_Represents the scaling shape._**
The scaling shape is made up of a scaling reference element, such as a point, and a scaling factor.

## Properties

### Property **Factor**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

Returns the scaling factor.

**Example:**     The following example returns in `factor` the scaling factor of the scaling `firstScaling`:

```VBScript
Set factor = firstScaling.Factor

```

### Property **ScalingReference**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the scaling reference element. It can be a point.
To set the property, you can use one of the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example:**     The following example returns in `ref` the scaling reference element of the scaling `firstScaling`, and then sets it to the created `MyRef`:

```VBScript
Set ref = firstScaling.ScalingSupport
Set MyRef = part.CreateReferenceFromGeometry (Point)
firstScaling.**ScalingSupport** = MyRef

```