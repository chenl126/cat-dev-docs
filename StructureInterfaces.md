# StructureInterfaces Framework

## Object Index

  * [ColorESSObjectSettingAtt](StructureInterfaces/interface_ColorESSObjectSettingAtt_117878.md)
  * [ColorSTDObjectSettingAtt](StructureInterfaces/interface_ColorSTDObjectSettingAtt_117820.md)
  * [MaterialESSObjectSettingAtt](StructureInterfaces/interface_MaterialESSObjectSettingAtt_148682.md)
  * [PathESSRessourcesSettingAtt](StructureInterfaces/interface_PathESSRessourcesSettingAtt_152193.md)
  * [StrAnchorPoint](StructureInterfaces/interface_StrAnchorPoint_42208.md)
  * [StrAnchorPoints](StructureInterfaces/interface_StrAnchorPoints_48821.md)
  * [StrComputeServices](StructureInterfaces/interface_StrComputeServices_70102.md)
  * [StrCutback](StructureInterfaces/interface_StrCutback_21398.md)
  * [StrFoundation](StructureInterfaces/interface_StrFoundation_37108.md)
  * [StrFoundations](StructureInterfaces/interface_StrFoundations_43298.md)
  * [StrMember](StructureInterfaces/interface_StrMember_17505.md)
  * [StrMemberExtremity](StructureInterfaces/interface_StrMemberExtremity_70726.md)
  * [StrMembers](StructureInterfaces/interface_StrMembers_21868.md)
  * [StrObject](StructureInterfaces/interface_StrObject_17492.md)
  * [StrObjectFactory](StructureInterfaces/interface_StrObjectFactory_54850.md)
  * [StrPlate](StructureInterfaces/interface_StrPlate_13958.md)
  * [StrPlates](StructureInterfaces/interface_StrPlates_17878.md)
  * [StrSection](StructureInterfaces/interface_StrSection_22058.md)
  * [StrWorkbench](StructureInterfaces/interface_StrWorkbench_31174.md)
  * [TypeESSObjectSettingAtt](StructureInterfaces/interface_TypeESSObjectSettingAtt_108511.md)

## Enumerated Types Index

  * [CATStrSectionProperties](StructureInterfaces/enum_CATStrSectionProperties_112005.md)
  * [CatStrCreationMode](StructureInterfaces/enum_CatStrCreationMode_67320.md)
  * [CatStrCutbackType](StructureInterfaces/enum_CatStrCutbackType_60664.md)
  * [CatStrLinkMode](StructureInterfaces/enum_CatStrLinkMode_40380.md)
  * [CatStrMaterialOrientation](StructureInterfaces/enum_CatStrMaterialOrientation_132902.md)
  * [CatStrMemberExtremity](StructureInterfaces/enum_CatStrMemberExtremity_94780.md)
  * [CatStrPlacementPoint](StructureInterfaces/enum_CatStrPlacementPoint_84662.md)
  * [CatStrPlaneMode](StructureInterfaces/enum_CatStrPlaneMode_46160.md)

---

# CatStrCreationMode (Enumeration)

**_Not yet implemented._**

---

# CatStrCutbackType (Enumeration)

**_Kinds of_**
[StrCutback](../StructureInterfaces/interface_StrCutback_21398.md) objects. Defines the plane that will cut the members extremities.

**Values:**

` catStrNormalType`      the cut plane is normal to the relimited member axis.
` catStrWeldedType`      the cut plane is defined by the relimiting member intersecting face.
` catStrMiteredType`      the cut plane is the mean plane between the two members.
` catStrNotchingType`      not yet implemented.

---

# CatStrLinkMode (Enumeration)

**_Associative mode._**
Creating a cutback uses, in a member, contextual geometry from other parts. This geometry can be copied with or without a link on the original geometry.

**Values:**

` catStrWithLinkMode`      a links is kept
` catStrNoLinkMode`      no links is kept
` catStrWithRefLinkMode`      a reference links is kept

---

# CatStrMaterialOrientation (Enumeration)

**_Material orientations._**
Each geometric object such as a plane or a surface has an intrinsic orientation. This intrinsic orientation or its reverse can be used when using this object as a reference.

**Values:**

` catStrStandardOrientation`      the same
` cat`      StrReverseOrientation

---

# CatStrMemberExtremity (Enumeration)

**_Extremities of a Member object._**

**Values:**

` catStartExtremity`      the member's start extremity
` catEndExtremity`      the member's end extremity
` catBothExtremity`      the member's both extremities

---

# CatStrPlacementPoint (Enumeration)

**_Anchor points of a_**
[Section](../SpaceAnalysisInterfaces/interface_Section_11089.md) object.

**Values:**

` catStrBottomLeft`      the bottom left anchor point
` catStrBottomCenter`      the bottom center anchor point
` catStrBottomRight`      the bottom right anchor point
` catStrCenterLeft`      the center left anchor point
` catStrCenterCenter`      the center center anchor point
` catStrCenterRight`      the center right anchor point
` catStrTopLeft`      the top left anchor point
` catStrTopCenter`      the top center anchor point
` catStrTopRight`      the top right anchor point
` catStrGravity`      the gravity center anchor point
` catStrGravityBottom`      the anchor point is the vertical projection of the gravity center on the bottom edge of the sections's profile.
` catStrGravityLeft`      the anchor point is the horizontal projection of the gravity center on the left edge of the sections's profile.
` catStrGravityRight`      the anchor point is the horizontal projection of the gravity center on the right edge of the sections's profile.
` catStrGravityTop`      the anchor point is the vertical projection of the gravity center on the top edge of the sections's profile.
` catStrUserPoint`      the user defined anchor point

---

# CatStrPlaneMode (Enumeration)

**_Usage modes of a plane used as a support for a member support axis._**

**Values:**

` catStrNonePlane`      The support is not a plane.
` catStrOnPlane`      The member support axis is in the support plane.
` catStrParallelToPlane`      The member support axis is in a plane parallel to the support plane.

---

# CATStrSectionProperties (Enumeration)

**_Property type._**

**Values:**

` catStrNonePlane`      The support is not a plane.
` catStrOnPlane`      The member support axis is in the support plane.
` catStrParallelToPlane`      The member support axis is in a plane parallel to the support plane.

---

# ColorESSObjectSettingAtt (Object)

**_The interface to access a CATIAColorESSObjectSettingAtt._**

## Methods

### Sub **GetMemberColor**( long  `oMemberColorR`,  long  `oMemberColorG`,  long  `oMemberColorB`)

   Returns or sets the MemberColor parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetMemberColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MemberColor parameter.

**Role** :Retrieves the state of the MemberColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetPlateColor**( long  `oPlateColorR`,  long  `oPlateColorG`,  long  `oPlateColorB`)

   Returns or sets the PlateColor parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetPlateColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlateColor parameter.

**Role** :Retrieves the state of the PlateColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMemberColor**( long  `iMemberColorR`,  long  `iMemberColorG`,  long  `iMemberColorB`)

### Sub **SetMemberColorLock**( boolean  `iLocked`)

   Locks or unlocks the MemberColor parameter.

**Role** :Locks or unlocks the MemberColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlateColor**( long  `iPlateColorR`,  long  `iPlateColorG`,  long  `iPlateColorB`)

### Sub **SetPlateColorLock**( boolean  `iLocked`)

   Locks or unlocks the PlateColor parameter.

**Role** :Locks or unlocks the PlateColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# ColorSTDObjectSettingAtt (Object)

**_The interface to access a CATIAColorSTDObjectSettingAtt._**

## Methods

### Sub **GetPlateColor**( long  `oPlateColorR`,  long  `oPlateColorG`,  long  `oPlateColorB`)

   Returns or sets the PlateColor parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetPlateColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlateColor parameter.

**Role** :Retrieves the state of the PlateColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetShapeColor**( long  `oShapeColorR`,  long  `oShapeColorG`,  long  `oShapeColorB`)

   Returns or sets the ShapeColor parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetShapeColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ShapeColor parameter.

**Role** :Retrieves the state of the ShapeColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetPlateColor**( long  `iPlateColorR`,  long  `iPlateColorG`,  long  `iPlateColorB`)

### Sub **SetPlateColorLock**( boolean  `iLocked`)

   Locks or unlocks the PlateColor parameter.

**Role** :Locks or unlocks the PlateColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetShapeColor**( long  `iShapeColorR`,  long  `iShapeColorG`,  long  `iShapeColorB`)

### Sub **SetShapeColorLock**( boolean  `iLocked`)

   Locks or unlocks the ShapeColor parameter.

**Role** :Locks or unlocks the ShapeColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# MaterialESSObjectSettingAtt (Object)

**_The interface to access a CATIAMaterialESSObjectSettingAtt._**

## Properties

### Property **MemberMaterial**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the MemberMaterial parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlateMaterial**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the PlateMaterial parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetMemberMaterialInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MemberMaterial parameter.

**Role** :Retrieves the state of the MemberMaterial parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlateMaterialInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlateMaterial parameter.

**Role** :Retrieves the state of the PlateMaterial parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMemberMaterialLock**( boolean  `iLocked`)

   Locks or unlocks the MemberMaterial parameter.

**Role** :Locks or unlocks the MemberMaterial parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlateMaterialLock**( boolean  `iLocked`)

   Locks or unlocks the PlateMaterial parameter.

**Role** :Locks or unlocks the PlateMaterial parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# PathESSRessourcesSettingAtt (Object)

**_The interface to access a CATIAPathESSRessourcesSettingAtt._**

## Properties

### Property **ResolvedSectionsPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ResolvedSectionsPath parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SectionsCatalogPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the SectionsCatalogPath parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ThicknessListPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ThicknessListPath parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetResolvedSectionsPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ResolvedSectionsPath parameter.

**Role** :Retrieves the state of the ResolvedSectionsPath parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSectionsCatalogPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SectionsCatalogPath parameter.

**Role** :Retrieves the state of the SectionsCatalogPath parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetThicknessListPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ThicknessListPath parameter.

**Role** :Retrieves the state of the ThicknessListPath parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetResolvedSectionsPathLock**( boolean  `iLocked`)

   Locks or unlocks the ResolvedSectionsPath parameter.

**Role** :Locks or unlocks the ResolvedSectionsPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSectionsCatalogPathLock**( boolean  `iLocked`)

   Locks or unlocks the SectionsCatalogPath parameter.

**Role** :Locks or unlocks the SectionsCatalogPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetThicknessListPathLock**( boolean  `iLocked`)

   Locks or unlocks the ThicknessListPath parameter.

**Role** :Locks or unlocks the ThicknessListPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# StrAnchorPoint (Object)

**_Represents an anchor point._**
An anchor point is a point used to place the section on the support in the design model.

## Methods

### Sub **GetCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoord`)

   Retrieves the coordinates of the anchor point. These coordinates are expressed in the section local coordinate system.

**Parameters:**

` oCoord`      The 2D coordinates of the anchor point.

**Example:**

```VBScript
     Dim coord(1)
     anchor_1.GetCoordinates(coord)

```

---

# StrAnchorPoints (Collection)

**_A collection of the anchor points of a section object._**

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAStrAnchorPoint](../StructureInterfaces/interface_StrAnchorPoint_42208.md)

   Returns an anchor point from its index in the anchor points collection.

**Parameters:**

` iIndex`      The index of the anchor point to retrieve in the collection of anchor points. This index can either be the rank of the anchor point in the collection or the name you assign to the anchor point. As a numerics, this index is the rank of the anchor point in the collection. The index of the first anchor point in the collection is 1, and the index of the last anchor point is Count. As a string, it is the name you assigned to the member using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved anchor point

---

# StrComputeServices (Object)

**_Represents a structure service object._**
Structure service object extracts properties on structure objects.

## Methods

### Sub **GetCenterOfGravity**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  double  `oX`,  double  `oY`,  double  `oZ`)

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

---

# StrCutback (Object)

**_Represents the cutback object._**
It is aggregated to an extremity of a member. It can be retrieved using the [StrMemberExtremity](../StructureInterfaces/interface_StrMemberExtremity_70726.md) object.

## Properties

### Property **Offset**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the parameter defining the offset.  
### Property **Type**( ) As [CatStrCutbackType](../StructureInterfaces/enum_CatStrCutbackType_60664.md) (Read Only)

   Returns the type of the cutback object.

**Example:**      This example retrieves the type for the `StrMember` object.

```VBScript
     Type = Member.Type

```

---

# StrFoundation (Object)

**_Represents a structure foundation assembly._**

---

# StrFoundations (Collection)

**_A collection of the Foundation objects contained in a given Product object of a ProductDocument object._**
A Product object aggregates zero or one Foundations collection. This collection is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the Foundation collection from the `oProduct` Product.

```VBScript
     Dim oFoundations as AnyObject
     Set oFoundations = oProduct.GetTechnologicalObject("StructureFoundations")

```

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAStrFoundation](../StructureInterfaces/interface_StrFoundation_37108.md)

   Returns a Foundation from its index in the Foundations collection.

**Parameters:**

` iIndex`      The index of the Foundation to retrieve in the collection of Foundations. This index can either be the rank of the Foundation in the collection or the name you assign to the Foundation. As a numerics, this index is the rank of the Foundation in the collection. The index of the first Foundation in the collection is 1, and the index of the last Foundation is Count. As a string, it is the name you assigned to the Foundation using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved Foundation  **Example:**      The following example returns in `ThisFoundation` the third Foundation, and in `ThatFoundation` the Foundation named `Column_1` in the `Assembly_1` Foundation collection.

```VBScript
     Dim ThisFoundation As Foundation
     Set ThisFoundation = Assembly_1.Item(3)
     Dim ThatFoundation As Foundation
     Set ThatFoundation = Assembly.Item("Column_1")

```

---

# StrMember (Object)

**_Represents a member object._**
The member object aggregates a section coming from a catalog, a support and two extremities. The member object inherits all methods from the structure object and the product object.

## Properties

### Property **Angle**( ) As double

   Returns or set the orientation of the section on the support object.

**Example:**

```VBScript
     angle = Member_1.Angle

```

### Property **AngleParameter**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the parameter used to define the orientation of the section on the support object.

**Example:**

```VBScript
     Dim angle As Parameter
     Set angle = Member_1.AngleParameter

```

### Property **CurrentAnchorPointName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the current anchor point used to locate the section on the support object.

**Example:**

```VBScript
     name = Member_1.CurrentAnchorPointName

```

### Property **EndExtremity**( ) As [CATIAStrMemberExtremity](../StructureInterfaces/interface_StrMemberExtremity_70726.md) (Read Only)

   Returns the member's end extremity object.

**Example:**

```VBScript
     Dim extremity As StrMemberExtremity
     Set extremity = Member_1.EndExtremity

```

### Property **InputSupport**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md) (Read Only)

   Retrieves the input support. The input support is the given support at the creation of the member.  
### Property **Section**( ) As [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md) (Read Only)

   Returns or sets the section object.

**Example:**

```VBScript
     Dim section As StrSection
     Set section = Member_1.Section

```

### Property **StartExtremity**( ) As [CATIAStrMemberExtremity](../StructureInterfaces/interface_StrMemberExtremity_70726.md) (Read Only)

   Returns the member's start extremity object.

**Example:**

```VBScript
     Dim extremity As StrMemberExtremity
     Set extremity = Member_1.StartExtremity

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md) (Read Only)

   Retrieves the result support object. For example, if your member object is created using two points, the result support object will be the line joining these two points.  
### Property **SurfaceReference**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Retrieves or sets the surface reference object for the member. The section will be oriented using this surface reference object if one is set. Nevertheless, the surface reference object can be null.

**Example:**      This example sets the reference object to null.

```VBScript
     myMember.SurfaceReference = Nothing

```

Methods

### Func **CreateCutback**( [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)  `iMember`,  [CatStrCutbackType](../StructureInterfaces/enum_CatStrCutbackType_60664.md)  `iCutback`,  double  `iOffset`) As [CATIAStrCutback](../StructureInterfaces/interface_StrCutback_21398.md)

   Creates a cutback object between two member objects.

**Parameters:**

` iMember`      The relimiting member
` iCutback`      The type of the cutback.
` iOffset`      The offset used in the cutback.

**Example:**      The following example create a cutback

```VBScript
     Dim cutback As StrCutback
     Set cutback = Member_1.CreateCutback(Member_2, catStrWeldedType, 0.05)

```

### Sub **Flip**( )

   Flips the section. Useful for asymetric section as the angle section, or the channel section.

**Example:**

```VBScript
     Member_1.Rotate(1,25)

```

### Sub **Rotate**( double  `iAngle`)

   Rotates the section on its support object. The given angle is applied using the current orientation of the section.

**Example:**

```VBScript
     Dim extremity As StrMemberExtremity
     Set extremity = Member_1.StartExtremity

```

---

# StrMemberExtremity (Object)

**_Represents an extremity of a member object._**
One is called the start extremity and the other the end extremity.

## Properties

### Property **AngleCut**( ) As double (Read Only)

   Returns the angle cut for a member extremity.  
### Property **Cutback**( ) As [CATIAStrCutback](../StructureInterfaces/interface_StrCutback_21398.md) (Read Only)

   Returns the cutback object.  
### Property **Input**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the input object defining the extremity. The input object may not belong to the support object.  
### Property **Offset**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the offset parameter defined on this extremity. This parameter can be null.  
### Property **Point**( ) As [CATIAHybridShapePoint](../GSMInterfaces/interface_Point_5884.md) (Read Only)

   Returns the point defining the extremity. This point belongs to the support object.  Methods

### Sub **AddOffset**( double  `iOffset`)

   Adds an offset on the extremity. This method has to be used when the extremity has no offset already defined, else you will get an error.  
### Sub **GetCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the extremity.

**Parameters:**

` oCoordinates`      The coordinates of the the extremity

### Sub **ResetCutback**( )

   Resets the defined cutback object.  
### Sub **SetExtremityFromCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Modifies the coordinates of the extremity defined by a point.

**Parameters:**

` iCoordinates`      The coordinates to modify the extremity

---

# StrMembers (Collection)

**_A collection of the Member objects contained in a given Product object of a ProductDocument object._**
A Product object aggregates zero or one Members collection. This collection is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the member collection from the `oProduct` Product.

```VBScript
     Dim oMembers as AnyObject
     Set oMembers = oProduct.GetTechnologicalObject("StructureMembers")

```

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Returns a member from its index in the Members collection.

**Parameters:**

` iIndex`      The index of the member to retrieve in the collection of members. This index can either be the rank of the member in the collection or the name you assign to the member. As a numerics, this index is the rank of the member in the collection. The index of the first member in the collection is 1, and the index of the last member is Count. As a string, it is the name you assigned to the member using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved member  **Example:**      The following example returns in `ThisMember` the third member, and in `ThatMember` the member named `Column_1` in the `Assembly_1` member collection.

```VBScript
     Dim ThisMember As Member
     Set ThisMember = Assembly_1.Item(3)
     Dim ThatMember As Member
     Set ThatMember = Assembly.Item("Column_1")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a member from the Members collection.

**Parameters:**

` iIndex`      The index of the member to remove. This index can either be the rank of the member in the collection or the name you assigned to the member. As a numerics, this index is the rank of the member in the collection. The index of the first member in the collection is 1, and the index of the last member is Count. As a string, it is the name you assigned to the member using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Example:**      The following example removes the sixth member and the member named `Column_1` from the `Assembly_1` member collection.

```VBScript
     Assembly_1.Remove(6)
     Assembly_1.Remove("Column_1")

```

---

# StrObject (Object)

**_Represents a structure object._**

## Properties

### Property **Type**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the type of the structure object.

**Example:**      This example retrieves the type of the `StructureMember` object.

```VBScript
     Dim oType As Parameter
     Set oType = StructureMember.Type

```

---

# StrObjectFactory (Object)

**_Represents the factory object for all the structure objects._**
The factory is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the structure factory object from the `oProduct` Product.

```VBScript
     Dim oFactory as AnyObject
     Set oFactory = oProduct.GetTechnologicalObject("StructureObjectFactory")

```

## Methods

### Func **AddDefExtFromCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoord`,  double  `iOffset`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Creates a member extremity definition object from coordinates and an offset value.

**Parameters:**

` iCoord`      The coordinates of the extremity
` iOffset`      The offset on this extremity

### Func **AddDefExtFromReference**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`,  double  `iOffset`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Creates a member extremity definition object from an existing object in the model and an offset value.

**Parameters:**

` iReference`      The reference object defining the extremity
` iOffset`      The offset on this extremity

### Func **AddDefExtOnMember**( [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)  `iMember`,  [CatStrMemberExtremity](../StructureInterfaces/enum_CatStrMemberExtremity_94780.md)  `iSide`,  double  `iDistance`,  double  `iOffset`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Creates a member extremity definition object from another member object, its side, a distance on it and an offset.

**Parameters:**

` iMember`      The member used to define the extremity
` iSide`      The side of the previous member used to define the distance along the member
` iDistance`      The distance along the selected member
` iOffset`      The offset on the extremity

### Func **AddDimMember**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iMathDirection`,  double  `iLength`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a dimension member object from a point and a mathematical definition of a direction.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iMathDirection`      The mathematical definition of the direction
` iLength`      The length of the member
` iType`      The type of the member. This type is user defined.

### Func **AddDimMemberOnPlane**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDirection`,  [CatStrPlaneMode](../StructureInterfaces/enum_CatStrPlaneMode_46160.md)  `iMode`,  double  `iLength`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a dimension member object on a plane following a mathematical definition of a plane.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iDefExtr2`      The extremity object defining the end limit of the member
` iDirection`      The direction object. It can be a line or a plane
` iMode`      The way the member is created with respect to the direction plane. Useless if if the direction is not a plane.
` iOrientation`      The orientation of the member
` iLength`      The length of the member
` iType`      The type of the member. This type is user defined.

### Func **AddDimMemberPtPt**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  double  `iLength`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a dimension member object from two given points.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iDefExtr2`      The extremity object defining the end limit of the member
` iLength`      The length of the member
` iType`      The type of the member. This type is user defined.

### Func **AddDimMemberWithSupport**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDirection`,  [CatStrPlaneMode](../StructureInterfaces/enum_CatStrPlaneMode_46160.md)  `iMode`,  [CatStrMaterialOrientation](../StructureInterfaces/enum_CatStrMaterialOrientation_132902.md)  `iOrientation`,  double  `iLength`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a dimension member object using a support object.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iDefExtr2`      The extremity object defining the end limit of the member. In case of line for a support, this parameter is not taking into account.
` iDirection`      The direction object. It can be a line or a plane
` iMode`      The way the member is created with respect to the direction plane. Useless if if the direction is not a plane.
` iOrientation`      The orientation of the member
` iLength`      The length of the member
` iType`      The type of the member

### Func **AddMember**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a member object.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iDefExtr2`      The extremity object defining the end limit of the member
` iType`      The type of the member. This type is user defined.

### Func **AddMemberFromDir**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDirection`,  [CatStrPlaneMode](../StructureInterfaces/enum_CatStrPlaneMode_46160.md)  `iMode`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a member object using a direction object as a line or a plane.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iDefExtr2`      The extremity object defining the end limit of the member
` iDirection`      The direction object used to orientate the support. The direction object can be a plane or a line.
` iMode`      The way the member is created with respect to the direction plane. Useless if if the direction is not a plane.
` iType`      The type of the member. This type is user defined.

### Func **AddMemberFromMathDir**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDirection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a member object using a mathematical definition of the direction.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iDefExtr2`      The extremity object defining the end limit of the member
` iDirection`      The mathematical definition of the direction
` iType`      The type of the member. This type is user defined.

### Func **AddMemberFromMathPlane**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPlane`,  [CatStrPlaneMode](../StructureInterfaces/enum_CatStrPlaneMode_46160.md)  `iPlaneMode`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a member object from a mathematical definition of a plane.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iDefExtr1`      The extremity object defining the start limit of the member
` iDefExtr2`      The extremity object defining the end limit of the member
` iDirection`      The mathematical definition of a plane
` iPlaneMode`      The way the member is created with respect to the direction plane. Useless if if the direction is not a plane.
` iType`      The type of the member. This type is user defined.

### Func **AddMemberOnSupport**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  double  `iAngle`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a member object on a given support.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iAngle`      The orientation of the section on its support
` iSupport`      The support for the member. The support can be a line or a curve
` iDefExtr1`      The extremity object defining the start limit of the member. It can be NULL.
` iDefExtr2`      The extremity object defining the end limit of the member. It can be NULL.
` iType`      The type of the member. This type is user defined.

### Func **AddMemberOnSupportWithRef**( [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)  `iSection`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAnchorName`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurfRef`,  double  `iAngle`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr1`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iDefExtr2`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

   Creates a member object on a given support object and a surface used to define the orientation of the section. The surface reference defines the relative orientation on which you add an angle.

**Parameters:**

` iSection`      The section object defining the profile for the member
` iAnchorName`      The name of the anchor point
` iReference`      The reference to define the zero orientation of the section. The section follows this guide line along the support of the member.
` iAngle`      The orientation of the section on its support
` iSupport`      The support for the member. The support can be a line or a curve
` iDefExtr1`      The extremity object defining the start limit of the member. It can be NULL.
` iDefExtr2`      The extremity object defining the end limit of the member. It can be NULL.
` iType`      The type of the member. This type is user defined.

### Func **AddPlate**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iThickness`,  [CatStrMaterialOrientation](../StructureInterfaces/enum_CatStrMaterialOrientation_132902.md)  `iOrientation`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iContour`,  double  `iOffset`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrPlate](../StructureInterfaces/interface_StrPlate_13958.md)

   Creates a plate from a contour defined by coordinates.

**Parameters:**

` iSupport`      The plane defining the support of the plate
` iThickness`      The standard thickness of the plate. The thickness follows the standard orientation of the support
` iOrientation`      The material orientation of the plate
` iContour`      The array containing all objects defining the contour of the plate
` iOffset`      The offset applies to the support of the plate
` iType`      The type of the plate. This information is user defined. It is added as an attribute on the plate.

### Func **AddRectangularEndPlate**( [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)  `iMember`,  [CatStrMemberExtremity](../StructureInterfaces/enum_CatStrMemberExtremity_94780.md)  `iSide`,  double  `iThickness`,  double  `iHeight`,  double  `iWidth`,  [CatStrMaterialOrientation](../StructureInterfaces/enum_CatStrMaterialOrientation_132902.md)  `iOrientation`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAStrPlate](../StructureInterfaces/interface_StrPlate_13958.md)

   Creates a rectangular end plate on an extremity of a given member.

**Parameters:**

` iMember`      The member on which the end-plate will be created
` iSide`      The side of the selected member
` iThickness`      The standard thickness of the plate. The thickness follows the standard orientation of the support
` iHeight`      The height of the plate
` iWidth`      The width of the plate
` iOrientation`      The material orientation of the plate
` iType`      The type of the plate. This information is user defined. It is added as an attribute on the plate.

### Func **AddSection**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iPart`) As [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)

   Creates a section object from part document. This part must aggregate a sketch object defining the contour of the section. The contour of the section have to be closed and may contain several domains.

**Parameters:**

` iPart`      The part document where the sketch of the section is defined

### Func **AddSectionFromCatalog**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iPart`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCatalogName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFamilyName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSectionName`) As [CATIAStrSection](../StructureInterfaces/interface_StrSection_22058.md)

   Creates a section object from part document. This part must aggregate a sketch object defining the contour of the section. This service gives you to define where the resolved part comes from to allow a replace mechanism. The contour of the section have to be closed and may contain several domains.

**Parameters:**

` iCatalogName`      The catalog name where the document comes from
` iFamilyName`      The family name where the document comes from
` iSectionName`      The section name where the document comes from
` iPart`      The part document where the sketch of the section is defined

### Func **ExtendProductAsFoundation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iClass`) As [CATIAStrFoundation](../StructureInterfaces/interface_StrFoundation_37108.md)

   Extend an assembly as a structure foundation assembly.

**Parameters:**

` iClass`      the name of the user class

---

# StrPlate (Object)

**_Represents a structure plate object._**
A plate is defined by a thickness and aggregates a support object and a sketch defining its contour.

## Properties

### Property **Offset**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the offset between the given support and the support of the plate.  
### Property **Sketch**( ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

   Returns the sketch object of the plate.  
### Property **StandardThickness**( ) As double

   Returns the standard thickness following the support orientation.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support of the plate.  Methods

### Sub **ReverseDirection**( )

   Reverses the material orientation of the plate.

```VBScript
     Plate_1.ReverseDirection

```

---

# StrPlates (Collection)

**_A collection of the Plate objects contained in a given Product object of a ProductDocument object._**
A Product object can aggregate one or zero Plates collection. This collection is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the plate collection from the `oProduct` Product.

```VBScript
     Dim oPlates as AnyObject
     Set oPlates = oProduct.GetTechnologicalObject("StructurePlates")

```

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAStrPlate](../StructureInterfaces/interface_StrPlate_13958.md)

   Returns a plate from its index in the Plates collection.

**Parameters:**

` iIndex`      The index of the plate to retrieve in the collection of plates. This index can either be the rank of the plate in the collection or the name you assign to the plate. As a numerics, this index is the rank of the plate in the collection. The index of the first plate in the collection is 1, and the index of the last plate is Count. As a string, it is the name you assigned to the plate using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved plate

**Example:**      The following example returns in `ThisPlate` the third plate, and in `ThatPlate` the plate named `EndPlate_1` in the `Assembly_1` plate collection.

```VBScript
     Dim ThisPlate As Plate
     Set ThisPlate = Assembly_1.Item(3)
     Dim ThatPlate As Plate
     Set ThatPlate = Assembly.Item("EndPlate_1")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a plate from the Plates collection.

**Parameters:**

` iIndex`      The index of the plate to remove. This index can either be the rank of the plate in the collection or the name you assigned to the plate. As a numerics, this index is the rank of the plate in the collection. The index of the first plate in the collection is 1, and the index of the last plate is Count. As a string, it is the name you assigned to the plate using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property

**Example:**      The following example removes the sixth plate and the plate named `EndPlate_1` from the `Assembly_1` plate collection.

```VBScript
     Assembly_1.Remove(6)
     Assembly_1.Remove("EndPlate_1")

```

---

# StrSection (Object)

**_Represents the section object._**
The section object is created from a part document in which a sketch has to be defined.
The sketch object may contain one or several contour but all of them have to be closed.
Predefined anchor points objects are calculated from the geometrical contour as the top bottom point, the center gravity point, etc.
User anchor points can be created in the sketch using the parametric geometry or not. However the names of these points have to prefixed by the string "Str" to be recognized as structure anchor points.
Some attributes are defined on the section object but cannot be modified.
A group of attributes defines the section name, the family name, and the the name of the catalog where the section comes from.
Another attribute called the profile type defines the type of the parametric contour used to create the section. The contour can be a Tee, an angle, a channel, a square tube, and so on. These predefined contours are useful to create a new catalog with some standard contours.

## Properties

### Property **CatalogName**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the parameter defining the catalog name.

**Example:**

```VBScript
     Dim name As Parameter
     Set name = Section_1.CatalogName

```

### Property **FamilyName**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the parameter defining the family name.

**Example:**

```VBScript
     Dim name As Parameter
     Set name = Section_1.FamilyName

```

### Property **ProfileType**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the parameter defining the profile type of the section.

**Example:**

```VBScript
     Dim type As Parameter
     Set type = Section_1.ProfileType

```

### Property **SectionName**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

   Returns the parameter defining the section name.

**Example:**

```VBScript
     Dim name As Parameter
     Set name = Section_1.SectionName

```

### Property **StrAnchorPoints**( ) As [CATIAStrAnchorPoints](../StructureInterfaces/interface_StrAnchorPoints_48821.md) (Read Only)

   Returns the collection of anchor points.

```VBScript

       **Example:**
            Dim anchorPts As StrAnchorPoints
     Set anchorPts = Section_1.StrAnchorPoints

```

Methods

### Sub **GetProperty**( [CATStrSectionProperties](../StructureInterfaces/enum_CATStrSectionProperties_112005.md)  `iProperty`,  double  `oValue`)

   Get a property value.

**Example:**

```VBScript
     Dim type As Parameter
     Set type = Section_1.GetProperty(CatStrArea)

```

---

# StrWorkbench (Object)

**_Represents the structure workbench object._**

## Properties

### Property **StrComputeServices**( ) As [CATIAStrComputeServices](../StructureInterfaces/interface_StrComputeServices_70102.md) (Read Only)

   Returns the compute services object. It allows you to calculate some properties on the structure objects.

**Example:**

```VBScript
     Dim services As StrComputeServices
     Set services = workbench_1.StrComputeServices

```

---

# TypeESSObjectSettingAtt (Object)

**_The interface to access a CATIATypeESSObjectSettingAtt._**

## Properties

### Property **MemberTypes**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the MemberTypes parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlateTypes**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the PlateTypes parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetMemberTypesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MemberTypes parameter.

**Role** :Retrieves the state of the MemberTypes parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlateTypesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlateTypes parameter.

**Role** :Retrieves the state of the PlateTypes parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMemberTypesLock**( boolean  `iLocked`)

   Locks or unlocks the MemberTypes parameter.

**Role** :Locks or unlocks the MemberTypes parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlateTypesLock**( boolean  `iLocked`)

   Locks or unlocks the PlateTypes parameter.

**Role** :Locks or unlocks the PlateTypes parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.