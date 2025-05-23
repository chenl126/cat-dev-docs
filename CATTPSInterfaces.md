# CATTPSInterfaces Framework

## Object Index

  * [Annotation](CATTPSInterfaces/interface_Annotation_22454.md)
  * [AnnotationFactory](CATTPSInterfaces/interface_AnnotationFactory_62969.md)
  * [AnnotationSet](CATTPSInterfaces/interface_AnnotationSet_36773.md)
  * [AnnotationSets](CATTPSInterfaces/interface_AnnotationSets_42954.md)
  * [Annotations](CATTPSInterfaces/interface_Annotations_27300.md)
  * [AssociatedRefFrame](CATTPSInterfaces/interface_AssociatedRefFrame_66556.md)
  * [Capture](CATTPSInterfaces/interface_Capture_11142.md)
  * [CaptureFactory](CATTPSInterfaces/interface_CaptureFactory_42816.md)
  * [Captures](CATTPSInterfaces/interface_Captures_14626.md)
  * [CompositeTolerance](CATTPSInterfaces/interface_CompositeTolerance_69422.md)
  * [ControledRadius](CATTPSInterfaces/interface_ControledRadius_48506.md)
  * [DMUTolSettingAtt](CATTPSInterfaces/interface_DMUTolSettingAtt_52882.md)
  * [DatumSimple](CATTPSInterfaces/interface_DatumSimple_26229.md)
  * [DatumTarget](CATTPSInterfaces/interface_DatumTarget_26204.md)
  * [DefaultAnnotation](CATTPSInterfaces/interface_DefaultAnnotation_62596.md)
  * [Dimension3D](CATTPSInterfaces/interface_Dimension3D_23823.md)
  * [DimensionLimit](CATTPSInterfaces/interface_DimensionLimit_42378.md)
  * [DimensionPattern](CATTPSInterfaces/interface_DimensionPattern_55714.md)
  * [EnvelopCondition](CATTPSInterfaces/interface_EnvelopCondition_55494.md)
  * [FTAInfraSettingAtt](CATTPSInterfaces/interface_FTAInfraSettingAtt_66300.md)
  * [FTASettingAtt](CATTPSInterfaces/interface_FTASettingAtt_34756.md)
  * [FlagNote](CATTPSInterfaces/interface_FlagNote_13602.md)
  * [FreeState](CATTPSInterfaces/interface_FreeState_17355.md)
  * [MaterialCondition](CATTPSInterfaces/interface_MaterialCondition_61948.md)
  * [Noa](CATTPSInterfaces/interface_Noa_2040.md)
  * [NonSemanticDatum](CATTPSInterfaces/interface_NonSemanticDatum_54142.md)
  * [NonSemanticGDT](CATTPSInterfaces/interface_NonSemanticGDT_38338.md)
  * [ParticularTolElem](CATTPSInterfaces/interface_ParticularTolElem_60749.md)
  * [ProjectedToleranceZone](CATTPSInterfaces/interface_ProjectedToleranceZone_102086.md)
  * [ReferenceFrame](CATTPSInterfaces/interface_ReferenceFrame_40808.md)
  * [Roughness](CATTPSInterfaces/interface_Roughness_18440.md)
  * [ShiftedProfileTolerance](CATTPSInterfaces/interface_ShiftedProfileTolerance_111177.md)
  * [TPSView](CATTPSInterfaces/interface_TPSView_10208.md)
  * [TPSViewFactory](CATTPSInterfaces/interface_TPSViewFactory_41420.md)
  * [TPSViews](CATTPSInterfaces/interface_TPSViews_13626.md)
  * [TangentPlane](CATTPSInterfaces/interface_TangentPlane_30606.md)
  * [Text](CATTPSInterfaces/interface_Text_3904.md)
  * [TolerancePerUnitBasisRestrictiveValue](CATTPSInterfaces/interface_TolerancePerUnitBasisRestrictiveValue_287569.md)
  * [ToleranceUnitBasisValue](CATTPSInterfaces/interface_ToleranceUnitBasisValue_110600.md)
  * [ToleranceZone](CATTPSInterfaces/interface_ToleranceZone_36203.md)
  * [UserSurface](CATTPSInterfaces/interface_UserSurface_25966.md)
  * [UserSurfaces](CATTPSInterfaces/interface_UserSurfaces_31234.md)

## Enumerated Types Index

  * [CATFTADimConfigureSnapping](CATTPSInterfaces/enum_CATFTADimConfigureSnapping_136090.md)
  * [CATFTADimCreateOn](CATTPSInterfaces/enum_CATFTADimCreateOn_54546.md)
  * [CATFTALeaderAssociativity](CATTPSInterfaces/enum_CATFTALeaderAssociativity_128196.md)

---

# CATFTADimConfigureSnapping (Enumeration)

**__**

---

# CATFTADimCreateOn (Enumeration)

---

# CATFTALeaderAssociativity (Enumeration)

**_The associativity of a FT &A (Functional Tolerancing & Annotation) leader with respect to the pointed geometrical element._**

**Values:**

` CATFTALeaderAssociativityUndefined`      When undefined, there is no leader
` CATFTALeaderAssociativityFree`      The leader is freely positioned with respect to the pointed geometrical element. This is the default.
` CATFTALeaderAssociativityPerpendicular`      The leader is perpendicular to to the pointed geometrical element

---

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

---

# AnnotationFactory (Object)

**_Interface for the TPS Factory._**
This factory is implemented on the Set object. All the created specifications are added to the Set from which this interface is retrieved.

## Methods

### Func **CreateDatum**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Datum Feature.

**Parameters:**

` iSurf`      User surface needed to construct the Datum Feature.
` oDatum`      The new created Datum Feature.

### Func **CreateDatumReferenceFrame**( ) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Reference Frame (DRF). iType = 1 : Straightness 2 : AxisStraightness 3 : Flatness 4 : Circularity 5 : Cylindricity 6 : ProfileOfALine 7 : ProfileOfASurface 8 : Position  
### Func **CreateDatumTarget**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`,  [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)  `iDatum`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Datum Target.

**Parameters:**

` iSurf`      User surface needed to construct the Datum Target.
` iDatum`      Datume Feature that is in relatino with the Datum Target.
` oDatum`      The new created Datum Target.

### Func **CreateEvoluateDatum**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`,  double  `iX`,  double  `iY`,  double  `iZ`,  boolean  `iWithLeader`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Datum Feature.

**Parameters:**

` iSurf`      User surface needed to construct the Datum Feature.
` iX`      X coordinate.
` iY`      Y coordinate.
` iZ`      Z coordinate.
` iWithLeader`      Create or not a leader on the annotation.
` oDatum`      The new created Datum Feature.

### Func **CreateEvoluateText**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`,  double  `iX`,  double  `iY`,  double  `iZ`,  boolean  `iWithLeader`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Text.

**Parameters:**

` iSurf`      User surface needed to construct the Text.
` iX`      X coordinate.
` iY`      Y coordinate.
` iZ`      Z coordinate.
` iWithLeader`      Create or not a leader on the annotation.
` oText`      The new created Text.

### Func **CreateFlagNote**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a FlagNote.

**Parameters:**

` iSurf`      User surface needed to construct the Flag Note.
` oFlagNote`      The new created Flag Note.

### Func **CreateNonSemanticDimension**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iDimensionType`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iLinearDimSubType`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Creates a non semantic Dimension specification.

**Parameters:**

` iSurf`      User surface needed to construct the Dimension.
` iDimensionType`      Type of the Dimension 0 : CATTPSUndefDimension 1 : CATTPSLinearDimension 2 : CATTPSAngularDimension 3 : CATTPSSecondLinearDim 4 : CATTPSChamferDimension 5 : CATTPSOrientedLinearDimension 6 : CATTPSOrientedAngularDimension
` iLinearDimSubType`      Sub type of LinearDimension type 0 : CATTPSDistanceDimension 1 : CATTPSDiameterDimension 2 : CATTPSRadiusDimension 3 : CATTPSThreadDimension 4 : CATTPSChamfDistDistDimension 5 : CATTPSChamfDistAngDimension
` oDimension`      The new created Dimension.

### Func **CreateRoughness**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Roughness.

**Parameters:**

` iSurf`      User surface needed to construct the Roughness.
` oRoughness`      The new created Roughness.

### Func **CreateSemanticDimension**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iType`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iSubType`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Creates a semantic Dimension specification.

**Parameters:**

` oDimension`      The new created Dimension.

### Func **CreateText**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Text.

**Parameters:**

` iAnnotation`      Annotation on which the Text will be .
` oText`      The new created Text.

### Func **CreateTextNOA**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`) As [CATIANoa](../CATTPSInterfaces/interface_Noa_2040.md)

   Create a "Text" NOA

**Parameters:**

` iSurf`      The user surface on which you apply the created NOA.
` oNoa`      The new created NOA.

### Func **CreateTextOnAnnot**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iText`,  [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)  `iAnnot`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Text grouped to an annotation.

**Parameters:**

` iText`      Character string that makes up the text.
` iAnnot`      Annotation reference needed to group the Text.
` oText`      The new created Text.

### Func **CreateToleranceWithDRF**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`,  [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)  `iDRF`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Tolerance With a Reference Frame DRF. iType = 1 : Angularity  
### Func **CreateToleranceWithoutDRF**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Create a Tolerance Without a Reference Frame (DRF). iType = 1 : Straightness 2 : AxisStraightness 3 : Flatness 4 : Circularity 5 : Cylindricity 6 : ProfileOfALine 7 : ProfileOfASurface 8 : Position  
### Func **InstanciateNOA**( [CATIANoa](../CATTPSInterfaces/interface_Noa_2040.md)  `iNoa`,  [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iSurf`) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)

   Instanciate an NOA from a Reference NOA.

**Parameters:**

` iNOA`      Reference NOA.
` iSurf`      User surface needed to construct the Dimension.
` oNOA`      The new instanciated NOA.

---

# Annotations (Collection)

**_Interface for collection of TPS objects CATIAAnnotation._**

## Methods

### Sub **Add**( [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md)  `iAnnot`)

   Add an Annotation.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve an Annotation.

---

# AnnotationSet (Object)

**_Interface for the TPS Set of objects._**

## Properties

### Property **ActiveView**( ) As [CATIATPSView](../CATTPSInterfaces/interface_TPSView_10208.md)

   Gets or Sets Annotation Set ActiveView.

**Parameters:**

` oView`      Value of CATIATPSView.

### Property **AnEmptyAnnotationsList**( ) As [CATIAAnnotations](../CATTPSInterfaces/interface_Annotations_27300.md) (Read Only)

   Retrieves an empty Annotations'Collection.

**Parameters:**

` oAnnots`      Empty Annotations' Collection.

### Property **AnnotationFactory**( ) As [CATIAAnnotationFactory](../CATTPSInterfaces/interface_AnnotationFactory_62969.md) (Read Only)

   Obtain the factory to create annotations.

**Parameters:**

` oAFact`      Annotations' factory.

### Property **Annotations**( ) As [CATIAAnnotations](../CATTPSInterfaces/interface_Annotations_27300.md) (Read Only)

   Retrieves the TPS components of the set.

**Parameters:**

` oAnnots`      Collection of returned component.

### Property **CaptureFactory**( ) As [CATIACaptureFactory](../CATTPSInterfaces/interface_CaptureFactory_42816.md) (Read Only)

   Obtain the factory to create Capture.

**Parameters:**

` opiCapFact`      Capture factory.

### Property **Captures**( ) As [CATIACaptures](../CATTPSInterfaces/interface_Captures_14626.md) (Read Only)

   Retrieves all the Captures that belong to the set.

**Parameters:**

` oCaptures`      Collection of returned Captures.

### Property **KindOfSet**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Give the kind of set (Part, Product...).

**Parameters:**

` oKindOfSet`      It could be : Part Product Product_TP Process_BB Cgr Cgr_TP.

### Property **Standard**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves the Parent Standard defined at set creation.

**Parameters:**

` oStandard`      Name of the Parent Standard applied for all TPS in the set. The Parent Standard is the international standard on which Standard File is based on. It can only be ISO, ANSI and JIS. (ANSI stands for ASME).

### Property **SwitchOn**( ) As boolean

   Gets or Sets Annotation Set Visualization.

**Parameters:**

` oDisplay`      Value of visualisation mode.

### Property **TPSViewFactory**( ) As [CATIATPSViewFactory](../CATTPSInterfaces/interface_TPSViewFactory_41420.md) (Read Only)

   Obtain the factory to create TPS Views.

**Parameters:**

` oTPSViewFact`      TPS Views' factory.

### Property **TPSViews**( ) As [CATIATPSViews](../CATTPSInterfaces/interface_TPSViews_13626.md) (Read Only)

   Retrieves all the TPSViews that belong to the set.

**Parameters:**

` oViews`      Collection of returned views.

---

# AnnotationSets (Collection)

**_Interface for collection of Annotations' Set_**

## Methods

### Func **AddInAProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iStandard`) As [CATIAAnnotationSet](../CATTPSInterfaces/interface_AnnotationSet_36773.md)

   Add a set in the product.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve a set.  
### Sub **LoadAnnotationSetsList**( )

   Loads the Annotation Sets list. This method is very useful when a cgr document containing Annotation Set is inserted in the product, because the Annotation Set is not automatically loaded If the Annotation Set is already loaded nothing happens.

---

# AssociatedRefFrame (Object)

**_Interface dedicated to manage Datum Reference Frame associated to a TPS._**

## Properties

### Property **ReferenceFrame**( ) As [CATIAAnnotation](../CATTPSInterfaces/interface_Annotation_22454.md) (Read Only)

   Retrieves the Datum Reference Frame associated to a TPS.

---

# Capture (Object)

**_The interface to access a CATIACapture_**

## Properties

### Property **ActiveView**( ) As [CATIATPSView](../CATTPSInterfaces/interface_TPSView_10208.md)

   Retrieves the active view for the capture.  
### Property **ActiveViewState**( ) As boolean

   Retrieves the Active View state, saved or Not. The Active View state describes what happens when Capture is displayed, if TRUE, the active view of the tolerancing set is replaced by the active view of the capture.  
### Property **Annotations**( ) As [CATIAAnnotations](../CATTPSInterfaces/interface_Annotations_27300.md)

   Retrieves the TPSs that are visualy managed by this Capture.  
### Property **Camera**( ) As [CATIACamera3D](../InfInterfaces/interface_Camera3D_11722.md)

   Retrieves or sets a camera.  
### Property **ClippingPlane**( ) As boolean

   Retrieves the clipping plane state, activated or Not. The Clipping plane state describes what happens when Capture is displayed, if TRUE, the active view is used to define a clipping plane. If FALSE, there is no clipping plane applied.

**Parameters:**

` oClipPlane`      The clipping plane state.

### Property **Current**( ) As boolean

   Retrieves the Capture state, current or Not.

**Parameters:**

` oCurrentState`      Capture state. if TRUE the capture is current.that means that after the creation of the capture, the future TPSs that would be added to the CATIA document will belong to the capture.

### Property **ManageHideShowBody**( ) As boolean

   Manage the visibility of Part instances, bodies and geometrical sets across the Capture.

**Parameters:**

` obManageHideShowBody`      TRUE: If Hide/Show of these elements will be managed FALSE: If Hide/Show of these elements will not be managed

### Property **Set**( ) As [CATIAAnnotationSet](../CATTPSInterfaces/interface_AnnotationSet_36773.md) (Read Only)

   Retrieves tolerancing set the Capture belongs too.  
### Property **TPSViews**( ) As [CATIATPSViews](../CATTPSInterfaces/interface_TPSViews_13626.md)

   Retrieves the TPS Views that are visualy managed by this Capture.  
### Property **ViewPoint**( ) As boolean

   Retrieves the ViewPoint state, saved or Not. The ViewPoint state describes what happens when Capture is displayed, if TRUE, the 3D Camera of the Capture is used to change the 3D ViewPoint.  Methods

### Sub **DisplayCapture**( )

   Displays the Capture.

---

# CaptureFactory (Object)

**_Interface for the Capture Factory._**
This factory is implemented on the Set object. All the created Captures are added to the Set from which this interface is retrieved.

## Methods

### Func **CreateCapture**( ) As [CATIACapture](../CATTPSInterfaces/interface_Capture_11142.md)

   Create a Capture.

**Parameters:**

` oCapture`      The new created Capture.

---

# Captures (Collection)

**_The interface to access a CATIACaptures_**

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve a Capture.

---

# CompositeTolerance (Object)

**_Interface for accessing composite tolerance on a TPS._**
(ASME norm only)

## Properties

### Property **BoxCount**( ) As double (Read Only)

   Retrieves datum count.  
### Property **Value**( ) As double (Read Only)

   Retrieves value (in millimeters).

**Parameters:**

` oValue`      Positive or equal to -1 which means not valuated.

---

# ControledRadius (Object)

**_Interface for accessing Controled Radius modifier on a linear TPS (ASME norm only)._**
This interface is exposed only by radius linear TPS.

## Properties

### Property **Modifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves Controled Radius modifier.

---

# DatumSimple (Object)

**_Interface for Simple Datum TPS (datum entity)._**
TPS for Technological Product Specifications.

## Properties

### Property **Label**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets Label.  
### Property **Targets**( ) As [CATIAAnnotations](../CATTPSInterfaces/interface_Annotations_27300.md) (Read Only)

   Retrieves a CATITPSList to read the list of datum target. All objects of the list adhere to CATITPSDatumTarget.

---

# DatumTarget (Object)

**_Interface for Datum Target TPS (datum entity)._**
TPS for Technological Product Specifications.

## Properties

### Property **Datum**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Retrieves simple datum, the target belongs to.  
### Property **Label**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves Label.

---

# DefaultAnnotation (Object)

**_This interface is used to get information about default annotation._**
Ther is two kinds of default annotation : \- with a manual selection \- with a selection automatic

## Properties

### Property **LinkWiGeomType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Get the type of link between the default annotation and the geometry. Return E_FAIL if the annotation is not a default one.

**Parameters:**

` oLinkWiGeom`      Type of link.

### Property **SearchAlgoType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Get the type of search algo to find geometry on which the annotation apply to. Return E_FAIL if the annotation is not a default one.

**Parameters:**

` oAlgo`      Type of algo.
Methods

### Func **IsInAutomaticSearchMode**( ) As boolean

   Get the type of search algo Return E_FAIL if the annotation is not a default one.

**Parameters:**

` oIsAutoMode`      oIsAutoMode = TRUE if Automatic mode

---

# Dimension3D (Object)

**__**

## Methods

### Func **Get2dAnnot**( ) As [CATIADrawingDimension](../DraftingInterfaces/interface_DrawingDimension_55138.md)

   Retrieves Drafting Dimension.

---

# DimensionLimit (Object)

**_Represents the limit object of tolerance dimensions._**

## Properties

### Property **DimensionLimitType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the dimension limit type.

**Legal values** : Valid dimension limit type values are:

  * CATTPSDLNotDefined
  * CATTPSDLNumerical
  * CATTPSDLTabulated
  * CATTPSDLSingleLimit

### Property **Modifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the dimension single limit modifier.  
### Property **Nominalvalue**( ) As double (Read Only)

   Returns the dimension limit nominal value.
This value is expressed in millimeters.  
### Property **SymetricValue**( ) As boolean

   Returns or sets whether the dimension limit is symmetric.
TRUE if it is symmetric.  
### Property **TabulatedLimit**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the dimension tabulated limit.
This tabulated limit is expressed as a string.  Methods

### Sub **Limits**( double  `oBottom`,  double  `oUp`)

   Retrieves dimension limit values.
These values are expressed in millimeters.

**Parameters:**

` oBottom`      The dimension limit bottom value
` oUp`      The dimension limit up value

### Sub **PutLimits**( double  `iBottom`,  double  `iUp`)

   Sets dimension limit values.
These values are expressed in millimeters.

**Parameters:**

` iBottom`      The dimension limit bottom value
` iUp`      The dimension limit up value

---

# DimensionPattern (Object)

**_Interface to dimension pattern._**

## Properties

### Property **InstanceCount**( ) As double (Read Only)

   Get count of instances.

---

# DMUTolSettingAtt (Object)

**_Represents the DMU Tolerancing setting controller object._**

**Role** : The DMU Tolerancing setting controller object deals with the setting parameters displayed in:

  * The DMU Tolerancing property page for the Related Surface Color and the Design Mode setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Digital Mockup** to unfold the workbench list
    * Click **DMU Tolerancing Review**
  * The Cgr Management property page for the Save in CGR setting parameter.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Infrastructure** to unfold the workbench list
    * Click **Product Structure**
    * Click the **Cgr Management** property page

The Save in CGR setting parameter represents the state of the check button named: Save FTA 3D Annotation representation in CGR.

## Properties

### Property **DesignMode**( ) As boolean

   Returns or sets the Design Mode setting parameter value.

**True** if the Design Mode setting parameter is checked and thus set to Automatic.

**Role** : When set to True, models are loaded in Design Mode to access technological data. Otherwise, when set to False, models are loaded in Visualization Mode, and only visualization data is loaded.  
### Property **PrevArea**( ) As boolean

   Returns or sets the Preview Area setting parameter value.

**True** if the Preview Area setting parameter is checked.  
### Property **SaveCGR**( ) As boolean

   Returns or sets the Save in CGR setting parameter value.

**True** if the Save in CGR setting parameter is checked.

**Role** : When set to True, the FTA 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  
### Property **SectPattern**( ) As boolean

   Returns or sets the Pattern of Visu setting parameter value.

**True** if the Pattern of Visu setting parameter is checked.

**Role** : When set to True, the FTA 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  Methods

### Func **GetDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Design Mode setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetPrevAreaInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Preview Area setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **GetRelatedColors**( long  `oRelatedR`,  long  `oRelatedG`,  long  `oRelatedB`)

   Retrieves the Related Surface Color setting parameter value.

**Role** : The Related Surface Color setting parameter defines the color of the annotation related surfaces, that is, of all the surfaces referenced or toleranced using the CATIA V4 FD&T function.

**Legal values** :The three color indexes range from 0 to 255.

**Parameters:**

` oRelatedR`      [out] The Related Surface Color red index
` oRelatedG`      [out] The Related Surface Color green index
` oRelatedB`      [out] The Related Surface Color blue index

### Func **GetRelatedColorsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Related Surface Color setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSaveCGRInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Save in CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSectPatternInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Pattern of Visu setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetDesignModeLock**( boolean  `iLocked`)

   Locks or unlocks the Design Mode setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPrevAreaLock**( boolean  `iLocked`)

   Locks or unlocks the Preview Area setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetRelatedColors**( long  `iRelatedR`,  long  `iRelatedG`,  long  `iRelatedB`)

   Sets the Related Surface Color setting parameter value.

**Role** : The Related Surface Color setting parameter defines the color of the annotation related surfaces, that is, of all the surfaces referenced or toleranced using the CATIA V4 FD&T function.

**Legal values** :The three color indexes range from 0 to 255.

**Parameters:**

` iRelatedR`      [in] The Related Surface Color red index
` iRelatedG`      [in] The Related Surface Color green index
` iRelatedB`      [in] The Related Surface Color blue index

### Sub **SetRelatedColorsLock**( boolean  `iLocked`)

   Locks or unlocks the Related Surface Color setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSaveCGRLock**( boolean  `iLocked`)

   Locks or unlocks the Save in CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSectPatternLock**( boolean  `iLocked`)

   Locks or unlocks the Pattern of Visu setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.

---

# EnvelopCondition (Object)

**_Interface for accessing Envelop Condition modifier on a TPS._**

## Properties

### Property **Modifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves Envelop Condition modifier.

---

# FlagNote (Object)

**_Interface for the TPS Flag Note object._**

## Properties

### Property **FlagNoteText**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves flag text.  
### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves text.  Methods

### Func **URL**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves url.

**Parameters:**

` iIndex`      Index of url.
` oUrl`      url

---

# FreeState (Object)

**_Interface for accessing Free State modifier on a TPS._**

## Properties

### Property **Modifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves Free State modifier.

---

# FTAInfraSettingAtt (Object)

**_Represents the FT &A (Functional Tolerancing & Annotation) infrastructure setting controller object._**

**Role** : The FT&A infrastructure setting controller object deals with the setting parameters displayed in:

  * The Tolerancing property page for the Tolerancing Standard and the Leader Associativity setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **Tolerancing**
  * The Display property page for the Grid Display, the Grid Snap Point, the Allow Distorsions, the Grid Primary Spacing, the Grid Secondary Step, the GridV Primary Spacing, the GridV Secondary Step, the Under Set Tree Visu, the Under View Tree Visu, and the Under Feature Tree Visu setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **Display**
  * The Manipulators property page for the Manipulator Reference Size, the Manipulator Zoom Capability, and the Move After Creation, setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **Manipulators**
  * The View/Annotation Plane property page for the View Associativity, the View Referential, the View Referential Zoomable, and the View Profile setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **View/Annotation Plane**
  * The Cgr Management property page for the Save in CGR setting parameter.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Infrastructure** to unfold the workbench list
    * Click **Product Structure**
    * Click **Cgr Management**

The Save in CGR setting parameter represents the state of the check button named: Save FTA 3D Annotation representation in CGR.

## Properties

### Property **AllowDistortions**( ) As boolean

   Returns or sets the Allow Distortions setting parameter value.

**True** if the Allow Distortions setting parameter is checked and thus enables distorsions.

**Role** : The Allow Distortions setting parameter defines whether grid spacing and graduations are the same horizontally and vertically (no distorsion) or not (distorsions enabled).  
### Property **GridDisplay**( ) As boolean

   Returns or sets the Grid Display setting parameter value.

**True** if the Grid Display setting parameter is checked and thus enables the grid to be displayed.

**Role** : The Grid Display setting parameter displays a grid on the active view.  
### Property **GridPrimarySpacing**( ) As double

   Returns or sets the Grid Primary Spacing setting parameter value.

**Role** : The Grid Primary Spacing setting parameter defines the horizontal spacing on the grid, expressed in millimiters. The default value is 100mm.  
### Property **GridSecondaryStep**( ) As long

   Returns or sets the Grid Secondary Step setting parameter value.

**Role** : The Grid Secondary Step setting parameter defines the grid's horizontal graduations. The default value is 10.  
### Property **GridSnapPoint**( ) As boolean

   Returns or sets the Grid Snap Point setting parameter value.

**True** if the Grid Snap Point setting parameter is checked and thus enables the annotation to be snapped to the nearest grid point. Otherwise, the gris is not used to anchor the annotation.  
### Property **GridVPrimarySpacing**( ) As double

   Returns or sets the GridV Primary Spacing setting parameter value.

**Role** : The GridV Primary Spacing setting parameter defines the vertical spacing on the grid, expressed in millimiters. The default value is 100mm. Set this value only if distorsions are allowed thanks to the AllowDistortions property. Otherwise, the value sets to the Grid Primary Spacing setting parameter thanks to the GridPrimarySpacing for horizontal spacing is taken into account.  
### Property **GridVSecondaryStep**( ) As long

   Returns or sets the GridV Secondary Step setting parameter value.

**Role** : The GridV Secondary Step setting parameter defines the grid's vertical graduations. The default value is 10. Set this value only if distorsions are allowed thanks to the AllowDistortions property. Otherwise, the value sets to the Grid Secondary Step setting parameter thanks to the GridSecondaryStep for the number of horizontal graduations is taken into account.  
### Property **LeaderAssociativity**( ) As [CATFTALeaderAssociativity](../CATTPSInterfaces/enum_CATFTALeaderAssociativity_128196.md)

   Returns or sets the Leader Associativity setting parameter value.

**Role** : The Leader Associativity setting parameter defines the associativity of a leader with the pointed geometrical element.  
### Property **ManRefSiz**( ) As double

   Returns or sets the Manipulator Reference Size setting parameter value.

**Role** : The Manipulator Reference Size setting parameter defines the size of the manipulator attached to the end of an annotation leader. The default value is 2mm.  
### Property **ManZooCap**( ) As boolean

   Returns or sets the Manipulator Zoom Capability setting parameter value.

**True** if the Manipulator Zoom Capability setting parameter is checked and thus enables the annotation leader end manipulator to be zoomable. Otherwise, it is not zoomable.  
### Property **MoveAfterCreation**( ) As boolean

   Returns or sets the Move After Creation setting parameter value.

**True** if the Move After Creation setting parameter is checked and thus enables the annotation leader end manipulator to be moved, after the annotation creation, along lines or curves that represent the intersection between the geometry and the annotation's plane. Otherwise, the annotation leader end manipulator cannot be moved.  
### Property **SaveInCGR**( ) As boolean

   Returns or sets the Save In CGR setting parameter value.

**True** if the Save In CGR setting parameter is checked.

**Role** : When set to True, the FT&A 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  
### Property **Standard**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Tolerancing Standard setting parameter value.

**Role** : The Tolerancing Standard setting parameter defines the standard of the annotation's set.

**Legal values** : five conventional standards are available:

  * **ASME** : American Society for Mechanical Engineers
  * **ASME_3D** : American Society for Mechanical Engineers
  * **ANSI** : American National Standards Institute
  * **JIS** : Japanese Industrial Standard
  * **ISO** : International Organization for Standardization

### Property **UnderFeature**( ) As boolean

   Returns or sets the Under Geometric Feature Nodes setting parameter value.

**True** if the Under Geometric Feature Nodes setting parameter is checked and thus enables 3D annotations to be displayed in the specification tree. This lets you view 3D annotations under the Part Design or Generative Shape Design feature nodes to which they are applied.  
### Property **UnderSet**( ) As boolean

   Returns or sets the Under Annotation Set Node setting parameter value.

**True** if the Under Annotation Set Node setting parameter is checked and thus enables 3D annotations to be displayed under the annotation set node in the specification tree. Set this parameter to True only if the Under View/Annotation Plane Nodes setting parameter managed by UnderView is set to True.  
### Property **UnderView**( ) As boolean

   Returns or sets the Under View/Annotation Plane Nodes setting parameter value.

**True** if the Under View/Annotation Plane Nodes setting parameter is checked and thus enables 3D annotations to be displayed under the view/annotation plane nodes in the specification tree. This lets you view 3D annotations under the view node to which they are linked.  
### Property **ViewAssociativity**( ) As boolean

   Returns or sets the View Associativity setting parameter value.

**True** if the View Associativity setting parameter is checked and thus enables the associativity of the view/annotation plane associativity with the pointed geometrical elements.

**Role** : The View Associativity setting parameter defines whether the views created are associative with the geometry. When views are associative to the geometry, any modification applied to the geometry or to the axis system is reflected in the view definition.  
### Property **ViewProfile**( ) As boolean

   Returns or sets the View Profile setting parameter value.

**True** if the View Profile setting parameter is checked and thus enables the view/annotation plane profile on the part/product to be displayed.  
### Property **ViewReferential**( ) As boolean

   Returns or sets the View Referential setting parameter value.

**True** if the View Referential setting parameter is checked and thus enables the display of the active annotation plane axis system.  
### Property **ViewReferentialZoomable**( ) As boolean

   Returns or sets the View Referential Zoomable setting parameter value.

**True** if the View Referential Zoomable setting parameter is checked and thus enables the annotation plane axis to be zoomable.  Methods

### Func **GetAllowDistortionsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Allow Distorsions setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Grid Display setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridPrimarySpacingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Grid Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridSecondaryStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Grid Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridSnapPointInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Grid Snap Point setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridVPrimarySpacingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the GridV Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridVSecondaryStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the GridV Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLeaderAssociativityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Leader Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetManRefSizInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Manipulator Reference Size setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetManZooCapInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Manipulator Zoom Capability setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMoveAfterCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Move After Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSaveInCGRInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Save In CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetStandardInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Tolerancing Standard setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUnderFeatureInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Under Geometric Feature Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUnderSetInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Under Annotation Set Node setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUnderViewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Under View/Annotation Plane Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewAssociativityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the View Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewProfileInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the View Profile setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewReferentialInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the View Referential setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewReferentialZoomableInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the View Referential Zoomable setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAllowDistortionsLock**( boolean  `iLocked`)

   Locks or unlocks the Allow Distorsions setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridDisplayLock**( boolean  `iLocked`)

   Locks or unlocks the Grid Display setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridPrimarySpacingLock**( boolean  `iLocked`)

   Locks or unlocks the Grid Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridSecondaryStepLock**( boolean  `iLocked`)

   Locks or unlocks the Grid Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridSnapPointLock**( boolean  `iLocked`)

   Locks or unlocks the Grid Snap Point setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridVPrimarySpacingLock**( boolean  `iLocked`)

   Locks or unlocks the GridV Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridVSecondaryStepLock**( boolean  `iLocked`)

   Locks or unlocks the GridV Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLeaderAssociativityLock**( boolean  `iLocked`)

   Locks or unlocks the Leader Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetManRefSizLock**( boolean  `iLocked`)

   Locks or unlocks the Manipulator Reference Size setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetManZooCapLock**( boolean  `iLocked`)

   Locks or unlocks the Manipulator Zoom Capability setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMoveAfterCreationLock**( boolean  `iLocked`)

   Locks or unlocks the Move After Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSaveInCGRLock**( boolean  `iLocked`)

   Locks or unlocks the Save In CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetStandardLock**( boolean  `iLocked`)

   Locks or unlocks the Tolerancing Standard setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUnderFeatureLock**( boolean  `iLocked`)

   Locks or unlocks the Under Geometric Feature Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUnderSetLock**( boolean  `iLocked`)

   Locks or unlocks the Under Annotation Set Node setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUnderViewLock**( boolean  `iLocked`)

   Locks or unlocks the Under View/Annotation Plane Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewAssociativityLock**( boolean  `iLocked`)

   Locks or unlocks the View Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewProfileLock**( boolean  `iLocked`)

   Locks or unlocks the View Profile setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewReferentialLock**( boolean  `iLocked`)

   Locks or unlocks the View Referential setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewReferentialZoomableLock**( boolean  `iLocked`)

   Locks or unlocks the View Referential Zoomable setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.

---

# FTASettingAtt (Object)

**_The interface to access a CATIAFTASettingAtt._**

## Properties

### Property **AlphabeticOrder**( ) As boolean

   Returns or sets the AlphabeticOrder setting parameter value.

**True** if the AlphabeticOrder setting parameter is checked.

**Role** : When set to True, the FTA 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  
### Property **AngulaireGeneralTolClass**( ) As long

   Returns or sets the Dimension general class parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **BodyHideInCapture**( ) As long

   Returns or sets the Visibility of Part instances, bodies and geometrical sets in Capture.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimAfterCre**( ) As boolean

   Returns or sets the Dimension After Creaation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimAfterMod**( ) As boolean

   Returns or sets the Dimension After Modification parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimBeforeCre**( ) As boolean

   Returns or sets the Dimension Before Creation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimBeforeMod**( ) As boolean

   Returns or sets the Dimension Before Modification parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimBlankingCre**( ) As boolean

   Returns or sets the Dimension Blanking Creation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimBlankingMod**( ) As boolean

   Returns or sets the Dimension Blanking Modification parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimConfigureSnapping**( ) As [CATFTADimConfigureSnapping](../CATTPSInterfaces/enum_CATFTADimConfigureSnapping_136090.md)

   Returns or sets the DimConfigureSnapping parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimConstantOffset**( ) As boolean

   Returns or sets the Constant Offset parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimCreateOn**( ) As [CATFTADimCreateOn](../CATTPSInterfaces/enum_CATFTADimCreateOn_54546.md)

   Returns or sets the DimCreateOn parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimLinePosValue**( ) As double

   Returns or sets the Dimension Line Position Value parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimLineUpBaseAngle**( ) As double

   Returns or sets the Dimension Line Up Base Angle parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimLineUpBaseLength**( ) As double

   Returns or sets the Dimension Line Up Base Length parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimLineUpCumul**( ) As boolean

   Returns or sets the Dimension Line Up Cululated parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimLineUpFunnel**( ) As boolean

   Returns or sets the Dimension Line Up Funnel parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimLineUpOffsetBetDimAngle**( ) As double

   Returns gets the DimLineUpOffsetBetDimAngle parameter.

**Parameters:**

` oValue`      Output value of the DimLineUpOffsetBetDimAngle. If return code E_FAIL oValue is not obtained. If return code S_OK oValue is obtained.

### Property **DimLineUpOffsetBetDimLength**( ) As double

   Returns gets the DimLineUpOffsetBetDimLength parameter.

**Parameters:**

` oValue`      Output value of the DimLineUpOffsetBetDimLength. If return code E_FAIL oValue is not obtained. If return code S_OK oValue is obtained.

### Property **DimLineUpOffsetToRefAngle**( ) As double

   Returns gets the DimLineUpOffsetToRefAngle parameter.

**Parameters:**

` oValue`      Output value of the DimLineUpOffsetToRefAngle. If return code E_FAIL oValue is not obtained. If return code S_OK oValue is obtained.

### Property **DimLineUpOffsetToRefLength**( ) As double

   Returns gets the DimLineUpOffsetToRefLength parameter.

**Parameters:**

` oValue`      Output value of the DimLineUpOffsetToRefLength. If return code E_FAIL oValue is not obtained. If return code S_OK oValue is obtained.

### Property **DimLineUpStack**( ) As boolean

   Returns or sets the Dimension Line Up Stack parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimManualPositionning**( ) As boolean

   Returns or sets the Manual Positionning parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimMove2dPartCre**( ) As boolean

   Returns or sets the Dimension Move 2D Creation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimMove2dPartMod**( ) As boolean

   Returns or sets the Dimension Move 2D Modification parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimMoveDimLineCre**( ) As boolean

   Returns or sets the Dimension Move Dimension Line Creation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimMoveDimLineMod**( ) As boolean

   Returns or sets the Dimension Move Dimension Line Modification parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimMoveLeaderCre**( ) As boolean

   Get the Dimension leader Creation parameter.

**Parameters:**

` oValue`      Output value of the Dimension Leader creation check box status. If return code E_FAIL oValue is not obtained. If return code S_OK oValue is obtained.

### Property **DimMoveLeaderMod**( ) As boolean

   Returns gets the Dimension leader modification parameter.

**Parameters:**

` oValue`      Output value of the Dimension Leader modification check box status. If return code E_FAIL oValue is not obtained. If return code S_OK oValue is obtained.

### Property **DimMoveSubPart**( ) As boolean

   Returns or sets the DimMoveSubPart parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimMoveValueCre**( ) As boolean

   Returns or sets the Dimension Move Value Creation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimMoveValueMod**( ) As boolean

   Returns or sets the Dimension Move Value Modification parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimORunCre**( ) As boolean

   Returns or sets the Dimension Over Run Creation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimORunMod**( ) As boolean

   Returns or sets the Dimension Over Run Modification parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimOriDefaultSymb**( ) As boolean

   Returns or sets the Dimension Orientation Default Symbol parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DimSnapping**( ) As boolean

   Returns or sets the Dimension Snapping parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GeneralTolClass**( ) As long

   Returns or sets the Dimension general class parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **HighlightDefAnnot**( ) As boolean

   Returns or sets the Highlight Def Annot parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **NoaCreation**( ) As boolean

   Returns or sets the Noa Creation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **NonSemanticAllwaysUpgrade**( ) As boolean

   Returns or sets the Non SemanticAllways Upgrade parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **NonSemanticAllwaysUpgradeGeneralTol**( ) As boolean

   Returns or sets the Non SemanticAllways Upgrade general tolerance parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **NonSemanticDimAllowed**( ) As boolean

   Returns or sets the Non Semantic Dim Allowed parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **NonSemanticMarked**( ) As boolean

   Returns or sets the Non Semantic Marked parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **NonSemanticTolAllowed**( ) As boolean

   Returns or sets the Non Semantic Tol Allowed parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ParametersInTree**( ) As boolean

   Returns or sets the Parameters in tree parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **RotationSnapAngle**( ) As double

   Returns or sets the Rotation Snap Angle parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **RotationSnapAuto**( ) As boolean

   Returns or sets the Rotation Snap Auto parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SectPattern**( ) As boolean

   Returns or sets the Pattern of Visu setting parameter value.

**True** if the Pattern of Visu setting parameter is checked.

**Role** : When set to True, the FTA 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  
### Property **SelectPublishedGeometry**( ) As boolean

   Returns or sets the Slect Published Geometry parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ShiftedProfile**( ) As boolean

   Returns or sets the Shifted Profile parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetAlphabeticOrderInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the AlphabeticOrder setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetAngulaireGeneralTolClassInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension general class tolerance setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetBodyHideInCaptureInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Visibility of Part instances, bodies and geometrical sets in Capture.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimAfterCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension After Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimAfterModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension After Modification setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimBeforeCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Before Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimBeforeModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Before Modification setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimBlankingCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Blanking Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimBlankingModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Blanking Modification setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimConfigureSnappingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the DimMoveSubPart setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimConstantOffsetInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Constant Offset setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimCreateOnInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the DimCreateOn setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLinePosValueInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Line Position Value setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpBaseAngleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Line Up Base Angle setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpBaseLengthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Line Up Base Length setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpCumulInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Line Up Cululated setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpFunnelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Line Up Funnel setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpOffsetBetDimAngleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the DimLineUpOffsetBetDimAngle setting parameter value.

**Parameters:**

` AdminLevel`      Input/Output parameter, is the administration level.
` oLocked`      Input/Output parameter, is the lock status of the check button.
` oModified`      Output paramter which gives the status as boolean if the status is modified. If return code E_FAIL the values are not obtained. If return code S_OK the values are obtained.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpOffsetBetDimLengthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the DimLineUpOffsetBetDimLength setting parameter value.

**Parameters:**

` AdminLevel`      Input/Output parameter, is the administration level.
` oLocked`      Input/Output parameter, is the lock status of the check button.
` oModified`      Output paramter which gives the status as boolean if the status is modified. If return code E_FAIL the values are not obtained. If return code S_OK the values are obtained.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpOffsetToRefAngleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the DimLineUpOffsetToRefAngle setting parameter value.

**Parameters:**

` AdminLevel`      Input/Output parameter, is the administration level.
` oLocked`      Input/Output parameter, is the lock status of the check button.
` oModified`      Output paramter which gives the status as boolean if the status is modified. If return code E_FAIL the values are not obtained. If return code S_OK the values are obtained.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpOffsetToRefLengthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the DimLineUpOffsetToRefLength setting parameter value.

**Parameters:**

` AdminLevel`      Input/Output parameter, is the administration level.
` oLocked`      Input/Output parameter, is the lock status of the check button.
` oModified`      Output paramter which gives the status as boolean if the status is modified. If return code E_FAIL the values are not obtained. If return code S_OK the values are obtained.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimLineUpStackInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Line Up Stack setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimManualPositionningInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Manual Positionning setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMove2dPartCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Move 2D Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMove2dPartModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Move 2D Modification setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMoveDimLineCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Move Dimension Line Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMoveDimLineModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Move Dimension Line Modification setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMoveLeaderCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension leader Creation setting parameter value.

**Parameters:**

` AdminLevel`      Input/Output parameter, is the administration level.
` oLocked`      Input/Output parameter, is the lock status of the check button.
` oModified`      Output paramter which gives the status as boolean if the status is modified. If return code E_FAIL the values are not obtained. If return code S_OK the values are obtained.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMoveLeaderModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension leader modification setting parameter value.

**Parameters:**

` AdminLevel`      Input/Output parameter, is the administration level.
` oLocked`      Input/Output parameter, is the lock status of the check button.
` oModified`      Output paramter which gives the status as boolean if the status is modified. If return code E_FAIL the values are not obtained. If return code S_OK the values are obtained.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMoveSubPartInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the DimMoveSubPart setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMoveValueCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Move Value Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimMoveValueModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Move Value Modification setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimORunCreInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Over Run Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimORunModInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Over Run Modification setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimOriDefaultSymbInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Orientation Default Symbol setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetDimSnappingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension Snapping setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetGeneralTolClassInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Dimension general class tolerance setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetHighlightDefAnnotInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Highlight Def Annot setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetNoaCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Noa Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetNonSemanticAllwaysUpgradeGeneralTolInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Non Semantic Allways Upgrade general tolerance setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetNonSemanticAllwaysUpgradeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Non Semantic Allways Upgrade setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetNonSemanticDimAllowedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Non Semantic Dim Allowed setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetNonSemanticMarkedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Non Semantic Marked setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetNonSemanticTolAllowedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Non Semantic Tol Allowed setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetParametersInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Parameters in tree setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetRotationSnapAngleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Rotation Snap Angle setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetRotationSnapAutoInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Rotation Snap Auto setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSectPatternInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Pattern of Visu setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSelectPublishedGeometryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Select Published Geometry setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetShiftedProfileInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Shifted Profile setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetAlphabeticOrderLock**( boolean  `iLocked`)

   Locks or unlocks the AlphabeticOrder setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAngulaireGeneralTolClassLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension general class parameter.  
### Sub **SetBodyHideInCaptureLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension general class parameter.  
### Sub **SetDimAfterCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension After Creaation parameter.  
### Sub **SetDimAfterModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension After Modification parameter.  
### Sub **SetDimBeforeCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Before Creation parameter.  
### Sub **SetDimBeforeModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Before Modification parameter.  
### Sub **SetDimBlankingCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Blanking Creation parameter.  
### Sub **SetDimBlankingModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Blanking Modification parameter.  
### Sub **SetDimConfigureSnappingLock**( boolean  `iLocked`)

   Locks or unlocks the DimConfigureSnapping parameter.  
### Sub **SetDimConstantOffsetLock**( boolean  `iLocked`)

   Locks or unlocks the Constant Offset parameter.  
### Sub **SetDimCreateOnLock**( boolean  `iLocked`)

   Locks or unlocks the DimCreateOn parameter.  
### Sub **SetDimLinePosValueLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Line Position Value parameter.  
### Sub **SetDimLineUpBaseAngleLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Line Up Base Angle parameter.  
### Sub **SetDimLineUpBaseLengthLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Line Up Base Length parameter.  
### Sub **SetDimLineUpCumulLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Line Up Cululated parameter.  
### Sub **SetDimLineUpFunnelLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Line Up Funnel parameter.  
### Sub **SetDimLineUpOffsetBetDimAngleLock**( boolean  `iLocked`)

   Locks or unlocks the DimLineUpOffsetBetDimAngle parameter.

**Parameters:**

` iLocked`      Input value of the DimLineUpOffsetBetDimAngle (lock/unlock). If return code E_FAIL iLocked is not set. If return code S_OK iLocked is set.

### Sub **SetDimLineUpOffsetBetDimLengthLock**( boolean  `iLocked`)

   Locks or unlocks the DimLineUpOffsetBetDimLength parameter.

**Parameters:**

` iLocked`      Input value of the DimLineUpOffsetBetDimLength (lock/unlock). If return code E_FAIL iLocked is not set. If return code S_OK iLocked is set.

### Sub **SetDimLineUpOffsetToRefAngleLock**( boolean  `iLocked`)

   Locks or unlocks the DimLineUpOffsetToRefAngle parameter.

**Parameters:**

` iLocked`      Input value of the DimLineUpOffsetToRefAngle (lock/unlock). If return code E_FAIL iLocked is not set. If return code S_OK iLocked is set.

### Sub **SetDimLineUpOffsetToRefLengthLock**( boolean  `iLocked`)

   Locks or unlocks the DimLineUpOffsetToRefLength parameter.

**Parameters:**

` iLocked`      Input value of the DimLineUpOffsetToRefLength (lock/unlock). If return code E_FAIL iLocked is not set. If return code S_OK iLocked is set.

### Sub **SetDimLineUpStackLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Line Up Stack parameter.  
### Sub **SetDimManualPositionningLock**( boolean  `iLocked`)

   Locks or unlocks the Manual Positionning parameter.  
### Sub **SetDimMove2dPartCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Move 2D Creation parameter.  
### Sub **SetDimMove2dPartModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Move 2D Modification parameter.  
### Sub **SetDimMoveDimLineCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Move Dimension Line Creation parameter.  
### Sub **SetDimMoveDimLineModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Move Dimension Line Modification parameter.  
### Sub **SetDimMoveLeaderCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension leader Creation parameter.

**Parameters:**

` iLocked`      Input value of the Dimension leader creation check box lock/unlock status. If return code E_FAIL iLocked is not set. If return code S_OK iLocked is set.

### Sub **SetDimMoveLeaderModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension leader modification parameter.

**Parameters:**

` iLocked`      Input value of the Dimension leader modification check box (lock/unlock). If return code E_FAIL iLocked is not set. If return code S_OK iLocked is set.

### Sub **SetDimMoveSubPartLock**( boolean  `iLocked`)

   Locks or unlocks the DimMoveSubPart parameter.  
### Sub **SetDimMoveValueCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Move Value Creation parameter.  
### Sub **SetDimMoveValueModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Move Value Modification parameter.  
### Sub **SetDimORunCreLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Over Run Creation parameter.  
### Sub **SetDimORunModLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Over Run Modification parameter.  
### Sub **SetDimOriDefaultSymbLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Orientation Default Symbol parameter.  
### Sub **SetDimSnappingLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension Snapping parameter.  
### Sub **SetGeneralTolClassLock**( boolean  `iLocked`)

   Locks or unlocks the Dimension general class parameter.  
### Sub **SetHighlightDefAnnotLock**( boolean  `iLocked`)

   Locks or unlocks the Highlight Def Annot parameter.  
### Sub **SetNoaCreationLock**( boolean  `iLocked`)

   Locks or unlocks the Noa Creation parameter.  
### Sub **SetNonSemanticAllwaysUpgradeGeneralTolLock**( boolean  `iLocked`)

   Locks or unlocks the Non Semantic Allways Upgrade general tolerance parameter.  
### Sub **SetNonSemanticAllwaysUpgradeLock**( boolean  `iLocked`)

   Locks or unlocks the Non Semantic Allways Upgrade parameter.  
### Sub **SetNonSemanticDimAllowedLock**( boolean  `iLocked`)

   Locks or unlocks the Non Semantic Dim Allowed parameter.  
### Sub **SetNonSemanticMarkedLock**( boolean  `iLocked`)

   Locks or unlocks the Non Semantic Marked parameter.  
### Sub **SetNonSemanticTolAllowedLock**( boolean  `iLocked`)

   Locks or unlocks the Non Semantic Tol Allowed parameter.  
### Sub **SetParametersInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the Parameters in tree parameter.  
### Sub **SetRotationSnapAngleLock**( boolean  `iLocked`)

   Locks or unlocks the Rotation Snap Angle parameter.  
### Sub **SetRotationSnapAutoLock**( boolean  `iLocked`)

   Locks or unlocks the Rotation Snap Auto parameter.  
### Sub **SetSectPatternLock**( boolean  `iLocked`)

   Locks or unlocks the Pattern of Visu setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSelectPublishedGeometryLock**( boolean  `iLocked`)

   Locks or unlocks the Select Published Geometry parameter.  
### Sub **SetShiftedProfileLock**( boolean  `iLocked`)

   Locks or unlocks the Shifted Profile parameter.

---

# MaterialCondition (Object)

**_Interface for accessing Material Condition modifier on a TPS._**

## Properties

### Property **Modifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves Material Condition modifier.

---

# Noa (Object)

**_Interface for the TPS Noa object._**

## Properties

### Property **FlagText**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves Flag Text.  
### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets Text Representation.

**Parameters:**

` oText`      Returned text for graphical representation.
Methods

### Func **URL**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves url.

**Parameters:**

` iIndex`      Index of url.
` oUrl`      url

---

# NonSemanticDatum (Object)

**__**

---

# NonSemanticGDT (Object)

**__**

---

# ParticularTolElem (Object)

**_Interface for accessing particular geometry of the toleranced element._**

## Properties

### Property **ParticularGeometry**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Retrieves particular geometry of the toleranced element.

---

# ProjectedToleranceZone (Object)

**_Interface for accessing projected tolerance zone informations of a TPS._**
========| Position Length / |<\----------->|<\----------->| Toleranced | | | Surface - - - +-------> +=============+ \ |\ \ \ \ | Origin Direction Projected Tolerance Zone ========|

## Properties

### Property **Length**( ) As double (Read Only)

   Retrieves length of the projected tolerance zone (in millimeters). The length defines the ending point of the tolerance zone. This point can be computed by using Origin and Direction of the axis.  
### Property **Position**( ) As double (Read Only)

   Retrieves position of the projected tolerance zone (in millimeters). The position defines the starting point of the tolerance zone. This point can be computed by using Origin and Direction of the axis.

---

# ReferenceFrame (Object)

**_Interface designed to manage reference frame associated to a TPS._**
Reference frame is composed of three boxes.

```VBScript
                             Reference Frame
                            /
                      _____|_____
                     /           \
             ---------------------
             |   |   |Box|Box|Box|
             |   |   | 1 | 2 | 3 |
             ---------------------

```VBScript

        **AllDatumsSimple**
          Retrieves all datums simple used in Reference Frame.

        **Frame**
          Retrieves Frame of the TPS.

        **SetFrame**
          Set Frame of the TPS.

    ## Properties

    ### Property **AllDatumsSimple**( ) As [CATIAAnnotations](../CATTPSInterfaces/interface_Annotations_27300.md)  (Read Only)

     Retrieves all datums simple used in Reference Frame.

       **Parameters:**

         opiListDatumsSimple
                All objects of the collection

     Methods

### Sub **Frame**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  oFirstBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  oSecondBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  oThirdBox)

     Retrieves Frame of the TPS.

       **Parameters:**

         oFirstBox

         oSecondBox

         oThirdBox
                Texts in first, second and third boxes.

### Sub **SetFrame**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iFirstBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iSecondBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iThirdBox)

     Set Frame of the TPS.

       **Parameters:**

         oFirstBox

         oSecondBox

         oThirdBox
                Texts in first, second and third boxes.

---

# Roughness (Object)

**_Interface to manage Roughness TPS._**
TPS for Technological Product Specifications.

## Properties

### Property **Applicability**( ) As short

   Retrieves or sets roughness applicability.  
### Property **Obtention**( ) As short

   Retrieves or sets roughness obtention mode.  Methods

### Func **Field**( short  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves roughness field.

```VBScript
                                          Field 4
                          Field 1     ------------------
                                     /         (Field 9)
                          Field 2   /
                                   / (Field 8)  Field 5
                              \   /
                    Field 3    \ /    Field 7   Field 6

      Pour le champs 7 les lettres autorisees sont :
      M, C, R, P, X, = ,L (symbole perpendicularite de la DSES)

```

**Parameters:**

` iIndex`      Field index, from 1 to 9 from V5R13 (Fields 8 and 9 added). from 1 to 7 before V5R13
` oField`      The contain of the iIndex field.

### Sub **SetField**( short  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iField`)

   Set roughness field.

```VBScript
                                          Field 4
                          Field 1     ------------------
                                     /         (Field 9)
                          Field 2   /
                                   / (Field 8)  Field 5
                              \   /
                    Field 3    \ /    Field 7   Field 6

      Pour le champs 7 les lettres autorisees sont :
      M, C, R, P, X, = ,L (symbole perpendicularite de la DSES)

```

**Parameters:**

` iIndex`      Field index, from 1 to 9 from V5R13 (Fields 8 and 9 added). from 1 to 7 before V5R13
` iField`      The contain of the iIndex field.

---

# ShiftedProfileTolerance (Object)

**_Interface for accessing shifted tolerance zone informations of a TPS._**

## Properties

### Property **ShiftValue**( ) As double

   Retrieves or sets shift value of tolerance zone (in millimeters). The shift value is the distance between the toleranced surface and the median surface of tolerance zone. The value is always positive because shift side is given by GetShiftSide method.

---

# TangentPlane (Object)

**_Interface for accessing Tangent Plane modifier on a TPS._**

## Properties

### Property **Modifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves Tangent Plane modifier.

---

# Text (Object)

**_Interface for the TPS Text object._**

## Properties

### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Get the annotation's text.  Methods

### Func **Get2dAnnot**( ) As [CATIADrawingText](../DraftingInterfaces/interface_DrawingText_26559.md)

   Retrieves Drafting text.

---

# TolerancePerUnitBasisRestrictiveValue (Object)

**_Interface for accessing tolerance per unit basis restrictive value on a TPS._**
(ASME norm only)

## Properties

### Property **Value**( ) As double

   Retrieves value (in millimeters).

**Parameters:**

` oValue`      Positive or equal to -1 which means not valuated.

---

# ToleranceUnitBasisValue (Object)

**_Interface for accessing values of the tolerance unit basis on a TPS._**

## Methods

### Sub **SetValues**( double  `iValue1`,  double  `iValue2`)

   Set tolerance unit basis values (in millimeters).

**Parameters:**

` oValue1`      Positive or equal to -1 which means not valuated.
` oValue2`      Positive or equal to -1 which means not valuated.

### Sub **Values**( double  `oValue1`,  double  `oValue2`)

   Retrieves tolerance unit basis values (in millimeters).

**Parameters:**

` oValue1`      Positive or equal to -1 which means not valuated.
` oValue2`      Positive or equal to -1 which means not valuated.

---

# ToleranceZone (Object)

**_Interface for accessing tolerance zone informations of a TPS._**

## Properties

### Property **Form**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves tolerance zone form.  
### Property **Value**( ) As double

   Retrieves tolerance zone value (in millimeters).

---

# TPSView (Object)

**__**

---

# TPSViewFactory (Object)

**_Represents the TPS view factory object._**
All the created views are added to the annotation set object from which this interface is retrieved, thanks to the [AnnotationSet.TPSFactory](../CATTPSInterfaces/interface_AnnotationSet_36773.htm#TPSFactory) property.

## Methods

### Func **CreateView**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iViewType`) As [CATIATPSView](../CATTPSInterfaces/interface_TPSView_10208.md)

   Creates a view.

**Parameters:**

` iPlane`      The plane onto which the view will be created
` iViewType`      The view type

**Legal values** :

  * 1: Front View
  * 2: Section View
  * 3: Cut View

---

# TPSViews (Collection)

**_Interface for collection of TPS Views CATIATPSView._**

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve a TPS View.

---

# UserSurface (Object)

**__**

## Methods

### Sub **AddReference**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Add a surface in a User Surface Support

**Parameters:**

` iSupport`      The surface that you want to add in the User Surface.

### Sub **AddReferenceInAProductCtx**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProdInst`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Add a surface in a User Surface Support

**Parameters:**

` iProdInst`      The product instance where there is the geometry.
` iSupport`      The surface that you want to add in the User Surface.

### Sub **AddUserSurface**( [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)  `iUserSurf`)

   Add a User Surface Support in a User Surface Node

**Parameters:**

` iUserSurf`      The User Surface Support that you want to add in the User Surface.

---

# UserSurfaces (Collection)

**__**

## Methods

### Func **Generate**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`) As [CATIAUserSurface](../CATTPSInterfaces/interface_UserSurface_25966.md)

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