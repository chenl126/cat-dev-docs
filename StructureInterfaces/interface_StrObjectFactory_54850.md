# StrObjectFactory (Object)

**_Represents the factory object for all the structure objects._**
The factory is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the structure factory object from the `oProduct` Product.

```VBScript
     Dim oFactory as AnyObject
     Set oFactory = oProduct.GetTechnologicalObject("StructureObjectFactory")

```

## Methods

### Func **AddDefExtFromCoordinates**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iCoord`,| | double | `iOffset`) As [CATIABase](../System/interface_AnyObject_17321.md)

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