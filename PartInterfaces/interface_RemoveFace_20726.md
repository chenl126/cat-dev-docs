# RemoveFace (Object)

**_Represents the Remove Face operation._**
It removes a face or a set of faces.

## Properties

### Property **KeepFace**(| [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `iKeepFace`) (Write Only)

   Adds a new face to be Kept.

**Parameters:**

` iKeepFace`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  
### Property **KeepFaces**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Get the specified faces to be kept.  
### Property **Propagation**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Get the faces that will be removed.  
### Property **RemoveFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemoveFace`) (Write Only)

   Adds a new face to be removed.

**Parameters:**

` iRemoveFace`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  
### Property **RemoveFaces**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Get the specified faces to be removed.  Methods

### Sub **remove_KeepFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iKeepFace`)

   Removes a face to be Kept.

**Parameters:**

` iKeepFace`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  
### Sub **remove_RemoveFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemoveFace`)

   Removes a face to be removed.

**Parameters:**

` iRemoveFace`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).