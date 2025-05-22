# CATSelectionFilter (Enumeration)

**_Values to use as selection filter._**
**Role** : Values which can be given as filter to [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2), [Selection.SelectElement3](../InfInterfaces/interface_Selection_18040.htm#SelectElement3), [Selection.IndicateOrSelectElement2D](../InfInterfaces/interface_Selection_18040.htm#IndicateOrSelectElement2D) or [Selection.IndicateOrSelectElement3D](../InfInterfaces/interface_Selection_18040.htm#IndicateOrSelectElement3D), beside the automation object names.

**Values:**

` ZeroDim`      Topological 0-D entity (such as a
[Point2D](../SketcherInterfaces/interface_Point2D_9306.md) ) ` MonoDim`      Topological 1-D entity which cannot be infinite (such as a
[HybridShapeSpline](../GSMInterfaces/interface_HybridShapeSpline_60786.md) ) ` MonoDimInfinite`      Topological 1-D entity which may be infinite, such as a
[HybridShapeSpline](../GSMInterfaces/interface_HybridShapeSpline_60786.md) (not infinite) or a [HybridShapeLinePtDir](../GSMInterfaces/interface_HybridShapeLinePtDir_81218.md) for which a call to [HybridShapeLinePtDir.GetLengthType](../GSMInterfaces/interface_HybridShapeLinePtDir_81218.htm#GetLengthType) would give 1, 2 or 3 (infinite) ` RectilinearMonoDim`      1-D entity which cannot be infinite, the entity having a rectilinear geometry
` RectilinearMonoDimInfinite`      1-D entity which may be infinite, the entity having a rectilinear geometry
` BiDim`      Topological 2-D entity which cannot be infinite (such as a
[HybridShapeCylinder](../GSMInterfaces/interface_HybridShapeCylinder_75955.md) ) ` BiDimInfinite`      Topological 2-D entity which may be infinite, such as a
[HybridShapeCylinder](../GSMInterfaces/interface_HybridShapeCylinder_75955.md) (non infinite) or a [HybridShapePlaneOffsetPt](../GSMInterfaces/interface_HybridShapePlaneOffsetPt_118752.md) (infinite) ` PlanarBiDim`      2-D entity which cannot be infinite, the entity having a planar geometry
` PlanarBiDimInfinite`      2-D entity having a planar geometry
` CylindricalBiDim`      2-D entity which cannot be infinite, the entity having a cylindrical geometry
` TriDim`      Topological 3-D entity (such as a
[Pad](../PartInterfaces/interface_Pad_1979.md) )