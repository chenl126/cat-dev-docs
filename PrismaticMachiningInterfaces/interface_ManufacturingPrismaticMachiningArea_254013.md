# ManufacturingPrismaticMachiningArea (Object)

**_ManufacturingPrismaticMachiningArea defines a set of properties and methods._**

## Properties

### Property **BottomType**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Hardness Mode on Bottom of a Manufacturing Prismatic Machining Area.

**Examples:**     The following example returns the hardness mode on bottom `ThisBottomType` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim ThisBottomType As CATBSTR
     ThisBottomType = CurrentPMA.BottomType

```

    The next example sets the hardness mode on bottom of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     CurrentPMA.BottomType = "**MfgHard** "

    To be allowed to change BottomType into **MfgSoft** , Islands geometries must be removed first.

```

**Legal values** : BottomType can be

`**MfgHard**` `**MfgSoft**` 
### Property **ContoursCount**( ) As long (Read Only)

   Retreives the number of Contour of a Manufacturing Prismatic Machining Area.

**Example:**     The following example returns the number of Contour `NumberOfContour` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim NumberOfContour As Long
     NumberOfContour = CurrentPMA.ContoursCount

```

### Property **IslandsCount**( ) As long (Read Only)

   Retreives the number of Island of a Manufacturing Prismatic Machining Area.

**Example:**     The following example returns the number of Island `NumberOfIsland` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim NumberOfIsland As Long
     NumberOfIsland = CurrentPMA.IslandsCount

```

### Property **TopType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Hardness Mode on top of a Manufacturing Prismatic Machining Area.

**Examples:**     The following example returns the hardness mode on top `ThisTopType` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim ThisTopType As CATBSTR
     ThisTopType = CurrentPMA.TopType

```

    The next example sets the hardness mode on top of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     CurrentPMA.TopType = "**MfgHard** "

```

**Legal values** : TopType can be

`**MfgHard**` `**MfgSoft**` 
### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Type of a Manufacturing Prismatic Machining Area.

**Examples:**     The following example returns the feature type `ThisType` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim ThisType As CATBSTR
     ThisType = CurrentPMA.Type

```

    The next example sets the feature type of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     CurrentPMA.Type = "**MfgPocketType** "

    To be allowed to change Type into **MfgPocketType** or into **MfgContouringType** , Contours and Islands geometries must be removed first.

```

**Legal values** : Type can be

`**MfgPocketType**` `**MfgContouringType**` Methods

### Func **GetContourSide**( long  `iContourNumber`) As short

   Gets the side of one contour of a Manufacturing Prismatic Machining Area.

**Parameters:**

` iContourNumber`      The geometry index inside the collection.

    Must be between 1 and ContoursCount (see Properties).

**Example:** The following example gets the side of the contour number `iContourNumber` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim iContourNumber As Long
     iContourNumber = 3

     Dim oContourSide As short
     oContourSide = CurrentPMA.GetContourSide(iContourNumber)

```

### Func **GetGeometriesAquisitionMode**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  long  `iGeometryNumber`) As short

   Gets the aquisition mode of one geometry of a Manufacturing Prismatic Machining Area.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be

`Contours`      to get the aquisition mode of a guiding element `Islands`      to get the aquisition mode of an island
(not allowed if Type == "MfgContouringType" or
if BottomType == "MfgSoft") (see Properties).
` iGeometryNumber`      The geometry index inside the collection.

    Must be 1 if Type == "MfgPocketType" (see Properties) and iGeometryType == "Contours".     Must be between 1 and IslandsCount + 1 (or ContoursCount + 1) (see Properties).

**Example:** The following example gets the aquisition mode of the contour number `iGeometryNumber` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim iGeometryNumber As Long
     iGeometryNumber = 3

     Dim oMode As Short
     oMode = CurrentPMA.GetGeometriesAquisitionMode("Contours",iGeometryNumber)

```

**Legal values** : GetGeometriesAquisitionMode value can be

`0`      by Edges `1`      by Belt of Faces `2`      by Boundary of Faces (Islands only) `5`      by Boundary of Faces (Contours only)

### Func **IsContourClosed**( long  `iContourNumber`) As short

   Return the status of one contour of a Manufacturing Prismatic Machining Area : closed or open.

**Parameters:**

` iContourNumber`      The geometry index inside the collection.

    Must be between 1 and ContoursCount (see Properties).

**Example:** The following example returns the status of the contour number `iContourNumber` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim iContourNumber As Long
     iContourNumber = 3

     Dim oIsClosed As short
     oIsClosed = CurrentPMA.IsContourClosed(iContourNumber)

```

**Legal values** : IsContourClosed value can be

`0` (means open contour) `1` (means closed contour)

### Sub **RemoveAllGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`)

   Removes all the geometry of a specified type linked to a Manufacturing Prismatic Machining Area.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be

`RelimitingPlane`      to remove the top plane `Parts`      to remove the bottom `Checks`      to remove the check elements `Contours`      to remove the guiding elements `Islands`      to remove the islands

**Example:** The following example removes the bottom of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Call CurrentPMA.RemoveAllGeometry("Parts")

```

### Sub **SetClosedContourSide**( long  `iContourNumber`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSide`)

   Sets the side of one closed contour of a Manufacturing Prismatic Machining Area.

**Parameters:**

` iContourNumber`      The geometry index inside the collection.

    Must be between 1 and ContoursCount (see Properties).
` iSide`      **Legal values** : iSide can be

`Inside` `Outside`

**Example:** The following example sets the side of the closed contour number `iContourNumber` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim iContourNumber As Long
     iContourNumber = 3

     Dim iContourSide As CATBSTR
     iContourSide = "Inside"
     Call CurrentPMA.SetClosedContourSide(iContourNumber,iContourSide)

```

### Sub **SetContourSide**( long  `iContourNumber`,  short  `iSide`)

   Sets the side of one contour of a Manufacturing Prismatic Machining Area.

**Parameters:**

` iContourNumber`      The geometry index inside the collection.

    Must be between 1 and ContoursCount (see Properties).
` iSide`      **Legal values** : iSide can be

`1` `2`

**Example:** The following example sets the side of the contour number `iContourNumber` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim iContourNumber As Long
     iContourNumber = 3

     Dim iContourSide As Short
     iContourSide = 2
     Call CurrentPMA.SetContourSide(iContourNumber,iContourSide)

```

### Sub **SetGeometries**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  short  `iMode`,  long  `iGeometryNumber`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  short  `iPosition`)

   Sets or adds geometry in a collection of a specified type to a Manufacturing Prismatic Machining Area.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be

`Contours`      to set or to add a guiding element `Islands`      to set or to add an island
(not allowed if Type == "MfgContouringType" or
if BottomType == "MfgSoft") (see Properties).
` iMode`      **Legal values** : iMode can be

`0`      by Edges
` iGeometryNumber`      The geometry index inside the collection.

    Must be 1 if Type == "MfgPocketType" (see Properties) and iGeometryType == "Contours".     Must be between 1 and IslandsCount + 1 (or ContoursCount + 1) (see Properties).
` iReference`      The geometry to be set.
` iProduct`      The product containing the geometry to be set.
` iPosition`      0

**Example:** The following example sets 3 Islands, linked to 2 circles and 3 lines, to the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim iGeometryNumber As Long
     iGeometryNumber = 0
     ...
     'Get number of Island of CurrentPMA and add 1 to create a new island (Island number 1)
     iGeometryNumber = CurrentPMA.IslandsCount + 1
     Call CurrentPMA.SetGeometries("Islands",0,iGeometryNumber,Circle1,PartMachined,0)

     'Get number of Island of CurrentPMA and add 1 to create a new island  (Island number 2)
     iGeometryNumber = CurrentPMA.IslandsCount + 1
     Call CurrentPMA.SetGeometries("Islands",0,iGeometryNumber,Circle2,PartMachined,0)

     'Get number of Island of CurrentPMA and add 1 to create a new island  (Island number 3)
     iGeometryNumber = CurrentPMA.IslandsCount + 1
     Call CurrentPMA.SetGeometries("Islands",0,iGeometryNumber,Line5,PartMachined,0)

     'Adding Line6 to Island number 3
     Call CurrentPMA.SetGeometries("Islands",0,iGeometryNumber,Line6,PartMachined,0)

     'Adding Line7 to Island number 3
     Call CurrentPMA.SetGeometries("Islands",0,iGeometryNumber,Line7,PartMachined,0)

```

### Sub **SetGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  short  `iPosition`)

   Sets a geometry of a specified type to a Manufacturing Prismatic Machining Area.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be

`RelimitingPlane`      to set the top plane `Parts`      to set the bottom `Checks`      to set a check element
` iReference`      The geometry to be set.
` iProduct`      The product containing the geometry to be set.
` iPosition`      0

**Example:** The following example sets the top plane `Plane2` to the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Call CurrentPMA.SetGeometry("RelimitingPlane",Plane2,PartMachined,0)

```

### Sub **SetOpenContourSide**( long  `iContourNumber`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPoint`)

   Sets the side of one open contour of a Manufacturing Prismatic Machining Area.

**Parameters:**

` iContourNumber`      The geometry index inside the collection.

    Must be between 1 and ContoursCount (see Properties).
` iPoint`      A point near one of both limits of the contour.

    From this limit to the other one, the side of the contour is on the left.

**Example:** The following example sets the side of the open contour number `iContourNumber` of the manufacturing prismatic machining area `CurrentPMA`

```VBScript
     Dim iContourNumber As Long
     iContourNumber = 3

     Dim Point1 As CATIABase
     ...
     Set Point1 = hybridShapes1.Item("Point.1")
     ...

     Call CurrentPMA.SetOpenContourSide(iContourNumber,Point1)

```