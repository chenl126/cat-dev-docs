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