# Mirror (Object)

**_Represents the mirror shape._**
It duplicates a shape with respect to a planar mirroring element, such as a planar face or a plane.

## Properties

### Property **MirroringObject**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

Returns the mirroring Object.  
### Property **MirroringPlane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the mirroring reference plane. It can be a plane, or a plane face.
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).

**Example:**     The following example returns in `ref` the mirroring reference plane of the mirroring `firstMirroring`, and then sets it to the created `MyRef`:

```VBScript
Set ref = firstMirroring.MirroringPlane
Set MyRef = part.CreateReferenceFromGeometry (plane)
firstMirroring.**MirroringPlane** = MyRef

```