# Section (Object)

**_Represents the Section object._**
The Section object is a specification of a sectioning display and computationwith a section plane, section slice or section box.

## Properties

### Property **AnnotatedViews**( ) As [CATIAAnnotatedViews](../NavigatorInterfaces/interface_AnnotatedViews_42578.md) (Read Only)

Returns the AnnotatedViews collection of the section.

**Example:**      This example retrieves the AnnotatedViews collection of `NewSection` Section.

```VBScript
   Dim TheAnnotatedViewsList As AnnotatedViews
   Set TheAnnotatedViewsList = NewSection.AnnotatedViews

```

### Property **Behavior**( ) As [CatSectionBehavior](../SpaceAnalysisInterfaces/enum_CatSectionBehavior_68434.md)

Returns or sets the general behavior of the section: Freeze, Automatic update, manual update The behavior value are defined in [CatSectionBehavior](../SpaceAnalysisInterfaces/enum_CatSectionBehavior_68434.md).

**Example:**      The first example retrieves the behavior of `NewSection` Section.

```VBScript
   Dim SectionBehavior As CatSectionBehavior
   Behavior = NewSection.Behavior

```

The second example sets the behavior of `NewSection` Section.

```VBScript
   NewSection.Behavior = catSectionBehaviorAutomatic

```

### Property **CutMode**( ) As long

Returns or sets the cutting mode of the section. The cutting mode value is 1 for clipping or 0 without clipping.

**Example:**      The first example retrieves the cutting mode of `NewSection` Section.

```VBScript
   Dim SectionMode As Integer
   SectionMode = NewSection.CutMode

```

The second example sets the cutting mode of `NewSection` Section.

```VBScript
   NewSection.CutMode = 1

```

### Property **Group**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

Returns or sets the sectionned group. By default, it is the all leaves group.

**Example:**      The first example retrieves the group of `NewSection` Section.

```VBScript
   Dim AGroup As Group
   AGroup = NewSection.Group

```

The second example sets the group of `NewSection` Section.

```VBScript
   Dim AGroup As Group
   NewSection.Group = AGroup

```

### Property **Height**( ) As double

Returns or sets the height of the section. The height value must be greater than 0.

**Example:**      The first example retrieves the height of `NewSection` Section.

```VBScript
   Dim SectionHeight As double
   SectionHeight = NewSection.Height

```

The second example sets the height value of `NewSection` Section.

```VBScript
   NewSection.Height = 100.

```

### Property **Marker3Ds**( ) As [CATIAMarker3Ds](../NavigatorInterfaces/interface_Marker3Ds_15928.md) (Read Only)

Returns the Marker3Ds collection of the section.

**Example:**      This example retrieves the Marker3Ds collection of `NewSection` Section.

```VBScript
   Dim TheMarker3DsList As Marker3Ds
   Set TheMarker3DsList = NewSection.Marker3Ds

```

### Property **Thickness**( ) As double

Returns or sets the thickness of the section. The thickness value must be greater than 0.

**Example:**      The first example retrieves the thickness of `NewSection` Section.

```VBScript
   Dim SectionThickness As double
   SectionThickness = NewSection.Thickness

```

The second example sets the thickness value of `NewSection` Section.

```VBScript
   NewSection.Thickness = 100.

```

### Property **Type**( ) As [CatSectionType](../SpaceAnalysisInterfaces/enum_CatSectionType_41996.md)

Returns or sets the type of the section. The type value are defined in [CatSectionType](../SpaceAnalysisInterfaces/enum_CatSectionType_41996.md).

**Example:**      The first example retrieves the type of `NewSection` Section.

```VBScript
   Dim SectionType As CatSectionType
   SectionType = NewSection.Type

```

The second example sets the type of `NewSection` Section.

```VBScript
   NewSection.Type = catSectionTypeSlice

```

### Property **Width**( ) As double

Returns or sets the width of the section. The width value must be greater than 0.

**Example:**      The first example retrieves the width of `NewSection` Section.

```VBScript
   Dim SectionWidth As double
   SectionWidth = NewSection.Width

```

The second example sets the width value of `NewSection` Section.

```VBScript
   NewSection.Width = 100.

```

Methods

### Func **Export**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Exports the sections curves of the section in a document.

**Returns:**      The document  **Example:**      This example exports the section curves of `NewSection` Section in `PartDoc` document.

```VBScript
   Dim PartDoc As Document
   PartDoc = NewSection.Export

```

### Sub **GetPosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oComponents`)

Retrieves the position of the section. The position of the section is made of a coordinate system whose origin is the center of the section, and X and Y axes lie on the section. It is retrieved in an array of the X, Y, Z axes components and the origin components with respect to the absolute coordinate system.

**Parameters:**

` oComponents`      The position of the section

  * oComponents( 0) is the X component of the X-axis
  * oComponents( 1) is the Y component of the X-axis
  * oComponents( 2) is the Z component of the X-axis
  * oComponents( 3) is the X component of the Y-axis
  * oComponents( 4) is the Y component of the Y-axis
  * oComponents( 5) is the Z component of the Y-axis
  * oComponents( 6) is the X component of the Z-axis
  * oComponents( 7) is the Y component of the Z-axis
  * oComponents( 8) is the Z component of the Z-axis
  * oComponents( 9) is the X component of the origin
  * oComponents(10) is the Y component of the origin
  * oComponents(11) is the Z component of the origin

**Example:**      This example retrieves the position of `NewSection` Section.

```VBScript
   Dim Components (11)
   NewSection.GetPosition Components

```

### Func **IsEmpty**( ) As long

Indicates whether the section is empty. The indicator value is 0 if the section is empty or 1 if the section comprise at least one segment.

**Example:**      This example retrieves the information on `NewSection` Section.

```VBScript
   Dim Indicator
   Indicator = NewSection.IsEmpty

```

### Sub **SetPosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iComponents`)

Sets the position of the section.

**Parameters:**

` oComponents`      The position of the section with respect to the absolute coordinate system

  * iComponents( 0) is the X component of the X-axis
  * iComponents( 1) is the Y component of the X-axis
  * iComponents( 2) is the Z component of the X-axis
  * iComponents( 3) is the X component of the Y-axis
  * iComponents( 4) is the Y component of the Y-axis
  * iComponents( 5) is the Z component of the Y-axis
  * iComponents( 6) is the X component of the Z-axis
  * iComponents( 7) is the Y component of the Z-axis
  * iComponents( 8) is the Z component of the Z-axis
  * iComponents( 9) is the X component of the origin
  * iComponents(10) is the Y component of the origin
  * iComponents(11) is the Z component of the origin

**Example:**      This example sets the position of `NewSection` Section.

```VBScript
   Dim MatrixPos (11) As Double
   MatrixPos( 0) = 1.0
   MatrixPos( 1) = 0.0
   MatrixPos( 2) = 0.0
   MatrixPos( 3) = 0.0
   MatrixPos( 4) = 1.0
   MatrixPos( 5) = 0.0
   MatrixPos( 6) = 0.0
   MatrixPos( 7) = 0.0
   MatrixPos( 8) = 1.0
   MatrixPos( 9) = 1000.0
   MatrixPos(10) = 0.0
   MatrixPos(11) = 0.0
   NewSection.SetPosition MatrixPos

```