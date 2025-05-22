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