# DrawingViewGenerativeBehavior (Object)

**_Represents the generative behavior of a drawing view._**

The generative behavior of a drawing view is an object that defines the parameters used to generate the drawing view from the document it represents. Main parameters include the type of the view, the plane on which the view is projected, the document to represent, and additional parameters depending on the view type.

## Properties

### Property **ColorInheritanceMode**( ) As [Cat3DColorInheritanceMode](../DraftingInterfaces/enum_Cat3DColorInheritanceMode_126115.md)

Returns or sets the view color inheritance mode.

**Example:**      This example sets the view color inheritance mode of the `MyView` drawing view to `cat3DColorInheritanceModeOn` to indicate that generated items inherit the color of the 3D elements they come from.

```VBScript
MyView.GenerativeBehavior.ColorInheritanceMode(cat3DColorInheritanceModeOn)

```

### Property **Document**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Returns or sets the document used to generate the drawing view. This document can be a CATIA Version 4 model, a CATIA Version 5 part or assembly. But it can be also just a body(partbody), according to the view links (then the document is the parent object). The document must be already loaded, that is it can be retrieved from the document collection managed by the CATIA application.

**Example:**      This example sets the document that the `MyView` drawing view should represent to the `CATPart1` CATIA Version 5 part.

```VBScript
Dim PartToDraw As Document
Set PartToDraw = CATIA.Documents.Item("CATPart1")
MyView.GenerativeBehavior.Document = PartToDraw

```

### Property **FilletRepresentation**( ) As [CatFilletRepresentation](../DraftingInterfaces/enum_CatFilletRepresentation_113677.md)

Returns or sets the view Fillet representation mode. The Fillet representation indicates how to draw lines coming from fillets.

**Example:**      This example sets the view Fillet representation of the `MyView` drawing view to `catFilletRepBoundary`

```VBScript
MyView.GenerativeBehavior.FilletRepresentation = catFilletRepBoundary

```

### Property **HiddenLineMode**( ) As [CatHiddenLineMode](../DraftingInterfaces/enum_CatHiddenLineMode_58289.md)

Returns or sets the view hidden line drawing mode. The hidden line drawing mode indicates whether to draw the hidden lines.

**Example:**      This example sets the view hidden line drawing mode of the `MyView` drawing view to `catHLRModeOn` to indicate that hidden lines must not be drawn.

```VBScript
MyView.GenerativeBehavior.HiddenLineMode = catHLRModeOn

```

### Property **ImageViewMode**( ) As [CatImageViewMode](../DraftingInterfaces/enum_CatImageViewMode_52190.md)

Returns or sets the view generation mode as pixel image.

**Returns:**      `S_OK`     if the operation succeeded. `E_FAIL`     For both methods, if an unspecified failure has occurred  **Example:**      This example sets the view image generation mode of the `MyView` drawing view to `catImageModeHRD` to indicate that view is generated as an HRD image.

```VBScript
MyView.GenerativeBehavior.CatImageViewMode(catImageModeHRD)

```

### Property **LimitBoundingBox**( ) As double

Returns or sets the bounding box limits under which a part. will not be taken into account during view generation. The value 0. means that no part will be filtered.

**Returns:**      `S_OK`     if the operation succeeded. `E_FAIL`     For both methods, if an unspecified failure has occurred  
### Property **ParentView**( ) As [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md) (Read Only)

Returns the parent view.

**Example:**      This example returns in `MyParentView` the parent view of the `MyView` drawing view.

```VBScript
Dim MyParentView As DrawingView
Set MyParentView = MyView.GenerativeBehavior.ParentView

```

### Property **PointsProjectionMode**( ) As [CatPointsProjectionMode](../DraftingInterfaces/enum_CatPointsProjectionMode_111523.md)

Returns or sets projection mode for 3D points. This mode indicates whether to project 3D points.

**Example:**      This example sets the points projection mode of the `MyView` drawing view to `catPointsProjectionModeOn` to indicate that 3D points must be projected.

```VBScript
MyView.GenerativeBehavior.PointsProjectionMode = catPointsProjectionModeOn

```

### Property **PointsSymbol**( ) As short

Returns or sets symbol for projected points. The 0 value means that projected points inherit the symbol of 3D points they come from.  
### Property **RepresentationMode**( ) As [CatRepresentationMode](../DraftingInterfaces/enum_CatRepresentationMode_93538.md)

Returns or sets generated geometry representation mode.

**Returns:**      `S_OK`     if the operation succeeded. `E_FAIL`     For both methods, if an unspecified failure has occurred and for the put_RepresentationMode method if the drawing view owns a detail, section or breakout specification.  **Example:**      This example sets the representation mode of the `MyView` drawing view to `catPolyhedricMode` to indicate that it is generated from CGR data.

```VBScript
MyView.GenerativeBehavior.RepresentationMode = catPolyhedricMode

```

Methods

### Sub **ApplyBreakoutTo**( [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md)  `iParentView`)

If a view have gone through a breakout view operation, this method realize a breakout view on the view given as parameter, and the other types of the view remain.

**Example:**      This example apply the last breakout view done on `MyView`, if so, on the view `MyDestinationView`.

```VBScript
MyView.GenerativeBehavior.ApplyBreakoutTo(MyDestinationView)

```

### Sub **DefineAuxiliaryView**( double  `iXStartPoint`,  double  `iYStartPoint`,  double  `iXEndPoint`,  double  `YEndPoint`,  short  `iSideToDraw`,  [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md)  `iParentViewGenerativeBehavior`)

Defines an auxiliary drawing view. The projection plane of this auxiliary drawing view is defined in its parent view using a line segment which represents the trace of the projection plane, considered as being normal to this parent view projection plane.

**Parameters:**

` iXStartPoint,iYStartPoint`      The coordinates of the trace line segment start point, expressed with respect of the parent view axis system
` iXEndPoint,iYEndPoint`      The coordinates of the trace line segment end point, expressed with respect of the parent view axis system
` iSideToDraw`      This side is defined according to the trace line segment. This segment is oriented from its start point to its end point. When looking along this segment, from its start point towards its end point, setting `iSideToDraw` to 0 (clockwise) draws the auxiliary view as if it were seen from the left of the segment in the parent view. Setting `iSideToDraw` to 1 (counterclockwise) draws the auxiliary view as if it were seen from the right of the segment.
0 Clockwise
1 Counterclockwise
` iParentViewGenerativeBehavior`      The generative behavior of the parent view in which the line segment representing the projection plane trace is defined
**Example:**      This example defines `MyView` as an auxiliary view of its parent view whose generative behavior is `MyParentViewGB`. The trace of the auxiliary view projection plane passes by the points of coordinates (100., 50.) and (500., 250.) respectively. The section is seen from the right of the trace line segment defining the auxiliary view projection plane.

```VBScript
MyView.GenerativeBehavior.DefineAuxiliaryView 100., 50., 500., 250., 1, MyParentViewGB

```

### Sub **DefineBox3DView**( [CATIABase](../System/interface_AnyObject_17321.md)  `iBoxableObject`)

Defines a drawing view intersected with a 3D box. The 3D box is defined by the interface CATISiSectionPlane

**Parameters:**

` iBoxableObject`      The 3D box object which must implement the CATISiSectionPlane interface

### Sub **DefineBreakout**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProfil`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPlane1`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPlane2`)

Defines a breakout on the current view.

**Parameters:**

` Profil`      the profile used, stored as a CATSafeArrayVariant of 2D coordinates, of dimension 2*n, n the number of control points on profile.
` Plane1`      the first reference plane, stored as a CATSafeArrayVariant [9] : Plane1 [0...2] : Plane origine coordinates Plane1 [3...5] : First direction vector coordinates Plane1 [6...8] : Second direction vector coordinates. This plane must intersect the 3D Volume.
` Plane2`      the second reference plane, stored as a CATSafeArrayVariant [9] : This plane2 is not used. Returns
**Legal values** : `S_OK` if breakout definition succeeded or `E_FAIL` if the breakout definition failed

### Sub **DefineBrokenView**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iBrokenLinesExtremities`,  double  `iXDirection`,  double  `iYDirection`)

Defines a broken drawing view. The broken area is represented by two lines and a direction in the source view.

**Parameters:**

` iBrokenLinesExtremities`      The lines defining the broken profile. This lines is passed as its point coordinate table. Only two lines have to be defined. It has the following contents:

`iBrokenLinesExtremities[0] = X1`     x coordinate of the first point for the first line `iBrokenLinesExtremities[1] = Y1`     y coordinate of the first point for the first line `iBrokenLinesExtremities[2] = X2`     x coordinate of the second point for the first line `iBrokenLinesExtremities[3] = Y2`     y coordinate of the second point for the first line `iBrokenLinesExtremities[4] = X3`     x coordinate of the first point for the second line `iBrokenLinesExtremities[5] = Y3`     y coordinate of the first point for the second line `iBrokenLinesExtremities[6] = X4`     x coordinate of the second point for the second line `iBrokenLinesExtremities[7] = Y4`     y coordinate of the second point for the second line
` iXDirection,iYDirection`      The direction stands for the translation. The direction must be horizontal or vertical.
**Example:**      This example defines `MyView` as a broken view. The direction for the translation is horizontal. The broken area is defined by to vertical lines.

```VBScript
MyView.GenerativeBehavior.DefineBrokenView X1, Y1, X2, Y2, X3, Y3, X4, Y4, XDirection, YDirection

```

### Sub **DefineCircularClippingView**( double  `XCenter`,  double  `YCenter`,  double  `Radius`)

Defines a Circular clipping on the current view.

**Parameters:**

` XCenter,`      YCenter clipping circle center position.
` Radius`      clipping circle radius. Returns
**Legal values** : `S_OK` if clipping definition succeeded or `E_FAIL` if the clipping definition failed

### Sub **DefineCircularDetailView**( double  `iXCenter`,  double  `iYCenter`,  double  `iRadius`,  [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md)  `iParentViewGenerativeBehavior`)

Defines a detail or a clipped drawing view. The clipped area is represented by a circle in the parent view.

**Parameters:**

` iXCenter,iYCenter`      The circle center coordinates, expressed in the parent view axis system
` iRadius`      The circle radius
` iParentViewGenerativeBehavior`      The generative behavior of the parent view in which the circular clipping is defined. For a clipped view, `iParentViewGenerativeBehavior` must be set to the current drawing view.
**Example:**      This example defines `MyView` as a detail view of the view considered as its parent view whose generative behavior is `MyParentViewGB`. The clipped area is a circle defined using its center coordinates (100., 150.), and its radius (75.) with respsect to the parent view axis system.

```VBScript
MyView.GenerativeBehavior.DefineCircularDetailView 100., 150., 75., MyParentViewGB

```

### Sub **DefineCircularExactClippingView**( double  `XCenter`,  double  `YCenter`,  double  `Radius`)

Defines a Circular exact clipping on the current view.

**Parameters:**

` XCenter,`      YCenter clipping circle center position.
` Radius`      clipping circle radius. Returns
**Legal values** : `S_OK` if clipping definition succeeded or `E_FAIL` if the clipping definition failed

### Sub **DefineFrontView**( double  `iX1`,  double  `iY1`,  double  `iZ1`,  double  `iX2`,  double  `iY2`,  double  `iZ2`)

Defines a front drawing view. The front view is defined using its projection plane, passed as the components of two vectors V1 and V2. The cross product of vector V1(`X1`, `Y1`, `Z1`) by vector V2(`X2`, `Y2`, `Z2`) defines the projection direction.

**Parameters:**

` iX1,iY1,iZ1`      The components of the first vector with respect to the document 3D axis system
` iX2,iY2,iZ2`      The components of the second vector with respect to the document 3D axis system
**Example:**      This example defines `MyView` as a front view by projecting the represented document in the YZ 3D plane.

```VBScript
MyView.GenerativeBehavior.DefineFrontView 0., 1., 0., 0., 0., 1.

```

### Sub **DefineIsometricView**( double  `iX1`,  double  `iY1`,  double  `iZ1`,  double  `iX2`,  double  `iY2`,  double  `iZ2`)

Defines an isometric drawing view. The isometric view is defined using its projection plane, passed as the components of two vectors V1 and V2. The cross product of vector V1(`X1`, `Y1`, `Z1`) by vector V2(`X2`, `Y2`, `Z2`) defines the projection direction.

**Parameters:**

` iX1,iY1,iZ1`      The components of the first vector with respect to the document 3D axis system
` iX2,iY2,iZ2`      The components of the second vector with respect to the document 3D axis system
**Example:**      This example defines `MyView` as an isometric view by projecting the represented document in the vertical plane making an angle of -45 degrees with respect to the X axis.

```VBScript
MyView.GenerativeBehavior.DefineIsometricView -0.707, 0.707, 0., 0., 0., 1.

```

### Sub **DefinePolygonalClippingView**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `profil`)

Defines a polygonal clipping on the current view.

**Parameters:**

` profil`      the profile used, stored as a CATSafeArrayVariant of 2D coordinates, of dimension 2*n, n the number of control points on profile. Returns
**Legal values** : `S_OK` if clipping definition succeeded or `E_FAIL` if the clipping definition failed

### Sub **DefinePolygonalDetailView**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProfile`,  [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md)  `iParentViewGenerativeBehavior`)

Defines a detail or a clipped drawing view. The clipped area is represented by a circle in the parent view.

**Parameters:**

` iProfile`      The polyline defining the detail profile. This polyline is passed as its point coordinate table. The polyline is automatically closed. It has the following contents:

`iProfile[0] = X1`     x coordinate of the first point `iProfile[1] = Y1`     y coordinate of the first point `iProfile[2] = X2`     x coordinate of the second point `iProfile[3] = Y2`     y coordinate of the second point `...` `iProfile[2n-2] = Xn`     x coordinate of the nth and last point `iProfile[2n-1] = Yn`     y coordinate of the nth and last point
` iParentViewGenerativeBehavior`      The generative behavior of the parent view in which the poligonal clipping is defined. For a clipped view, `iParentViewGenerativeBehavior` must be set to the current drawing view.
**Example:**      This example defines `MyView` as a detail view of the view considered as its parent view whose generative behavior is `MyParentViewGB`. The clipped area is a square defined using its four corners with respsect to the parent view axis system.

```VBScript
MyView.GenerativeBehavior.DefinePolygonalDetailView 0., 0., 100., 0., 100., 100., 0., 100., MyParentViewGB

```

### Sub **DefinePolygonalExactClippingView**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `profil`)

Defines a polygonal exact clipping on the current view.

**Parameters:**

` profil`      the profile used, stored as a CATSafeArrayVariant of 2D coordinates, of dimension 2*n, n the number of control points on profile. Returns
**Legal values** : `S_OK` if clipping definition succeeded or `E_FAIL` if the clipping definition failed

### Sub **DefineProjectionView**( [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md)  `iParentViewGenerativeBehavior`,  [CatProjViewType](../DraftingInterfaces/enum_CatProjViewType_47846.md)  `iType`)

Defines a projection drawing view.

**Parameters:**

` iParentViewGenerativeBehavior`      The generative behavior of the parent view.
` iType`      The type of the drawing view with respect to its parent view
**Example:**      This example defines `MyView` as a right view of the front view considered as its parent view whose generative behavior is `MyParentViewGB`.

```VBScript
MyView.GenerativeBehavior.DefineProjectionView MyParentViewGB, catRightView

```

### Sub **DefineSectionView**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProfile`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSectionType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProfileType`,  short  `iSideToDraw`,  [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md)  `iParentViewGenerativeBehavior`)

Defines a section drawing view. A section drawing view is defined using a section profile defined itself as a polyline, a section type to indicate whether to draw the section or only the section cut, a section profile type that can be offset or aligned, the side of the section to draw, and the generative behavior of the parent view.

**Parameters:**

` iProfile`      The polyline defining the section profile. This polyline is passed as its point coordinate table. It has the following contents:

`iProfile[0] = X1`     x coordinate of the first point `iProfile[1] = Y1`     y coordinate of the first point `iProfile[2] = X2`     x coordinate of the second point `iProfile[3] = Y2`     y coordinate of the second point `...` `iProfile[2n-2] = Xn`     x coordinate of the nth and last point `iProfile[2n-1] = Yn`     y coordinate of the nth and last point
` iSectionType`      The section type: `SectionCut` or `SectionView`
` iProfileType`      The cutting profile type: `Offset` or `Aligned`
` iSideToDraw`      The side of the section to draw. This side is defined according to the first segment of the section profile. This segment is oriented from its start point to its end point. When looking along this segment, from its start point towards its end point, setting `iSideToDraw` to 0 (clockwise) draws the section seen from the left of the segment. Setting `iSideToDraw` to 1 (counterclockwise)draws the section seen from the right of the segment.
0 Clockwise
1 Counterclockwise
` iParentViewGenerativeBehavior`      The generative behavior of the parent view. The section profile is defined with respect to this parent view axis system
**Example:**      This example defines `MyView` as an offset section view of the view considered as its parent view whose generative behavior is `MyParentViewGB`. The section is seen from the left of the first section profile segment. The section profile is defined in the `SectionProfile` array.

```VBScript
Dim SectionProfile
ReDim SectionProfile(7)
SectionProfile(0) = 10.
SectionProfile(1) = 200.
SectionProfile(2) = 100.
SectionProfile(3) = 200.
SectionProfile(4) = 100.
SectionProfile(5) = 50.
SectionProfile(6) = 300.
SectionProfile(7) = 50.
MyView.GenerativeBehavior.DefineSectionView SectionProfile, SectionView, Offset, 0, MyParentViewGB

```

### Sub **DefineStandAloneSection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `profil`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `type_of_section`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `type_of_profile`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPlane`,  short  `iSide`)

Defines a section view without a reference view.

**Parameters:**

` profil`      the profile used, stored as a CATSafeArrayVariant of 2D coordinates, of dimension 2*n, n the number of control points on profile.
` type_of_section`
**Legal values** : ` SectionCut ` ` SectionView `
` type_of_profile`
**Legal values** : ` Aligned ` ` Offset `
` iPlane`      the reference plane, on which the profile lies Plane1 [0...2] : Plane origine coordinates Plane1 [3...5] : First direction vector coordinates Plane1 [6...8] : Second direction vector coordinates.
` iSide`
**Legal values** : ` 1 ` ` -1 `
**Returns:**      `S_OK`     if the section was correctly defined `E_FAIL`     if the operation failed.  **Example:**      // 3 points profile Dim arrayOfVariantOfDouble1(5) arrayOfVariantOfDouble1(0) = -30.000000 arrayOfVariantOfDouble1(1) = -150.000000 arrayOfVariantOfDouble1(2) = -30.000000 arrayOfVariantOfDouble1(3) = -50.000000 arrayOfVariantOfDouble1(4) = 21.997045 arrayOfVariantOfDouble1(5) = -50.000000 // XY plane Dim arrayOfVariantOfDouble2(8) arrayOfVariantOfDouble2(0) = 0.000000 arrayOfVariantOfDouble2(1) = 0.000000 arrayOfVariantOfDouble2(2) = 0.000000 arrayOfVariantOfDouble2(3) = 1.000000 arrayOfVariantOfDouble2(4) = 0.000000 arrayOfVariantOfDouble2(5) = 0.000000 arrayOfVariantOfDouble2(6) = 0.000000 arrayOfVariantOfDouble2(7) = 1.000000 arrayOfVariantOfDouble2(8) = 0.000000 // defines offset sectionview drawingViewGenerativeBehavior1.DefineStandAloneSection arrayOfVariantOfDouble1, "SectionView", "Offset", arrayOfVariantOfDouble2, 1  
### Sub **DefineTPSSectionView**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProfile`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSectionType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProfileType`,  short  `iSideToDraw`,  [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md)  `iParentViewGenerativeBehavior`)

Defines a TPS section drawing view. A section TPS drawing view is defined using a section profile defined itself as a polyline, a section type to indicate whether to draw the section or only the section cut, a section profile type that can be offset or aligned, the side of the section to draw, and the generative behavior of the parent view.

**Parameters:**

` iProfile`      The polyline defining the section profile. This polyline is passed as its point coordinate table. It has the following contents:

`iProfile[0] = X1`     x coordinate of the first point `iProfile[1] = Y1`     y coordinate of the first point `iProfile[2] = X2`     x coordinate of the second point `iProfile[3] = Y2`     y coordinate of the second point `...` `iProfile[2n-2] = Xn`     x coordinate of the nth and last point `iProfile[2n-1] = Yn`     y coordinate of the nth and last point
` iSectionType`      The section type: `SectionCut` or `SectionView`
` iProfileType`      The cutting profile type: `Offset` or `Aligned`
` iSideToDraw`      The side of the section to draw. This side is defined according to the first segment of the section profile. This segment is oriented from its start point to its end point. When looking along this segment, from its start point towards its end point, setting `iSideToDraw` to 0 (clockwise) draws the section seen from the left of the segment. Setting `iSideToDraw` to 1 (counterclockwise)draws the section seen from the right of the segment.
0 Clockwise
1 Counterclockwise
` iParentViewGenerativeBehavior`      The generative behavior of the parent view. The section profile is defined with respect to this parent view axis system
**Example:**      This example defines `MyView` as an offset section view of the view considered as its parent view whose generative behavior is `MyParentViewGB`. The section is seen from the left of the first section profile segment. The section profile is defined in the `SectionProfile` array.

```VBScript
Dim SectionProfile
ReDim SectionProfile(7)
SectionProfile(0) = 10.
SectionProfile(1) = 200.
SectionProfile(2) = 100.
SectionProfile(3) = 200.
SectionProfile(4) = 100.
SectionProfile(5) = 50.
SectionProfile(6) = 300.
SectionProfile(7) = 50.
MyView.GenerativeBehavior.DefineSectionView SectionProfile, SectionView, Offset, 0, MyParentViewGB

```

### Sub **DefineUnfoldedView**( double  `iX1`,  double  `iY1`,  double  `iZ1`,  double  `iX2`,  double  `iY2`,  double  `iZ2`)

Defines a unfolded drawing view. The unfolded view is defined using its projection plane, passed as the components of two vectors V1 and V2. The cross product of vector V1(`X1`, `Y1`, `Z1`) by vector V2(`X2`, `Y2`, `Z2`) defines the projection direction.

**Parameters:**

` iX1,iY1,iZ1`      The components of the first vector with respect to the document 3D axis system
` iX2,iY2,iZ2`      The components of the second vector with respect to the document 3D axis system
**Example:**      This example defines `MyView` as a unfolded view by projecting the represented document in the YZ 3D plane.

```VBScript
MyView.GenerativeBehavior.DefineUnfoldedView 0., 1., 0., 0., 0., 1.

```

### Sub **ForceUpdate**( )

Forces the Update the drawing view even if not necessary.

**Example:**      This example updates the `MyView` drawing view.

```VBScript
MyView.GenerativeBehavior.ForceUpdate()

### Sub **GetAxisSysteme**( [CATIABase](../System/interface_AnyObject_17321.md)  oProduct,  [CATIABase](../System/interface_AnyObject_17321.md)  oAxisSysteme)

Retrieves the axis systeme associated with the view.

  **Parameters:**

    oProduct
      		The reference product stored as a CATIABase.

    oAxisSysteme
      		The axis system stored as a CATIABase.

### Func **GetGPSName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves the set of generative parameters currently applied to the view.
    	Parameters will be taken into account at view update time.

  **Parameters:**

    ioGPSName
      		The XML file where generative parameters are retrieved from

  **Returns:**
       S_OK     if the operation succeeded.
E_FAIL

  **Example:**
       This example retrieves the generative parameters file applied to the MyView drawing view as GPSFile.

```VBScript
MyView.GenerativeBehavior.GetGPSName GPSFile

```

### Sub **GetProjectionPlane**( double  `oX1`,  double  `oY1`,  double  `oZ1`,  double  `oX2`,  double  `oY2`,  double  `oZ2`)

Returns the drawing view projection plane.

**Parameters:**

` oX1,oY1,oZ1`      The components of the first vector with respect to the document 3D axis system
` oX2,oY2,oZ2`      The components of the second vector with respect to the document 3D axis system
**Example:**      This example retrieves the projection plane of the `MyView` drawing view as two sets of components, X1, Y1, and Z1 for the first vector, X2, Y2, and Z2 for the second vector.

```VBScript
MyView.GenerativeBehavior.GetProjectionPlane X1, Y1, Z1, X2, Y2, Z2

```

### Sub **GetProjectionPlaneNormal**( double  `oXNormal`,  double  `oYNormal`,  double  `oZNormal`)

Returns the normal vector of the drawing view projection plane. This represents the direction of projection.

**Parameters:**

` oXNormal,oYNormal,oZNormal`      The components of the projection plane normal vector with respect to the document 3D axis system
**Example:**      This example retrieves the projection plane normal vector of the `MyView` drawing view as three components Xn, Yn, and Zn.

```VBScript
MyView.GenerativeBehavior.GetProjectionPlaneNormal Xn, Yn, Zn

```

### Sub **SetAxisSysteme**( [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iAxisSysteme`)

Defines an axis systeme in the view.

**Parameters:**

` iProduct`      The reference product stored as a CATIABase.
` iAxisSysteme`      The axis system stored as a CATIABase.

### Sub **SetGPSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGPSName`)

Applies a set of generative parameters to the current view. Parameters will be taken into account at view update time.

**Parameters:**

` iGPSName`      The XML file where generative parameters are retrieved from
**Returns:**      `S_OK`     if the operation succeeded. `E_FAIL`      **Example:**      This example applied the GPSFile1 to the `MyView` drawing view.

```VBScript
MyView.GenerativeBehavior.SetGPSName "GPSFile1.xml"

```

### Sub **SetProjectionPlane**( double  `iX1`,  double  `iY1`,  double  `iZ1`,  double  `iX2`,  double  `iY2`,  double  `iZ2`)

Sets the drawing view projection plane. The projection plane is the plane to which the document's geometrical objects are projected and is used as the drawing view plane. This plane is defined in the document 3D space using the components of two of its vectors. The cross product of vector V1(`X1`, `Y1`, `Z1`) by vector V2(`X2`, `Y2`, `Z2`) defines the projection direction. This method can be used with front views and isometric views to change the projection plane defined when such views were created. It should not be used with the other types of views, since their projection planes are defined with respect to their parent view projection plane.

**Parameters:**

` iX1,iY1,iZ1`      The components of the first vector with respect to the document 3D axis system
` iX2,iY2,iZ2`      The components of the second vector with respect to the document 3D axis system
**Example:**      This example sets the projection plane of the `MyView` drawing view to the XY plane, that is the plane defined with the vectors (1., 0., 0.) and (0., 1., 0.).

```VBScript
MyView.GenerativeBehavior.SetProjectionPlane 1., 0., 0., 0., 1., 0.

```

### Sub **UnBreak**( )

If a view have been broken with lines in order to hide an area of this view, this method undoes this modification of the view, and the other types of view remain.

**Example:**      This example removes the BrokenView type from `MyView` if so.

```VBScript
MyView.GenerativeBehavior.UnBreak()

```

### Sub **UnBreakout**( )

If a view have gone through a breakout view operation, this method removes all the breakout view done on this view, and the other types of view remain.

**Example:**      This example removes all the breakouts view done on `MyView` if so.

```VBScript
MyView.GenerativeBehavior.UnBreakout()

```

### Sub **UnBreakoutNum**( short  `iBreakoutNumber`)

If a view have gone through a breakout view operation, this method removes the specified breakout view done on this view, and the other types of view remain.

**Parameters:**

` iBreakoutNumber`      The reference number of the breakout view to be removed (1 to n)
**Example:**      This example removes the first breakout view done on `MyView` if so.

```VBScript
MyView.GenerativeBehavior.UnBreakout(1)

```

### Sub **UnClip**( )

If a view have been clipped, this method removes the last clipping view done on this view, and the other types of view remain.

**Example:**      This example removes the last clipping view done on `MyView` if so.

```VBScript
MyView.GenerativeBehavior.UnClip()

```

### Sub **Update**( )

Updates the drawing view. This update is performed with respect to any modification of its [DrawingView.GenerativeBehavior](../DraftingInterfaces/interface_DrawingView_26239.htm#GenerativeBehavior) property.

**Example:**      This example updates the `MyView` drawing view.

```VBScript
MyView.GenerativeBehavior.Update()