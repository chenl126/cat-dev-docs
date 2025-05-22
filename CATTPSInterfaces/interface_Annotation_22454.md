# Annotation (Object)

**_Interface for the Technological Product Specification (TPS) objects._**
Leaf entity in the Design Pattern Composite. TPS modeler enables definition of specification related to surfaces.

## Properties

### Property **SuperType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Get the Super Type.

**Parameters:**

` oSuperType`      The Super Type. The list of SuperType available: "FTA_NonSemantic" "FTA_Form" "FTA_Dimension" "FTA_Position" "FTA_Datum" "FTA_Orientation" "FTA_RunOut"

### Property **TPSStatus**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Get the TPS Status.

**Parameters:**

` oStatus`      The Status.

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Get the Type.

**Parameters:**

` oType`      The Type. List of types available ordered by SuperType: SuperType = "FTA_NonSemantic" Type = "FTA_Text" Type = "FTA_FlagNote" Type = "FTA_Roughness" Type = "FTA_Weld" Type = "FTA_Noa" Type = "FTA_NonSemanticDatum" Type = "FTA_NonSemanticTarget" Type = "FTA_NonSemanticGDT" Type = "FTA_NonSemanticDimension" SuperType = "FTA_Form" Type = "FTA_Flatness" Type = "FTA_Straightness" Type = "FTA_Circularity" Type = "FTA_Cylindricity" Type = "FTA_ProfileOfAnyLine" Type = "FTA_ProfileOfASurface" Type = "FTA_PatternTruePos" SuperType = "FTA_Dimension" Type = "FTA_LinearDimension" Type = "FTA_AngularDimension" Type = "FTA_SecondLinearDimension" Type = "FTA_ChamferDimension" Type = "FTA_BasicDimension" SuperType = "FTA_Position" Type = "FTA_TruePosition" Type = "FTA_Concentricity" Type = "FTA_Symmetry" Type = "FTA_PositionOfAnyLine" Type = "FTA_PositionOfASurface" SuperType = "FTA_Datum" Type = "FTA_DatumSimple" Type = "FTA_DatumTarget" Type = "FTA_DatumSystem" Type = "FTA_ReferenceFrame" SuperType = "FTA_Orientation" Type = "FTA_Parallelism" Type = "FTA_Perpendicularity" Type = "FTA_Angularity" SuperType = "FTA_RunOut" Type = "FTA_TotalRunOut" Type = "FTA_CircularRunOut"

### Property **Z**( double  `iZ`) (Write Only)

method get_Z will never be exposed Set the offset of the annotation

**Parameters:**

` iZ`      The offset.
Methods

### Sub **AddLeader**( )

Add a leader.  
### Sub **ApplyReferencedGeomColor**( long  `iReleatedR`,  long  `iReleatedG`,  long  `iReleatedB`)

Apply a color to referenced geometry.  
### Sub **ApplyReferencedInitColor**( )

Apply the initial color to referenced geometry.  
### Func **AssociatedRefFrame**( ) As [CATIAAssociatedRefFrame](../CATTPSInterfaces/interface_AssociatedRefFrame_66556.md)

Get the annotation on the AssociatedRefFrame interface.  
### Func **CompositeTolerance**( ) As [CATIACompositeTolerance](../CATTPSInterfaces/interface_CompositeTolerance_69422.md)

Get the annotation on the CompositeTolerance interface.  
### Func **ControledRadius**( ) As [CATIAControledRadius](../CATTPSInterfaces/interface_ControledRadius_48506.md)

Get the annotation on the ControledRadius interface.  
### Func **DatumSimple**( ) As [CATIADatumSimple](../CATTPSInterfaces/interface_DatumSimple_26229.md)

Get the annotation on the DatumSimple interface.  
### Func **DatumTarget**( ) As [CATIADatumTarget](../CATTPSInterfaces/interface_DatumTarget_26204.md)

Get the annotation on the DatumTarget interface.  
### Func **DefaultAnnotation**( ) As [CATIADefaultAnnotation](../CATTPSInterfaces/interface_DefaultAnnotation_62596.md)

Get the annotation on the DefaultAnnotation interface.  
### Func **Dimension3D**( ) As [CATIADimension3D](../CATTPSInterfaces/interface_Dimension3D_23823.md)

Get the 3D Dimension on the 3D Dimension interface.

**Parameters:**

` oDim`      The 3D Dimension.

### Func **DimensionLimit**( ) As [CATIADimensionLimit](../CATTPSInterfaces/interface_DimensionLimit_42378.md)

Get the annotation on the DimensionLimit interface.  
### Func **DimensionPattern**( ) As [CATIADimensionPattern](../CATTPSInterfaces/interface_DimensionPattern_55714.md)

Get the annotation on the DimensionPattern interface.  
### Func **EnvelopCondition**( ) As [CATIAEnvelopCondition](../CATTPSInterfaces/interface_EnvelopCondition_55494.md)

Get the annotation on the EnvelopCondition interface.  
### Func **FlagNote**( ) As [CATIAFlagNote](../CATTPSInterfaces/interface_FlagNote_13602.md)

Get the annotation on the FlagNote interface.

**Parameters:**

` oFlagNote`      The annotation Flag Note.

### Func **FreeState**( ) As [CATIAFreeState](../CATTPSInterfaces/interface_FreeState_17355.md)

Get the annotation on the FreeState interface.  
### Sub **GetSurfaces**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

Get the geometry on which the Annotation is applied to.  
### Func **GetSurfacesCount**( ) As double

Count the geometry on which the Annotation is applied to.  
### Func **HasAControledRadius**( ) As boolean

To know if the Annotation has a Controled Radius.  
### Func **HasAFreeState**( ) As boolean

To know if the Annotation has a Free State.  
### Func **HasAMaterialCondition**( ) As boolean

To know if the Annotation has a Material Condition.  
### Func **HasAParticularTolElem**( ) As boolean

To know if the Annotation has a Particuler Element.  
### Func **HasATolerancePerUnitBasisRestrictiveValue**( ) As boolean

To know if the Annotation has a Tolerance Per Unit Basis Restricted Value.  
### Func **HasAnEnvelopCondition**( ) As boolean

To know if the Annotation has an Envelop Condition.  
### Func **HasDimensionLimit**( ) As boolean

To know if the Annotation has a Dimension Limit.  
### Func **IsACompositeTolerance**( ) As boolean

To know if the Annotation is a composite Tolerance.  
### Func **IsADefaultAnnotation**( ) As boolean

To know if the Annotation is a Default Annotation.  
### Func **IsADimensionPattern**( ) As boolean

To know if the Annotation is a Dimension Pattern.  
### Func **IsAProjectedToleranceZone**( ) As boolean

To know if the Annotation is a Projected Zone.  
### Func **IsAShiftedProfileTolerance**( ) As boolean

To know if the Annotation is a Shifted Profile Tolerance.  
### Func **IsATangentPlane**( ) As boolean

To know if the Annotation is a Tangent Plane.  
### Func **IsAToleranceUnitBasisValue**( ) As boolean

To know if the Annotation is a Tolerance Unit Basis Value.  
### Func **IsAToleranceZone**( ) As boolean

Is the a Tolerance Zone.  
### Func **IsAnAssociatedRefFrame**( ) As boolean

To know if the Annotation is an Associated Reference Frame.  
### Func **MaterialCondition**( ) As [CATIAMaterialCondition](../CATTPSInterfaces/interface_MaterialCondition_61948.md)

Get the annotation on the MaterialCondition interface.  
### Sub **ModifyVisu**( )

To refresh the 3D visualization.  
### Func **Noa**( ) As [CATIANoa](../CATTPSInterfaces/interface_Noa_2040.md)

Get the annotation on the Noa interface.  
### Func **ParticularTolElem**( ) As [CATIAParticularTolElem](../CATTPSInterfaces/interface_ParticularTolElem_60749.md)

Get the annotation on the ParticularTolElem interface.  
### Func **ProjectedToleranceZone**( ) As [CATIAProjectedToleranceZone](../CATTPSInterfaces/interface_ProjectedToleranceZone_102086.md)

Get the annotation on the ProjectedToleranceZone interface.  
### Func **ReferenceFrame**( ) As [CATIAReferenceFrame](../CATTPSInterfaces/interface_ReferenceFrame_40808.md)

Get the annotation on the ReferenceFrame interface.  
### Func **Roughness**( ) As [CATIARoughness](../CATTPSInterfaces/interface_Roughness_18440.md)

Get the annotation on the Roughness interface.  
### Sub **SetXY**( double  `iX`,  double  `iY`)

method GetXY will never be exposed Set TPS coordinates in the view

**Parameters:**

` oX`      The X coordinate.
` oY`      The Y coordinate.

### Func **ShiftedProfileTolerance**( ) As [CATIAShiftedProfileTolerance](../CATTPSInterfaces/interface_ShiftedProfileTolerance_111177.md)

Get the annotation on the ShiftedProfileTolerance interface.  
### Func **TangentPlane**( ) As [CATIATangentPlane](../CATTPSInterfaces/interface_TangentPlane_30606.md)

Get the annotation on the TangentPlane interface.  
### Func **Text**( ) As [CATIAText](../CATTPSInterfaces/interface_Text_3904.md)

Get the annotation on the Text interface.

**Parameters:**

` oText`      The annotation Text.

### Func **TolerancePerUnitBasisRestrictiveValue**( ) As [CATIATolerancePerUnitBasisRestrictiveValue](../CATTPSInterfaces/interface_TolerancePerUnitBasisRestrictiveValue_287569.md)

Get the annotation on the TolerancePerUnitBasisRestrictiveValue interface.  
### Func **ToleranceUnitBasisValue**( ) As [CATIAToleranceUnitBasisValue](../CATTPSInterfaces/interface_ToleranceUnitBasisValue_110600.md)

Get the annotation on the ToleranceUnitBasisValue interface.  
### Func **ToleranceZone**( ) As [CATIAToleranceZone](../CATTPSInterfaces/interface_ToleranceZone_36203.md)

Get the annotation on the ToleranceZone interface.  
### Sub **TransfertToView**( [CATIATPSView](../CATTPSInterfaces/interface_TPSView_10208.md)  `iView`)

Move the annotation in another view.

**Parameters:**

` iView`      The destination view.