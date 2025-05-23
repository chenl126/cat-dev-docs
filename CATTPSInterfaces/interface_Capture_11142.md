# Capture (Object)

**_The interface to access a CATIACapture_**

## Properties

### Property **ActiveView**(| ) As [CATIATPSView](../CATTPSInterfaces/interface_TPSView_10208.md)

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