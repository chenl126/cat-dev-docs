# AnnotationSet (Object)

**_Interface for the TPS Set of objects._**

## Properties

### Property **ActiveView**(| ) As [CATIATPSView](../CATTPSInterfaces/interface_TPSView_10208.md)

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