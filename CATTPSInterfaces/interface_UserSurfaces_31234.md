# UserSurfaces (Collection)

**__**

## Methods

### Func **Generate**(| [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `iSupport`) As [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)

   Use this method in a Part. Creates a new user surface and adds it to the Surfaces collection.

**Parameters:**

` iSupport`      The first reference that will support the user surface

**Returns:**      The created user surface  **Example:**      The following example creates a user surface names `NewUserSurf` from the reference `Ref` in the Surfaces collection of the `rootPart` part in the `partDoc` part document.

```VBScript
     Set rootPart = partDoc.Part
     Set NewUserSurf = rootPart.UserSurfaces.Add(Ref)

```

### Func **GenerateInAProductCtx**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProdInst`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`) As [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)

   Use this method in a Product. Creates a new user surface and adds it to the Surfaces collection.

**Parameters:**

` iProduct`      The level on which you want to create annotation (part or product).
` iProdInst`      The product instance where there is the geometry.
` iSupport`      The first reference that will support the user surface

**Returns:**      The created user surface  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)

   Find a user surface inside the collection.

**Parameters:**

` iIndex`      The position of the users surface in the collection

**Returns:**      The user surface that is in the iIndex position in the collection  
### Func **MakeUserSurfaceNode**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iFirstUserSurf`,  [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSecondUserSurf`) As [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)

   Usefull to create a User Surface Node from two others User Surface. Creates a new user surface and adds it to the Surfaces collection.

**Parameters:**

` iFirstUserSurf`      The first User Surface to use.
` iSecondUserSurf`      The second User Surface to use.

**Returns:**      The created user surface  
### Func **MakeUserSurfaceNode2**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListOfUserSurfaces`) As [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)

   Usefull to create a User Surface Node from a list of User Surfaces. Creates a new user surface and adds it to the Surfaces collection.

**Parameters:**

` iListOfUserSurfaces`      The list User Surfaces to use.

**Returns:**      The created user surface