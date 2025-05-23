# RenderingEnvironments (Collection)

**_A collection of all the Rendering Environments objects._**

## Methods

### Func **Add**(| short | `iEnvironmentType`) As [CATIARenderingEnvironment](../CATRscInterfaces/interface_RenderingEnvironment_87036.md)

   Adds a new environment to the environments collection.

**Parameters:**

` iEnvironmentType`      The type of the environment to create choosen among:

1     For cubical environment 2     For spherical environment 3     For cylindrical environment

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIARenderingEnvironment](../CATRscInterfaces/interface_RenderingEnvironment_87036.md)

   Returns an environment index in the environments collection.

**Parameters:**

` iIndex`      The index of the environment to retrieve in the collection of environments. Compared with other collections, you cannot use the name of the environment as argument.

**Returns:**      The retrieved environment  **Example:**      The following example returns in `MyEnvironment` the sixth environment in a environment collection.

```VBScript
     Dim MyEnvironment As RenderingEnvironment
     Set MyEnvironment = RenderingEnvironments.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a environment from the environments collection.  
### Sub **RemoveAll**( )

   Removes all environments.of the collection