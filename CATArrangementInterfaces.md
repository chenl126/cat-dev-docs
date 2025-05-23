# CATArrangementInterfaces Framework

## Object Index

  * [ArrBOMReport](CATArrangementInterfaces/interface_ArrBOMReport_29616.md)
  * [ArrBendableString](CATArrangementInterfaces/interface_ArrBendableString_60583.md)
  * [ArrNomenclature](CATArrangementInterfaces/interface_ArrNomenclature_48920.md)
  * [ArrNomenclatureTree](CATArrangementInterfaces/interface_ArrNomenclatureTree_76774.md)
  * [ArrNomenclatures](CATArrangementInterfaces/interface_ArrNomenclatures_55994.md)
  * [ArrSystemLineProduct](CATArrangementInterfaces/interface_ArrSystemLineProduct_85388.md)
  * [ArrWorkbench](CATArrangementInterfaces/interface_ArrWorkbench_30890.md)
  * [ArrangementArea](CATArrangementInterfaces/interface_ArrangementArea_47127.md)
  * [ArrangementAreas](CATArrangementInterfaces/interface_ArrangementAreas_54164.md)
  * [ArrangementBoundaries](CATArrangementInterfaces/interface_ArrangementBoundaries_94314.md)
  * [ArrangementBoundary](CATArrangementInterfaces/interface_ArrangementBoundary_77900.md)
  * [ArrangementContour](CATArrangementInterfaces/interface_ArrangementContour_70746.md)
  * [ArrangementContours](CATArrangementInterfaces/interface_ArrangementContours_79187.md)
  * [ArrangementItemReservation](CATArrangementInterfaces/interface_ArrangementItemReservation_144876.md)
  * [ArrangementItemReservations](CATArrangementInterfaces/interface_ArrangementItemReservations_156900.md)
  * [ArrangementNode](CATArrangementInterfaces/interface_ArrangementNode_47648.md)
  * [ArrangementNodes](CATArrangementInterfaces/interface_ArrangementNodes_54698.md)
  * [ArrangementPathway](CATArrangementInterfaces/interface_ArrangementPathway_70114.md)
  * [ArrangementPathways](CATArrangementInterfaces/interface_ArrangementPathways_78543.md)
  * [ArrangementProduct](CATArrangementInterfaces/interface_ArrangementProduct_70174.md)
  * [ArrangementRectangle](CATArrangementInterfaces/interface_ArrangementRectangle_84792.md)
  * [ArrangementRectangles](CATArrangementInterfaces/interface_ArrangementRectangles_94094.md)
  * [ArrangementRun](CATArrangementInterfaces/interface_ArrangementRun_42486.md)
  * [ArrangementRuns](CATArrangementInterfaces/interface_ArrangementRuns_49110.md)

## Enumerated Types Index

  * [CATArrangementAreaVisuMode](CATArrangementInterfaces/enum_CATArrangementAreaVisuMode_137110.md)
  * [CATArrangementItemResVisuMode](CATArrangementInterfaces/enum_CATArrangementItemResVisuMode_171619.md)
  * [CATArrangementRouteSection](CATArrangementInterfaces/enum_CATArrangementRouteSection_141224.md)
  * [CATArrangementRouteVisuMode](CATArrangementInterfaces/enum_CATArrangementRouteVisuMode_150809.md)

---

# CATArrangementAreaVisuMode (Enumeration)

**_ArrangementAreaVisuMode Styles._**

**Role:** The styles defined here can be used to provide the appropriate Visual Mode to the ArrangementArea.

**Values:**

` CatArrangementAreaVisuModeFlat`      The Area is flattened on its base plane (the height is not shown).
` CatArrangementAreaVisuModeSolid`      The Area is shown as a Solid with its height shown.

---

# CATArrangementItemResVisuMode (Enumeration)

**_Visualization mode for Item Reservation._**

**Values:**

` CatArrangementItemReservationVisuModeVisuAxis`      The Item Reservation is visualized as an axis (no extents are shown).
` CatArrangementItemReservationVisuModeVisuFlat`      The Item Reservation is visualized as a flattened box.
` CatArrangementItemReservationVisuModeItem`      Reservation The Item Reservation is visualized as solid box.

---

# CATArrangementRouteSection (Enumeration)

**_Section Types for ArrangementRun, ArrangementPathway and ArrangementBoundary objects._**

**See also:**      [ArrangementRun](../CATArrangementInterfaces/interface_ArrangementRun_42486.md), [ArrangementPathway](../CATArrangementInterfaces/interface_ArrangementPathway_70114.md), [ArrangementBoundary](../CATArrangementInterfaces/interface_ArrangementBoundary_77900.md) **Values:**

` CatArrangementRouteSectionNone`      There is no section shape (it is considered a point).
` CatArrangementRouteSectionRectangular`      The section is rectangular.
` CatArrangementRouteSectionRound`      The section is round (circular). **Note:** This mode is used only on ArrangementRun, ArrangementPathway objects.
` CatArrangementRouteSectionFlatOval`      The section is flat oval (rectangular in the middle half circle at sides). **Note:** This mode is used only on ArrangementRun, ArrangementPathway objects.
` CatArrangementRouteSectionRadiusCorner`      The section is rectangular with cornered radius. **Note:** This mode is used only on ArrangementRun, ArrangementPathway objects.
` CatArrangementRouteSectionDoubleRidge`      The section is rectangular with cornered radius. **Note:** This mode is used only on ArrangementRun, ArrangementPathway objects.

---

# CATArrangementRouteVisuMode (Enumeration)

**_The visualization mode for the ArrangementRun, ArrangementPathway, ArrangementBoundary objects._**

**See also:**      [ArrangementRun](../CATArrangementInterfaces/interface_ArrangementRun_42486.md), [ArrangementPathway](../CATArrangementInterfaces/interface_ArrangementPathway_70114.md), [ArrangementBoundary](../CATArrangementInterfaces/interface_ArrangementBoundary_77900.md) **Values:**

` CatArrangementRouteVisuModeCurve`      The routing object is visualized as a curve (wire).
` CatArrangementRouteVisuModeFlat`      The routing object is visualized as flat on the orientation plane.
` CatArrangementRouteVisuModeSolid`      The routing object is visualized as a solid.

---

# ArrangementArea (Object)

**_Use this object to access an ArrangementArea object's properties and functions._**

**Role:** The ArrangementArea object is a type of Arrangement Object defining an area containing other objects.

## Properties

### Property **ArrangementContours**( ) As [CATIAArrangementContours](../CATArrangementInterfaces/interface_ArrangementContours_79187.md) (Read Only)

   Returns the ArrangementContours collection object associated with an ArrangementArea object.

**Example:**      This example retrieves the ArrangementContours collection object for the `objArea1` object.

```VBScript
     Dim objArrContours   As ArrangementContours
     Set objArrContours  = objArea1.ArrangementContours

```

### Property **Height**( ) As double

   Returns or sets the Height of an ArrangementArea object.

**Example:**      This example retrieves the Height for the `objArea1` object.

```VBScript
     Dim dblAreaHeight   As Double
     dblAreaHeight  = objArea1.Height

```

### Property **Size**( ) As double (Read Only)

   Returns the Size of the ArrangementArea.

**Example:**      This example retrieves the Size of the `objArea1` object.

```VBScript
     Dim dblAreaSize   As Double
     dblAreaSize  = objArea1.Size

```

### Property **VisuMode**( ) As [CATArrangementAreaVisuMode](../CATArrangementInterfaces/enum_CATArrangementAreaVisuMode_137110.md)

   Returns or sets the Visualization Mode for an ArrangementArea object.

**Example:**      This example sets the Visualization Mode for the `objArea1` object to `CatArrangementAreaVisuModeVolume`.

```VBScript
     objArea1.VisuMode = CatArrangementAreaVisuModeVolume

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the applicative data whose type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.

**Returns:**      oApplicativeObj The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objArea1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objArea1.GetTechnologicalObject("Product")

```

---

# ArrangementAreas (Collection)

**_A Collection object for ArrangementArea objects._**

**Role:** Use this interface to add, retrieve and remove ArrangementArea objects from this collection.

## Methods

### Func **AddArea**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`,  double  `iHeight`) As [CATIAArrangementArea](../CATArrangementInterfaces/interface_ArrangementArea_47127.md)

   Creates a ArrangementArea and adds it to the collection. The Area created will be without any contour. Hence only the height of the area is specified.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iPosition`      Position information for the Area (rotation and location).
` iHeight`      Height of the Area.

**Returns:**      The newly created ArrangementArea object that is also added to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementArea](../CATArrangementInterfaces/interface_ArrangementArea_47127.md)

   Returns the specified item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementArea to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementArea in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementArea by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementArea object.

**Example:**      This example retrieves ArrangementArea, `objArea1`, of rank 1 under the ` Areas ` collection.

```VBScript
     Dim objArea1 As ArrangementArea
     Set objArea1= Areas.Item(1)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementArea object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementArea to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementArea in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementArea by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

**Example:**      This example removes ArrangementArea of rank 1 under the ` Areas ` collection.

```VBScript
     Areas.Remove(1)

```

---

# ArrangementBoundaries (Collection)

**_A collection object for ArrangementBoundary objects._**

**Role:** This collection object is used to manage (create, retrieve and remove )ArrangementBoundary objects.

## Methods

### Func **AddBoundary**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListofMathPoints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iMathDirection`) As [CATIAArrangementBoundary](../CATArrangementInterfaces/interface_ArrangementBoundary_77900.md)

   Creates an ArrangementBoundary and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iListofMathPoints`      List of points through which to route.
` iMathDirection`      Starting routing direction.

**Returns:**      The newly created ArrangementBoundary object.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementBoundary](../CATArrangementInterfaces/interface_ArrangementBoundary_77900.md)

   Returns the specified ArrangementBoundary item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementBoundary to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementBoundary in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementBoundary by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementBoundary object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementBoundary object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementBoundary to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementBoundary in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementBoundary by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# ArrangementBoundary (Object)

**_Access properties and functions of an ArrangementBoundary object._**

**Role:** Use this interface to control the visualization mode, section parameters, nodes that define the ArrangementBoundary object.

## Properties

### Property **ArrangementNodes**( ) As [CATIAArrangementNodes](../CATArrangementInterfaces/interface_ArrangementNodes_54698.md) (Read Only)

   Returns the collection of ArrangementNodes that make up the ArrangementBoundary.

**Example:**      This example gets the ArrangementNodes for the `objBoundary1` object.

```VBScript
     Dim objArrNodes   As ArrangementNodes
     Set objArrNodes = objBoundary1.ArrangementNodes

```

### Property **Length**( ) As double (Read Only)

   Returns the length of the ArrangementBoundary object.

**Example:**      This example retrieves the Length of the `objBoundary1` object.

```VBScript
     Dim dblBoundaryLength   As Double
     dblBoundaryLength  = objBoundary1.Length

```

### Property **SectionHeight**( ) As double

   Returns or sets the SectionHeight for an ArrangementBoundary object.

**Example:**      This example gets the SectionHeight for the `objBoundary1` object.

```VBScript
     Dim dblSectionHeight   As Double
     dblSectionHeight = objBoundary1.SectionHeight

```

### Property **SectionType**( ) As [CATArrangementRouteSection](../CATArrangementInterfaces/enum_CATArrangementRouteSection_141224.md)

   Returns or sets the SectionType for an ArrangementBoundary object.

**Legal values** :

CatArrangementRouteSectionNone
CatArrangementRouteSectionRectangular

**Example:**      This example sets the SectionType for the `objBoundary1` object to `CatArrangementRouteSectionRectangular`.

```VBScript
     objBoundary1.SectionType = CatArrangementRouteSectionRectangular

```

### Property **SectionWidth**( ) As double

   Returns or sets the SectionWidth for an ArrangementBoundary object.

**Example:**      This example gets the SectionWidth for the `objBoundary1` object.

```VBScript
     Dim dblSectionWidth   As Double
     dblSectionWidth = objBoundary1.SectionWidth

```

### Property **VisuMode**( ) As [CATArrangementRouteVisuMode](../CATArrangementInterfaces/enum_CATArrangementRouteVisuMode_150809.md)

   Returns or sets the Visualization Mode for an ArrangementBoundary object.

**Example:**      This example sets the Visualization Mode for the `objBoundary1` object to `CatArrangementRouteVisuModeSolid`.

```VBScript
     objBoundary1.VisuMode = CatArrangementRouteVisuModeSolid

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the applicative data whose type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objBoundary1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objBoundary1.GetTechnologicalObject("Product")

```

---

# ArrangementContour (Object)

**_The ArrangementContour object._**

---

# ArrangementContours (Collection)

**_A collection object for ArrangementContours of an Area._**

**Role:** Use this to manage (create, retrieve and remove) ArrangementContours of an ArrangementArea.

## Methods

### Func **AddRectangularContour**( [CATIAArrangementRectangle](../CATArrangementInterfaces/interface_ArrangementRectangle_84792.md)  `iRectangle`) As [CATIAArrangementContour](../CATArrangementInterfaces/interface_ArrangementContour_70746.md)

   Creates a Rectangular Contour by adding a ArrangementRectangle to the collection.

**Parameters:**

` iRectangle`      ArrangementRectangle to create the contour from.

**Returns:**      Returns the newly created ArrangementContour object and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementContour](../CATArrangementInterfaces/interface_ArrangementContour_70746.md)

   Returns the specified ArrangementContour item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementContour to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementContour in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementContour by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementContour object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementContour object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementContour to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementContour in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementContour by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# ArrangementItemReservation (Object)

**_Use this object to access the ArrangementItemReservation properties and methods._**

**Role:** Use this object to control the visualization mode, dimensions of the ArrangementItemReservation.

## Properties

### Property **Height**( ) As double

   Returns or sets the height of the ArrangementItemReservation.

**Example:**      This example retrieves the Height of the `objItemRes1` object.

```VBScript
     Dim dblHeight   As Double
     dblHeight  = objItemRes1.Height

```

### Property **VisuMode**( ) As [CATArrangementItemResVisuMode](../CATArrangementInterfaces/enum_CATArrangementItemResVisuMode_171619.md)

   Returns or set the Visualization Mode for the ArrangementItemReservation.

**Example:**      This example Sets the Visualization Mode of the `objItemRes1` object to ` CatArrangementItemReservationVisuModeBox `.

```VBScript
     objItemRes1.VisuMode = CatArrangementItemReservationVisuModeBox

```

### Property **XLength**( ) As double

   Returns or sets the XLength of the ArrangementItemReservation.

**Example:**      This example retrieves the XLength of the `objItemRes1` object.

```VBScript
     Dim dblXLength   As Double
     dblXLength  = objItemRes1.XLength

```

### Property **YLength**( ) As double

   Returns or sets the YLength of the ArrangementItemReservation.

**Example:**      This example retrieves the YLength of the `objItemRes1` object.

```VBScript
     Dim dblYLength   As Double
     dblYLength  = objItemRes1.YLength

```

Methods

### Sub **GetDimension**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioItemResDimensions`)

   Returns the Dimensions of the ArrangementItemReservation.

**Parameters:**

` ioItemResDimensions`      The output array initialized with the dimensions that make up the ArrangementItemReservation. The first three components represent the Minimum XCoord, YCoord and Z Coord while the remaining three components represent the Maximum XCoord, YCoord and Z Coord respectively.

**Example:**      This example retrieves the coordinate dimensions of the `objItemRes1` object.

```VBScript
     Dim dblDimension(6)   As Double
     objItemRes1.GetDimension(dblDimension)

```

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the applicative data whose type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objItemRes1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objItemRes1.GetTechnologicalObject("Product")

```

### Sub **SetDimension**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iItemResDimensions`)

   Sets the Dimensions of the ArrangementItemReservation.

**Parameters:**

` iItemResDimensions`      The input array initialized with the dimensions that make up the ArrangementItemReservation. The first three components represent the Minimum XCoord, YCoord and Z Coord while the remaining three components represent the Maximum XCoord, YCoord and Z Coord respectively.

**Example:**      This example sets the coordinate dimensions of the `objItemRes1` object.

```VBScript
     Dim dblDimension(6)   As Double
     dblDimension(0)       = 300.0 '//XMin
     dblDimension(1)       = 500.0 '//YMin
     dblDimension(2)       = 300.0 '//ZMin
     dblDimension(3)       = 500.0 '//XMax
     dblDimension(4)       = 0.0   '//YMax
     dblDimension(5)       = 300.0 '//ZMax
     objItemRes1.SetDimension(dblDimension)

```

---

# ArrangementItemReservations (Collection)

**_A collection object for ArrangementItemReservation objects._**

**Role:** Use this collection object to manage (create, retrieve and remove) ArrangementItemReservation objects.

## Methods

### Func **AddItemReservation**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`,  double  `iXMin`,  double  `iYMin`,  double  `iZMin`,  double  `iXMax`,  double  `iYMax`,  double  `iZMax`) As [CATIAArrangementItemReservation](../CATArrangementInterfaces/interface_ArrangementItemReservation_144876.md)

   Creates an ArrangementItemReservation and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iPosition`      Position information for the ItemReservation (rotation and location).
` iXMin`      Minium X Coordinate of the bounding box on the Item Reservation.
` iYMin`      Minium Y Coordinate of the bounding box on the Item Reservation.
` iZMin`      Minium Z Coordinate of the bounding box on the Item Reservation.
` iXMax`      Maximum X Coordinate of the bounding box on the Item Reservation.
` iYMax`      Maximum Y Coordinate of the bounding box on the Item Reservation.
` iZMax`      Maximum Z Coordinate of the bounding box on the Item Reservation.

**Returns:**      Returns the newly created ArrangementItemReservation object and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementItemReservation](../CATArrangementInterfaces/interface_ArrangementItemReservation_144876.md)

   Returns the specified ArrangementItemReservation item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementItemReservation to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementItemReservation in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementItemReservation by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementItemReservation object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementItemReservation object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementItemReservation to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementItemReservation in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementItemReservation by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# ArrangementNode (Object)

**_This interface provides access to a CATIAArrangementNode object._**
Use this object to fetch the properties of an ArrangementNode object. **Role:** Use this object to retrieve the bend angle, bend radius and location of an ArrangementNode object.

## Properties

### Property **BendAngle**( ) As double (Read Only)

   Returns the BendAngle of the current ArrangementNode.

**Example:**      This example retrieves the BendAngle of the `objNode1` object.

```VBScript
     Dim dblBendAngle   As Double
     dblBendBendAngle  = objNode1.BendAngle

```

### Property **BendRadius**( ) As double

   Returns or sets the BendRadius of the current ArrangementNode.

**Example:**      This example retrieves the BendRadius of the `objNode1` object.

```VBScript
     Dim dblBendRadius   As Double
     dblBendRadius  = objNode1.BendRadius

```

Methods

### Sub **GetPoint**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioNodeLocation`)

   Returns the location of the current ArrangementNode.

**Parameters:**

` iRelAxis`      The relative axis to be considered when calculating the coordinate.
` ioNodeLocation`      The location of the ArrangementNode.

**Example:**      This example retrieves the location of the ArrangementNode object `objNode1`.

```VBScript
     Dim dblCoords(3)   As Double
     Dim iRelAxis       As Move
     'Fetch iRelAxis from the object containing the node
     ...
     objNode1.GetPoint(iRelAxis, dblCoords)

```

### Sub **SetPoint**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iNodeLocation`)

   Sets the location of the current ArrangementNode.

**Parameters:**

` iRelAxis`      The relative axis to be considered when calculating the coordinate.
` ioNodeLocation`      The location of the ArrangementNode.

**Example:**      This example sets the location of the ArrangementNode object `objNode1`.

```VBScript
     Dim dblCoords(3)   As Double
     Dim iRelAxis       As Move
     'Fetch iRelAxis from the object containing the node
     ...
     dblCoords(0)       = 300.0 '//X
     dblCoords(1)       = 500.0 '//Y
     dblCoords(2)       = 300.0 '//Z
     objNode1.SetPoint(iRelAxis, dblCoords)

```

---

# ArrangementNodes (Collection)

**_A Collection object for ArrangementNode objects._**
Use this object to access individual ArrangementNode objects of an ArrangementRun, ArrangementPathway and ArrangementBoundary.

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementNode](../CATArrangementInterfaces/interface_ArrangementNode_47648.md)

   Returns the specified ArrangementNode item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementNode to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementNode in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementNode by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementNode object.

---

# ArrangementPathway (Object)

**_Use this object to access properties and methods of an ArrangementPathway object._**

**Role:** Use this interface to control the visualization mode, section parameters, nodes that define the ArrangementPathway object.

## Properties

### Property **ArrangementNodes**( ) As [CATIAArrangementNodes](../CATArrangementInterfaces/interface_ArrangementNodes_54698.md) (Read Only)

   Returns the ArrangementNodes that make up the ArrangementPathway.

**Example:**      This example gets the ArrangementNodes for the `objPathway1` object.

```VBScript
     Dim objArrNodes   As ArrangementNodes
     Set objArrNodes = objPathway1.ArrangementNodes

```

### Property **Length**( ) As double (Read Only)

   Returns the length of the ArrangementPathway object.

**Example:**      This example retrieves the Length of the `objPathway1` object.

```VBScript
     Dim dblLength   As Double
     dblLength  = objPathway1.Length

```

### Property **SectionDiameter**( ) As double

   Returns or sets the SectionDiameter for an ArrangementPathway object.

**Example:**      This example retrieves the SectionDiameter for the `objPathway1` object.

```VBScript
     Dim dblSectionDia   As Double
     dblSectionDia = objPathway1.SectionDiameter

```

### Property **SectionHeight**( ) As double

   Returns or sets the SectionHeight for an ArrangementPathway object.

**Example:**      This example gets the SectionHeight for the `objPathway1` object.

```VBScript
     Dim dblSectionHeight   As Double
     dblSectionHeight = objPathway1.SectionHeight

```

### Property **SectionType**( ) As [CATArrangementRouteSection](../CATArrangementInterfaces/enum_CATArrangementRouteSection_141224.md)

   Returns or sets the Section for an ArrangementPathway object.

**Example:**      This example sets the SectionType for the `objPathway1` object to `CatArrangementRouteSectionRectangular`.

```VBScript
     objPathway1.SectionType = CatArrangementRouteSectionRectangular

```

### Property **SectionWidth**( ) As double

   Returns or sets the SectionWidth for an ArrangementPathway object.

**Example:**      This example gets the SectionWidth for the `objPathway1` object.

```VBScript
     Dim dblSectionWidth   As Double
     dblSectionWidth = objPathway1.SectionWidth

```

### Property **VisuMode**( ) As [CATArrangementRouteVisuMode](../CATArrangementInterfaces/enum_CATArrangementRouteVisuMode_150809.md)

   Returns or sets the Visualization Mode for an ArrangementPathway object.

**Example:**      This example sets the Visualization Mode for the `objPathway1` object to `CatArrangementRouteVisuModeSolid`.

```VBScript
     objPathway1.VisuMode = CatArrangementRouteVisuModeSolid

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objPathway1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objPathway1.GetTechnologicalObject("Product")

```

---

# ArrangementPathways (Collection)

**_A collection object for ArrangementPathway objects._**

**Role:** Use this collection object to manage (create, retrieve and remmove) ArrangementPathway objects.

## Methods

### Func **AddPathway**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListofMathPoints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iMathDirection`) As [CATIAArrangementPathway](../CATArrangementInterfaces/interface_ArrangementPathway_70114.md)

   Creates an ArrangementItemReservation and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iListofMathPoints`      List of points through which to route.
` iMathDirection`      Starting routing direction.

**Returns:**      Returns the newly created ArrangementPathway object and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementPathway](../CATArrangementInterfaces/interface_ArrangementPathway_70114.md)

   Returns the specified ArrangementPathway item of the collection object.

**Parameters:**

` iIndex`      The index or the name of the ArrangementPathway to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementPathway in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementPathway by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementPathway object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementPathway object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementPathway to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementPathway in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementPathway by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# ArrangementProduct (Object)

**_Use this object as a factory for Arrangement collection objects._**

**Role:** Use this interface to get access to the Arrangement collections (Areas, Rectangles, ItemReservations, Runs, Pathways, Boundaries) aggregated a given Product.

## Properties

### Property **ArrangementAreas**( ) As [CATIAArrangementAreas](../CATArrangementInterfaces/interface_ArrangementAreas_54164.md) (Read Only)

   Returns the collection of ArrangementAreas under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementAreas collection, `oArrAreas `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrAreas As ArrangementAreas
     Set oArrAreas = objArrProd1.Areas

```

### Property **ArrangementBoundaries**( ) As [CATIAArrangementBoundaries](../CATArrangementInterfaces/interface_ArrangementBoundaries_94314.md) (Read Only)

   Returns the collection of ArrangementBoundaries under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementBoundaries collection, `oArrBoundaries `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrBoundaries As ArrangementBoundaries
     Set oArrBoundaries = objArrProd1.oArrObjType

```

### Property **ArrangementItemReservations**( ) As [CATIAArrangementItemReservations](../CATArrangementInterfaces/interface_ArrangementItemReservations_156900.md) (Read Only)

   Returns the collection of ArrangementItemReservations under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementItemReservations collection, `oArrItemReservations `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrItemReservations As ArrangementItemReservations
     Set oArrItemReservations = objArrProd1.ItemReservations

```

### Property **ArrangementPathways**( ) As [CATIAArrangementPathways](../CATArrangementInterfaces/interface_ArrangementPathways_78543.md) (Read Only)

   Returns the collection of ArrangementPathways under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementPathways collection, `oArrPathways `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrPathways As ArrangementPathways
     Set oArrPathways = objArrProd1.Pathways

```

### Property **ArrangementRectangles**( ) As [CATIAArrangementRectangles](../CATArrangementInterfaces/interface_ArrangementRectangles_94094.md) (Read Only)

   Returns the collection of ArrangementRectangles under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementRectangles collection, `oArrRectangles `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrRectangles As ArrangementRectangles
     Set oArrRectangles = objArrProd1.Rectangles

```

### Property **ArrangementRuns**( ) As [CATIAArrangementRuns](../CATArrangementInterfaces/interface_ArrangementRuns_49110.md) (Read Only)

   Returns the collection of ArrangementRuns under the current ArrangementProduct.

**Example:**      This example retrieves the ArrangementRuns collection, `oArrRuns `, for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrRuns As ArrangementRuns
     Set oArrRuns = objArrProd1.Runs

```

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the Type of the ArrangementProduct in the form of a String.

**Example:**      This example retrieves the type information as a string for the `objArrProd1` ArrangementProduct object.

```VBScript
     Dim oArrObjType  As String
     oArrObjType  = objArrProd1.Type

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the product's applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objArrProd1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objArrProd1.GetTechnologicalObject("Product")

```

### Sub **SetArrangementNomenclature**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNomenclature`)

   Sets the nomenclature of the ArrangementProduct.

**Returns:**      An HRESULT value.

**Legal values** :

S_OK
    operation is successful
E_FAIL
    operation failed

**Example:**      This example sets the ArrangementNomenclature for `objArrProd1` ArrangementProduct object.

```VBScript
     objArrProd1.SetArrangementNomenclature = "Building"

```

### Sub **SetAutoName**( )

   Causes the name of the ArrangementProduct automatically.

**Returns:**      An HRESULT value.

**Legal values** :

S_OK
    operation is successful
E_FAIL
    operation failed

**Example:**      This example shows how the automatic naming of the `objArrProd1` ArrangementProduct object can be done.

```VBScript
     objArrProd1.SetAutoName

```

---

# ArrangementRectangle (Object)

**_Use this object to access the properties and methods of an ArrangementRectangle object._**

**Role** : The ArrangementRectangle object is a geometric shape used for defining Contours of Areas. The ArrangementRectangle is defined by width and length and its Product position (which is the min-x, min-y corner of the rectangle).

## Properties

### Property **XLength**( ) As double

   Returns or sets the XLength of the ArrangementRectangle.

**Example:**      This example retrieves the XLength for the `objRectangle1` object.

```VBScript
     Dim dblXLength  As Double
     dblXLength = objRectangle1.XLength

```

### Property **YLength**( ) As double

   Returns or sets the YLength of the ArrangementRectangle.

**Example:**      This example retrieves the YLength for the `objRectangle1` object.

```VBScript
     Dim dblYLength  As Double
     dblYLength = objRectangle1.YLength

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objRectangle1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objRectangle1.GetTechnologicalObject("Product")

```

---

# ArrangementRectangles (Collection)

**_A Collection object for ArrangementRectangle objects._**

**Role:** Use this object to manage (create, retrieve and remove) ArrangementRectangle objects.

## Methods

### Func **AddRectangle**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`,  double  `iWidth`,  double  `iLength`) As [CATIAArrangementRectangle](../CATArrangementInterfaces/interface_ArrangementRectangle_84792.md)

   Creates an ArrangementRectangle and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iPosition`      Position information for the Rectangle (rotation and location).
` iWidth`      Width of the Rectangle.
` iLength`      Length of the Rectangle.

**Returns:**      Returns the newly created ArrangementRectangle and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementRectangle](../CATArrangementInterfaces/interface_ArrangementRectangle_84792.md)

   Returns the specified ArrangementRectangle item of the collection object.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRectangle to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementRectangle in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementRectangle by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementRectangle object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementRectangle object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRectangle to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementRectangle in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementRectangle by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# ArrangementRun (Object)

**_Use this object to access the properties and methods of an ArrangementRun object._**

**Role:** Use this interface to control the visualization mode, section parameters, nodes that define the ArrangementRun object.

## Properties

### Property **ArrangementNodes**( ) As [CATIAArrangementNodes](../CATArrangementInterfaces/interface_ArrangementNodes_54698.md) (Read Only)

   Returns the ArrangementNodes that make up the ArrangementRun.

**Example:**      This example gets the ArrangementNodes for the `objRun1` object.

```VBScript
     Dim objArrNodes   As ArrangementNodes
     Set objArrNodes = objRun1.ArrangementNodes

```

### Property **Length**( ) As double (Read Only)

   Returns the length of the ArrangementRun object.

**Example:**      This example retrieves the Length of the `objRun1` object.

```VBScript
     Dim dblLength   As Double
     dblLength  = objRun1.Length

```

### Property **SectionDiameter**( ) As double

   Returns or sets the SectionDiameter for an ArrangementRun object.

**Example:**      This example retrieves the SectionDiameter for the `objRun1` object.

```VBScript
     Dim dblSectionDia   As Double
     dblSectionDia = objRun1.SectionDiameter

```

### Property **SectionHeight**( ) As double

   Returns or sets the SectionHeight for an ArrangementRun object.

**Example:**      This example gets the SectionHeight for the `objRun1` object.

```VBScript
     Dim dblSectionHeight   As Double
     dblSectionHeight = objRun1.SectionHeight

```

### Property **SectionType**( ) As [CATArrangementRouteSection](../CATArrangementInterfaces/enum_CATArrangementRouteSection_141224.md)

   Returns or sets the SectionType for an ArrangementRun object.

**Example:**      This example sets the SectionType for the `objRun1` object to `CatArrangementRouteSectionRectangular`.

```VBScript
     objRun1.SectionType = CatArrangementRouteSectionRectangular

```

### Property **SectionWidth**( ) As double

   Returns or sets the SectionWidth for an ArrangementRun object.

**Example:**      This example gets the SectionWidth for the `objRun1` object.

```VBScript
     Dim dblSectionWidth   As Double
     dblSectionWidth = objRun1.SectionWidth

```

### Property **VisuMode**( ) As [CATArrangementRouteVisuMode](../CATArrangementInterfaces/enum_CATArrangementRouteVisuMode_150809.md)

   Returns or sets the Visualization Mode for an ArrangementRun object.

**Example:**      This example sets the Visualization Mode for the `objRun1` object to `CatArrangementRouteVisuModeSolid`.

```VBScript
     objRun1.VisuMode = CatArrangementRouteVisuModeSolid

```

Methods

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the applicative data which type is the given parameter.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
` oApplicativeObj`      The matched applicative object.

**Example:**      This example retrieves the desired applicative object from the `objRun1` object.

```VBScript
     Dim objProd   As Product
     objProd  = objRun1.GetTechnologicalObject("Product")

```

---

# ArrangementRuns (Collection)

**_A collection object of ArrangementRun objects._**

**Role:** Use this collection object to manage ArrangementRun objects.

## Methods

### Func **AddRun**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListofMathPoints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iMathDirection`) As [CATIAArrangementRun](../CATArrangementInterfaces/interface_ArrangementRun_42486.md)

   Creates an ArrangementRun and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iListofMathPoints`      List of points through which to route.
` iMathDirection`      Starting routing direction.

**Returns:**      Returns the newly created ArrangementRun object and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementRun](../CATArrangementInterfaces/interface_ArrangementRun_42486.md)

   Returns the specified ArrangementRun item of the collection object.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRun to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementRun in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementRun by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementRun object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementRun object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRun to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementRun in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementRun by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# ArrBendableString (Object)

**_The interface to access a CATIAArrBendableString

Using this prefered syntax will enable mkdoc to document your class._**

## Methods

### Func **GetNumOfSegments**( ) As long

   Returns the cumulative number of the straight/arc segments that make up the Bendable object.

**Example:**      This example shows how to number of segments of `BendablePipe001`.

```VBScript
     Dim NumOfBendSegments
     NumOfBendSegments = BendablePipe001.GetNumOfSegments

```

### Func **GetNumOfSegmentsLocalAxis**( ) As long

   Returns the cumulative number of the straight/arc segments that make up the Bendable object.

### Sub **GetSegmentData**( long  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSegmentData`)

   Returns the data of the segment (Point Indices, Slope angle, Rotation Angle).

**Example:**      This example shows how to retrieve segment #2 of `BendablePipe001`.

```VBScript
     Dim SegmentData(14) As double
     BendablePipe001.GetSegmentData(2, SegmentData)
     where the data is returned in the Array in the following format...
     SegmentData(0)  = Starting Point of Segment (X Coord)
     SegmentData(1)  = Starting Point of Segment (Y Coord)
     SegmentData(2)  = Starting Point of Segment (Z Coord)
     SegmentData(3)  = End Point of Segment (X Coord)
     SegmentData(4)  = End Point of Segment (Y Coord)
     SegmentData(5)  = End Point of Segment (Z Coord)
     SegmentData(6)  = Bend Point of Segment (X Coord) '//Valid only if SegmentData(9) > 0
     SegmentData(7)  = Bend Point of Segment (Y Coord) '//Valid only if SegmentData(9) > 0
     SegmentData(8)  = Bend Point of Segment (Z Coord) '//Valid only if SegmentData(9) > 0
     SegmentData(9)  = Bend Radius at Bend Point '//Valid only if SegmentData(9) > 0
     SegmentData(10) = Bend Angle at Bend Point  '//Valid only if SegmentData(9) > 0
     SegmentData(11) = Rotation Angle of Segment
     SegmentData(12) = Slope Angle of Segment
     SegmentData(13) = Length of linear Segment
     SegmentData(14) = Length of Arc Segment '//Valid only if SegmentData(9) > 0

```

### Func **InstanceName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the Bendable's Instance Name.

**Example:**      This example shows how to retrieve the Bendable Instance Name of `BendablePipe001`.

```VBScript
     Dim _BendInstanceName
     _BendInstanceName = BendablePipe001.InstanceName

```

---

# ArrBOMReport (Object)

**_The interface to access a CATIAArrBOMReport_**

## Methods

### Sub **GenerateBOMReport**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocumentToExtractData`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iOutputFileName`)

   This method generate a BOM report on the current piping document to an output html file.

---

# ArrNomenclature (Object)

**_Represents the UserNomenclature object._**
The UserNomenclature object is used in the CATIAArrNomenclatureTree object to maintain the hierarchy of user type names and associated icons. CATIAArrNomenclatureTree | |_______ Area - (I_ArrArea) | |_______ Building - (I_ArrBuilding) | |_______ Safety Zone - (I_ArrSafetyZone) | |-------- Run - (I_ArrRun) | |_______ Conduit Run |_______ Raceway Run In the diagram shown above, Area (along with its subtypes) and and Run (also along with it's subtypes) are all UserNomenclature objects. Entries such as the Area and Run are called System or SuperClass objects that have to be defined first before the subclasses such as Building and Safety Zone are defined. SuperClasses will not have a supertype. Each Nomenclature holds the following information... (1) NLSName - So as to support names in different languages (2) IconName - So as to allow user's to define their own icons (3) SuperType - For subtypes to fetch their parent names (4) SubTypes - SubTypes defined under this User Nomenclature

## Properties

### Property **IconName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets/Sets the Icon Name associated to the Type Name. The IconName is the file name, without the extension, of the Icon bitmap representing this user type. The icon definition file must be in one of the icon directories defined in the search paths used by CATIA.  
### Property **IntSysClassName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets/Sets the internal class names for System nomenclatures. This value is set only for System nomenclatures  
### Property **NLSInstanceName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets/Sets the InstanceName  
### Property **SubTypes**( ) As [CATIAArrNomenclatures](../CATArrangementInterfaces/interface_ArrNomenclatures_55994.md) (Read Only)

   Returns the collection of subtype UserNomenclatures within this UserNomenclature.  
### Property **SuperTypeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Get/Set the Supertype Information This property is used to set the subtypes for system classes  Methods

### Func **IsSystemNomenclature**( ) As boolean

   Returns TRUE if the nomenclature happens to be a system nomenclature. Returns FALSE if it is a user specified nomenclature.

---

# ArrNomenclatures (Collection)

**_The collection of UserNomenclature objects._**

## Methods

### Func **AddUserNomenclature**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIconName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iClassType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSuperType`) As [CATIAArrNomenclature](../CATArrangementInterfaces/interface_ArrNomenclature_48920.md)

   Creates a new UserNomenclature and adds it to this collection. The NomenclatureType of the new UserNomenclature will be "User". The base objects in the UserDictionary are created when the UserDictionary is created.

**Parameters:**

` iName`      The user nomenclature name.
` iIconName`      The icon name associated to this nomenclature name.

**Returns:**      The new UserNomenclature.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrNomenclature](../CATArrangementInterfaces/interface_ArrNomenclature_48920.md)

   Returns the specified item of the collection

**Parameters:**

` iItem`      The list index (long) or name (CATBSTR) of the member to retrieve.

**Returns:**      The retrieved member object.

---

# ArrNomenclatureTree (Object)

**_Represents the root User Dictionary object._**
The user dictionary defines a hierarchy of user object type names used for dynamically classifying objects. These type names are defined by the user organization according to the needs of the disciplines represented in the data. The user type of any object may be changed as the data becomes more precise. The hierarchy of type names starts with base names, defined by the system, for each type of object. The user organization may define or change the hierarchy of type names under each base name.

## Properties

### Property **BaseNomenclatures**( ) As [CATIAArrNomenclatures](../CATArrangementInterfaces/interface_ArrNomenclatures_55994.md) (Read Only)

   Returns the collection of BaseNomenclatures within this UserDictionary.  Methods

### Func **GetNomenclature**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeName`) As [CATIAArrNomenclature](../CATArrangementInterfaces/interface_ArrNomenclature_48920.md)

   Finds a UserNomenclature by Name from this UserDictionary.

---

# ArrSystemLineProduct (Object)

**_The interface to access a CATIAArrSystemLineProduct

Using this prefered syntax will enable mkdoc to document your class._**

## Methods

### Func **GetSubItem**( long  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Allows the user to get the item at a specific index location.  
### Func **GetSubProductsCount**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIntfId`) As long

   Returns the count of the sub-products that make up the System-Line Arrangement Product and that match a specifc interface id. If the interface Id is NULL, then it searches for CATIAProduct objects by default.

---

# ArrWorkbench (Object)

**_Returns the Arrangement Workbench._**

**Role:** Use this interface to manage the ArrNomenclatureTree object, create Arrangement objects (such as ArrangementArea, ArrangementRun etc).

## Properties

### Property **ArrNomenclatureTree**( ) As [CATIAArrNomenclatureTree](../CATArrangementInterfaces/interface_ArrNomenclatureTree_76774.md) (Read Only)

   Returns the ArrNomenclatureTree.  Methods

### Func **AddNomenclatureTree**( ) As [CATIAArrNomenclatureTree](../CATArrangementInterfaces/interface_ArrNomenclatureTree_76774.md)

   This method allows the user to add a nomenclature tree if the get_ArrNomenclatureTree returns a Return code of E_FAIL. Basically, the workbench could not locate the startup instance to generate the necessary NomenclatureTree information.  
### Func **ConvertArrangementProductToProduct**( [CATIAArrangementProduct](../CATArrangementInterfaces/interface_ArrangementProduct_70174.md)  `iArrProduct`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   This method converts an ArrangementProduct back to a Product.

**Parameters:**

` iArrProduct`      Input ArrangementProduct to be converted.

**Returns:**      oProduct As CATIAProduct Converted Product.  **See also:**      [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Func **ConvertProductToArrangementProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATIAArrangementProduct](../CATArrangementInterfaces/interface_ArrangementProduct_70174.md)

   This method converts a Product to an ArrangementProduct.

**Parameters:**

` iProduct`      Input Product to be converted.

**Returns:**      oArrProduct Converted ArrangementProduct.  **See also:**      [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Func **FindInterface**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   This method returns a interface handle as specified by the input interface name and the input interface handle.

```VBScript
     Dim interfaceFound As AnyObject
     Set interfaceFound = CATIAArrWorkbench.FindInterface("InterfaceNameToFind",CATIAProduct_iObject)

```

**Parameters:**

` iInterfaceName`      interface name to search for ("CATIAxxxx")
` iObject`      The object to search for the required interface.

**Returns:**      oInterfaceFound interface handle found