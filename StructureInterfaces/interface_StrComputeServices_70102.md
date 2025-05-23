# StrComputeServices (Object)

**_Represents a structure service object._**
Structure service object extracts properties on structure objects.

## Methods

### Sub **GetCenterOfGravity**(| [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) | `iProduct`,| | double | `oX`,| | double | `oY`,| | double | `oZ`)

   Retreive the center of gravity for a structure object.

**Parameters:**

` iProduct`      The selected structure object
` oX`      The x coordinate of the center of gravity
` oY`      The y coordinate of the center of gravity
` oZ`      The z coordinate of the center of gravity

### Func **GetLength**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As double

   Returns the length to cut for a member object.

**Parameters:**

` iProduct`      The selected structure object

### Func **GetMass**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As double

   Returns the mass for a structure object.

**Parameters:**

` iProduct`      The selected structure object

### Func **GetMaterialName**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the material name for a structure object.

**Parameters:**

` iProduct`      The selected structure object
` oName`      The name of the material

### Func **GetSurface**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As double

   Returns the surface for a structure object.

**Parameters:**

` iProduct`      The selected structure object

### Func **GetVolume**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As double

   Returns the volume for a structure object.

**Parameters:**

` iProduct`      The selected structure object

### Func **GetWetArea**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As double

   Returns the wet area for a structure object.

**Parameters:**

` iProduct`      The selected structure object