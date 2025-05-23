# SchCompGraphic (Object)

**_Manage the graphical representation of a schematic component._**

## Methods

### Sub **Activate**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iGRRName`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iDb2WhereAt`,| | [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md) | `oGRR`)

   To add a new image to an existing object. This new image is an instance of graphical representation with the input name.

**Parameters:**

` iGRRName`      The name of the graphic representation
` iDb2WhereAt`      The x-y coordinates of the image position. If NULL, the image will be positioned at the origin.
` oGRR`      Pointer to the new graphical image of the component.

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim strVar1 As String
     Dim dbVar2(2) As CATSafeArrayVariant
     Dim objArg3 As SchGRRComp
      ...
     objThisIntf.ActivatestrVar1,dbVar2,objArg3

```

### Sub **AddGraphicalRepresentation**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRRToAdd`)

   Add a graphical representation to a component.

**Parameters:**

` iGRRToAdd`      The graphical representation to be added to the component.

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.AddGraphicalRepresentationobjArg1

```

### Sub **Deactivate**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`)

   To remove an image to an existing object.

**Parameters:**

` iGRR`      The graphical image to be removed from the component.
` iDb2WhereAt`      The x-y coordinates of the image position. If NULL, the image will be positioned at the origin.

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.DeactivateobjArg1

```

### Func **ListGraphicalImages**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List all graphical images (instances of the rep) of a component.

**Parameters:**

` oLGRR`      A list of graphical images (members are CATISchGRRComp interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListGraphicalImages

```

### Func **ListGraphicalRepresentations**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List all graphical representation of a component.

**Parameters:**

` oLGRR`      A list of graphical representations (members are CATISchGRRComp interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListGraphicalRepresentations

```

### Sub **RemoveGraphicalRepresentation**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRRToRemove`)

   Remove a graphical representation from a component.

**Parameters:**

` iGRRToRemove`      The graphical representation to be removed from the component.

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.RemoveGraphicalRepresentationobjArg1

```

### Sub **Switch**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGRRName`,  [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `oGRR`)

   Replace the input image object with an image of the graphical representation with the input name.

**Parameters:**

` iGRR`      Pointer to the component graphical image to be switched.
` oGRR`      Pointer to the new graphical image of the component.

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim objArg1 As SchGRRComp
     Dim strVar2 As String
     Dim objArg3 As SchGRRComp
      ...
     objThisIntf.SwitchobjArg1,strVar2,objArg3

```

### Sub **SwitchAll**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGRRName`)

   Replace all occurances of the images of this component with those of the graphical representation with the input name.

**Parameters:**

` iGRRName`      The name of the graphical representation

**Example:**

```VBScript
     Dim objThisIntf As SchCompGraphic
     Dim strVar1 As String
      ...
     objThisIntf.SwitchAllstrVar1

```