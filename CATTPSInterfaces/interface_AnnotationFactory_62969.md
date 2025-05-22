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