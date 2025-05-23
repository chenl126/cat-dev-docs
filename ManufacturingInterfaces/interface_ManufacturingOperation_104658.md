# ManufacturingOperation (Object)

**_ManufacturingOperation defines a set of methods._**

## Properties

### Property **Comment**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Return the Comment linked to a Manufacturing Operation.

**Example:**     The following example returns the Comment `ThisComment` linked to a manufacturing operation `CurrentMo`

```VBScript
     Set ThisComment = CurrentMo.Comment

```

Methods

### Sub **AddClearance**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  double  `iA`,  double  `iB`,  double  `iC`,  double  `iD`)

   Add a 'clearance to a plane' path to a Manufacturing Operation.

**Example:**     The following example add a path (clerarance) on approach macro of `operation`

```VBScript
     call Operation.AddClearance("Approach", A, B, C, D)

```

### Sub **AddDistanceAlongAlineMotion**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Add a path 'distance along a line' to a Manufacturing Operation.

**Example:**     The following example add a path (distance along a line) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAlineMotion("LinkingApproach", distance, iLine, iProduct)

```

### Sub **AddDistanceAlongAlineMotionFeed**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`,  double  `iFeedrateValue`)

   Add a path 'distance along a line' with Feedrate info to a Manufacturing Operation.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be

`"None"`      `"Machining"`      `"Approach"`      `"Retract"`      `"RAPID"`      `"Local"`
` iFeedrateValue`      feedrate Value in MKS units : m/s if linear feedrate, or m/turn if angular feedrate (take into account only if iFeedrateType = "Local")  **Example:**     The following example add a path (distance along a line) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAlineMotionFeed("LinkingApproach", distance, iLine, iProduct, iFeedrateType, iFeedrateValue)

```

### Sub **AddDistanceAlongAxis**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`)

   Add a path 'distance along axis' to a Manufacturing Operation.

**Example:**     The following example add a path (distance along axis) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAxis("LinkingApproach", distance)

```

### Sub **AddDistanceAlongAxisFeed**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`,  double  `iFeedrateValue`)

   Add a path 'distance along axis' with Feedrate info to a Manufacturing Operation.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be

`"None"`      `"Machining"`      `"Approach"`      `"Retract"`      `"RAPID"`      `"Local"`
` iFeedrateValue`      feedrate Value in MKS units : m/s if linear feedrate, or m/turn if angular feedrate (take into account only if iFeedrateType = "Local")  **Example:**     The following example add a path (distance along axis) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAxisFeed("LinkingApproach", distance, iFeedrateType, iFeedrateValue)

```

### Sub **AddGotoHorizontal**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  double  `iDistance`,  double  `iAngle1`,  double  `iAngle2`)

   Add a path 'goto horizontal' to a Manufacturing Operation.

**Example:**     The following example add a path (goto horizontal) on approach macro of `operation`

```VBScript
     call Operation.AddGotoHorizontal("Approach", distance, angle1, angle2)

```

### Sub **AddMotionGoToAPoint**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPoint`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Add a path 'goto a point' to a Manufacturing Operation.

**Example:**     The following example add a path (goto a point ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionGoToAPoint("Approach", iPoint, iProduct )

```

### Sub **AddMotionGoToAPointFeed**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPoint`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`,  double  `iFeedrateValue`)

   Add a path 'goto a point' with Feedrate info to a Manufacturing Operation.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be

`"None"`      `"Machining"`      `"Approach"`      `"Retract"`      `"RAPID"`      `"Local"`
` iFeedrateValue`      feedrate Value in MKS units : m/s if linear feedrate, or m/turn if angular feedrate (take into account only if iFeedrateType = "Local")  **Example:**     The following example add a path (goto a point ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionGoToAPointFeed("Approach", iPoint, iProduct, iFeedrateType, iFeedrateValue)

```

### Sub **AddMotionToAPlane**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  short  `iMode`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPlane`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Add a path 'goto a plane with axial or perpendicular move' to a Manufacturing Operation.

**Example:**     The following example add a path (goto a plane with axial move ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionToAPlane("Approach", 1, iPlane, iProduct)

```

**Example:**     The following example add a path (goto a plane with perpendicular move ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionToAPlane("Approach", 0, iPlane, iProduct)

```

### Sub **AddPPWords**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPPWords`)

   Add a path 'PP Words' to a Manufacturing Operation.

**Example:**     The following example add a path (PP Words) on the retract group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddPPWords("LinkingRetract", "PP Words example")

```

### Func **GetAGeometricAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve a Geometric Attribute of a Manufacturing Operation.

**Example:**     The following example retrieves in `Offset` the attribute `OriginOffset` of Manufacturing Operation `firstOperation`

```VBScript
     Set Offset = firstOperation.GetAttribute(OriginOffset)

```

### Func **GetAnAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve the Attribute of a Manufacturing Operation.

**Example:**     The following example Retrieves in `RapidFeed` the attribute `MfgRapidFeed` of Manufacturing Operation `firstOperation`

```VBScript
     Set RapidFeed = firstOperation.GetAttribute(MfgRapidFeed)

```

### Func **GetFeature**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve the Machinable Feature asociated to a Manufacturing Operation.

**Example:**     The following example Retrieves in `firstOperation` the machinable feature `Feature`

```VBScript
     call firstOperation.GetFeature(Feature)

```

### Func **GetFeedSpeedAutoUpdate**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As boolean

   Returns the Auto Update status for Feed Rate or Spindle Speed.

**Parameters:**

` iType`      Determines if the method works on Feed Rate or Spindle Speed **Legal values** : iType can be

  * `"FEEDRATE"`
  * `"SPINDLESPEED"`

**Returns:**      oAutoUpdate Auto update status

  * **Example:**
  * The following example checks the status of AutoUpdate for Feed Rate
  * Dim isAutoUpdateEnabled As Boolean
  * isAutoUpdateEnabled = firstOperation.GetFeedSpeedAutoUpdate("FEEDRATE")

### Func **GetListOfToolMotions**( ) As [CATIAMfgToolMotions](../ManufacturingInterfaces/interface_MfgToolMotions_42584.md)

   Give a list of Manufacturing ToolMotion contained by a sequential operation.

See interface CATIAMfgToolMotions for methods available on the list      The following example extract the tool motions of operation SeqMO in the MfgToolMotions      list TMList2 .

```VBScript

     **Example:**
    	Dim TMList2 As MfgToolMotions
    	Set TMList2 = SeqMO.GetListOfToolMotions
    	Dim Test2 As ManufacturingToolMotion
    	Set Test2 = TMList2.GetElement(1)

```

### Func **GetManufacturingFeature**( ) As [CATIAManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

   Retrieve the Manufacturing Feature asociated to a Manufacturing Operation.

**Example:**     The following example Retrieves in `firstOperation` the manufacturing feature `Feature`

```VBScript
     Set Feature = firstOperation.GetManufacturingFeature

```

### Func **GetMfgAparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim A
     Set A = firstOperation.GetMfgBparamTopPln

```

### Func **GetMfgAxialFeatureDiameter**( ) As double

   Retrieve the diameter of an axial manufacturing feature.

**Example:**     The following example Retrieves in `Diam` the diameter of the axial manufacturing feature linked to the operation `firstOperation`

```VBScript
     Dim Diam
     Set Diam = firstOperation.GetMfgAxialFeatureDiameter

```

### Func **GetMfgBparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim B
     Set B = firstOperation.GetMfgBparamTopPln

```

### Func **GetMfgCparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim C
     Set C = firstOperation.GetMfgCparamTopPln

```

### Func **GetMfgDparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim D
     Set D = firstOperation.GetMfgDparamTopPln

```

### Sub **GetMfgFeaturePosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioPosition`)

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim oPositionArray(3) As CATSafeArrayVariant
     Call firstOperation.GetMfgFeaturePosition(oPositionArray)
     Assume this array is oPositionArray. It contains:

     oPositionArray[0],oPositionArray[1],oPositionArray[2]
         The X, Y, and Z direction vector components

     **Example:**
         The following example returns in oPositionArray
     the coordinates of the feature position

```VBScript
     Call firstOperation.GetMfgFeaturePosition(oCoord)
     x = oPositionArray[0]
     y = oPositionArray[1]
     z = oPositionArray[2]

```

### Func **GetMfgFeatureXPosition**( ) As double

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim X
     X = firstOperation.GetMfgFeatureXPosition

```

### Func **GetMfgFeatureYPosition**( ) As double

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim Y
     Y = firstOperation.GetMfgFeatureYPosition

```

### Func **GetMfgFeatureZPosition**( ) As double

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim Z
     Z = firstOperation.GetMfgFeatureZPosition

```

### Sub **GetMfgTopPlane**( double  `oA`,  double  `oB`,  double  `oC`,  double  `oD`)

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Call firstOperation.GetMfgTopPlane(A,B,C,D)

```

### Func **GetPattern**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve the Machining Pattern asociated to a Manufacturing Operation.

**Example:**     The following example Retrieves in `firstOperation` the machining pattern `Pattern`

```VBScript
     Set Pattern = firstOperation.GetPattern

```

### Func **GetRadiusOnMacro**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMacroType`) As double

   Retrieves radius attribute on the circular elementary macro motion on CIRCULAR MILLING or THREAD MILLING operations ONLY.

**Parameters:**

` iMacroType`      **Legal values** : iMacroType can be:

`"Approach"`, to get the radius on the Approach Macro      `"Retract"`, to get the radius on the Retract Macro      `"ReturnInALevelApproach"`, to get the radius on the Return in a level Macro (Approach)      `"ReturnInALevelRetract"`, to get the radius on the Return in a level Macro (Retract)      `"ReturnBetweenLevelsApproach"`, to get the radius on the Return between levels Macro (Approach)      `"ReturnBetweenLevelsRetract"`, to get the radius on the Return between levels Macro (Approach)
` oRadius`      Radius value. (expressed in millimeters)  **Example:**     The following example retrieves the radius on the circular motion of the retract macro on the Circular Milling operation CircularMilling1

```VBScript
     dim RadValue as double
     RadValue = CircularMilling1.GetRadiusOnMacro("Retract")

```

### Sub **GetRelimitingGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oProduct`,  double  `oOffset`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPosition`)

   Retrieves start / end element on PROFILE CONTOURING operation ONLY.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be:

`"StartElement"`, to get the Start element on Profile Contouring      `"EndElement"`, to get the End element on Profile Contouring
` oReference`      The relimiting geometry.
` oProduct`      Product containing the relimiting geometry.
` oOffset`      Offset set on the relimiting geometry. (expressed in millimeters)
` oPosition`      Tool position set on the relimiting geometry.

**Legal values** : oPosition can be:

`"IN"`     `"ON"`     `"OUT"`     **Example:**     The following example gets the End relimiting element of the Profile Contouring operation Contouring1

```VBScript
     Call Contouring1.GetRelimitingGeometry("EndElement",RelimitingElement,PartMachined,Offset,Position)

```

### Sub **GetStartPointGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oGeometryPosition`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oProduct`,  double  `oOffset`)

   Retrieves geometry and offset of a start point on POCKETING operation ONLY.

**Parameters:**

` oGeometryPosition`      **Legal values** : oGeometryPosition can be:

`"Outside"`, if the start point is outside the pocket contour      `"Inside"`, if the start point is inside the pocket contour
` oReference`      The start point geometry.
` oProduct`      Product containing the start point geometry.
` oOffset`      Offset set on the start point. (expressed in millimeters)
Offset has a meaning only if oGeometryPosition value is "Outside".  **Example:**     The following example gets the Start point geometry on the Pocketing operation Pocketing1

```VBScript
     Call Pocketing1.GetStartPointGeometry(Position,Point1,Part,OffsetValue)

```

### Sub **GetToolGage**( double  `oMinToolLength`,  double  `oMinToolGage`)

   Retrieves the minimum tool cutting lentgh and the minimum tool gage length.

**Example:**     The following example Retrieves in `MinToolLength` and `MinToolGage` the values of tool of Manufacturing Operation `Operation`

```VBScript
     Call Operation.GetToolGage(MinToolLength,MinToolGage)

```

### Sub **GetTrajectoryEndPointCoord**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oEndPoint`)

   Retrieve the Machining Operation's trajectory end point.

**Example:**     The following example Retrieves in `oEndPoint` the end point of the Machining Operation `Operation`

```VBScript
     Dim oEndPoint(2)
     call Operation.GetTrajectoryEndPointCoord(oEndPoint)
     x = oEndPoint(0)
     y = oEndPoint(1)
     z = oEndPoint(2)

```

### Sub **GetTrajectoryStartPointCoord**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oStartPoint`)

   Retrieve the Machining Operation's trajectory start point.

**Example:**     The following example Retrieves in `oStartPoint` the start point of the Machining Operation `Operation`

```VBScript
     Dim oEndPoint(2)
     call Operation.GetTrajectoryStartPointCoord(oStartPoint)
     x = oStartPoint(0)
     y = oStartPoint(1)
     z = oStartPoint(2)

```

### Func **InsertToolMotion**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  short  `iPosition`) As [CATIAManufacturingToolMotion](../ManufacturingInterfaces/interface_ManufacturingToolMotion_113852.md)

   Create, given its type, a Manufacturing ToolMotion inside a sequential operation.

    The available type for lathe sequential operation are :     for GoStandard and GoGo tool motion iType = `MfgSeqMotionLatheGoStd`     for GoDelta tool motion, iType = `MfgSeqMotionLatheDelta`     for Indirv tool motion, iType = `MfgSeqMotionLatheIndirv`     for Follow tool motion, iType = `MfgSeqMotionLatheFollow`     for PPWord tool motion, iType = `MfgSeqMotionPPWord`          The available type for prismatic sequential operation are :     for Goto Point tool motion, iType = `MfgSeqMotionPoint`     for Goto Position tool motion, iType = `MfgSeqMotionPosition`     for Goto Delta tool motion, iType = `MfgSeqMotionDelta`      `iType` type of the ToolMotion to be created `iPosition` rank in the operation list where the ToolMotion will be created      iPosition=0 means creation at the end of the list of tool motions `oToolMotion` the created ManufacturingToolMotion          The following example creates in ManufacturingOperation `SeqMO`      which is a Lathe Sequential operation     the ManufacturingToolMotion `ThisToolMotion` of type `MfgSeqMotionLatheGoStd` at the first rank

```VBScript

     **Example:**
    	Set SeqMO = Program1.AppendOperation("MfgLatheMfgSequentialOperation",1)
    	Set ThisToolMotion = SeqMO.InsertToolMotion("MfgSeqMotionLatheGoStd",1)

```

    The following example creates in ManufacturingOperation `SeqMO`      which is an Axial Point to Point sequential operation     the ManufacturingToolMotion `ThisToolMotion` of type `MfgSeqMotionPoint` at the first rank

```VBScript

     **Example:**
    	Set SeqMO = Program1.AppendOperation("PointToPoint",1)
    	Set ThisToolMotion = SeqMO.InsertToolMotion("MfgSeqMotionPoint",1)

```

### Func **IsGeometricallyAccessibleOnSetup**( [CATIABase](../System/interface_AnyObject_17321.md)  `iManufacturingSetup`) As boolean

   Returns True if the Manufacturing Axial Operation is geometrically accessible on the given Manufacturing Setup.The Axial Operation must have a valid tool axis and a machine must be assigned to the Manufacturing Setup. If this is not the case, the method returns False.

**Parameters:**

` iSetup`      The Manufacturing Setup gives the accessibility checking context : the part,the machine and the relative orientation of the part on the machine.

**Example:**     The following example checks the accessibility of `firstOperation` on `firstSetup`.

```VBScript
     Dim isAccessible As Boolean
     isAccessible = firstOperation.IsGeometricallyAccessibleOnSetup(firstSetup)

```

### Sub **RemoveRelimitingGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`)

   Removes the geometry on relimiting element PROFILE CONTOURING operation ONLY.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be:

`"StartElement"`, to remove the Start element on Profile Contouring      `"EndElement"`, to remove the End element on Profile Contouring      **Example:**     The following example removes the End relimiting element of the Profile Contouring operation Contouring1

```VBScript
     Call Contouring1.RemoveRelimitingGeometry("EndElement")

```

### Sub **RemoveStartPointGeometry**( )

   Removes the start point element on POCKETING operation ONLY.

**Example:**     The following example removes the start point of the Pocketing operation Pocketing1

```VBScript
     Call Pocketing1.RemoveStartPointGeometry

```

### Sub **SetFeature**( [CATIABase](../System/interface_AnyObject_17321.md)  `iMachinableFeature`)

   Associate a Machinable Feature to a Manufacturing Operation.

**Example:**     The following example associates in `firstOperation` the machinable feature `Feature`

```VBScript
     call firstOperation.SetFeature(Feature)

```

### Sub **SetFeedSpeedAutoUpdate**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  boolean  `iAutoUpdate`)

   Set the Auto Update status for Feed Rate or Spindle Speed.

**Parameters:**

` iType`      Determines if the method works on Feed Rate or Spindle Speed **Legal values** : iType can be

  * `"FEEDRATE"`
  * `"SPINDLESPEED"`

` iAutoUpdate`      Auto update status **Legal values** : iType can be

  * `True`
  * `False`

    * **Example:**
    * The following example enables AutoUpdate for Spindle Speed
    * firstOperation.SetFeedSpeedAutoUpdate("SPINDLESPEED", True)

### Sub **SetFeedrateMagnitude**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`)

   Defines the magnitude of the feedrate values.

```VBScript

         The available types for Magnitude are:
         for Linear Magnitude , iMagnitudeName = LINEARFEEDRATE
         for Angular Magnitude , iMagnitudeName = ANGULARFEEDRATE

     **Example:**
     Dim Operation1 As ManufacturingOperation
     Set Operation1 = Program1.AppendOperation ("Drilling",1)
     Operation1.SetFeedrateMagnitude("LINEARFEEDRATE")

```

### Sub **SetGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  short  `iPosition`)

   Assigns geometry to a Manufacturing Operation.

**Parameters:**

` iGeometryType`      Type of geometry to assign (Parts, Drives, ..)
` iReference`      Geometry to assign: it may be a feature (point, hole, ..) or a BREP feature.
` iProduct`      Product containing the geometry to assign. It must be the occurence of the product which owns the part containing the geometry. Also see method GetProductInstance of CATIAManufacturingSetup interface.
` iPosition`      Position of the geometry in the list (0 to append at the end of the list). **Example:**     The following example assigns the plane `Plane.1` as bottom of operation ` Pocketing1 ` of the Manufacturing Program `Program1`. The Product `Product1` is associated to Manufacturing Setup ` Setup1`. This example is valid only if the Product owning the part which contains the plane has been associated to the Manufacturing Setup (if the CATPart containing the plane has been associated to the Manufacturing Setup). In other cases, the product must be retrieved differently.

```VBScript
     Set Product1 = Setup1.GetProductInstance()
     Dim Pocketing1 As ManufacturingOperation
     Set Pocketing1 = Program1.AppendOperation ("Pocketing",1)
     Pocketing1 .SetGeometry("PartBottom",Plane1,Product1,0)

```

### Sub **SetPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPattern`)

   Associate a Machining Pattern to a Manufacturing Operation.

**Example:**     The following example associates in `firstOperation` the machining pattern `Pattern`

```VBScript
     call firstOperation.SetPattern(Pattern)

```

### Sub **SetRadiusOnMacro**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMacroType`,  double  `iRadius`)

   Defines radius attribute on the circular elementary macro motion on CIRCULAR MILLING or THREAD MILLING operations ONLY.

**Parameters:**

` iMacroType`      **Legal values** : iMacroType can be:

`"Approach"`, to set the radius on the Approach Macro      `"Retract"`, to set the radius on the Retract Macro      `"ReturnInALevelApproach"`, to set the radius on the Return in a level Macro (Approach)      `"ReturnInALevelRetract"`, to set the radius on the Return in a level Macro (Retract)      `"ReturnBetweenLevelsApproach"`, to set the radius on the Return between levels Macro (Approach)      `"ReturnBetweenLevelsRetract"`, to set the radius on the Return between levels Macro (Approach)
` iRadius`      Radius value. (expressed in millimeters)  **Example:**     The following example sets a radius 5mm on the circular motion of the retract macro on the Circular Milling operation CircularMilling1

```VBScript
     Dim CircularMilling1 As ManufacturingOperation
     Set CircularMilling1 = Program1.AppendOperation ("CircularMilling1",1)
     Call CircularMilling1.SetRadiusOnMacro("Retract",5.00)

```

### Sub **SetRelimitingGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  double  `iOffset`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPosition`)

   Defines start / end element on PROFILE CONTOURING operation ONLY.
Sets a geometry on relimiting element in profile contouring operation.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be:

`"StartElement"`, to set the Start element on Profile Contouring      `"EndElement"`, to set the End element on Profile Contouring
` iReference`      Geometries to be set. It can be a list of curves or a single point. The curves must be adjacent.
` iProduct`      Product containing the geometry to be set.
` iOffset`      Offset to set on the relimiting geometry. (expressed in millimeters)
` iPosition`      Tool position to set on the relimiting geometry.

**Legal values** : iPosition can be:

`"IN"`, to set the tool position IN      `"ON"`, to set the tool position ON      `"OUT"`, to set the tool position OUT      **Example:**     The following example sets the Start relimiting element Curve1 on the Profile Contouring operation Contouring1

```VBScript
     Call Contouring1.SetRelimitingGeometry("StartElement",Curve1,PartMachined,3.00,"ON")

```

### Sub **SetSpindleMagnitude**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`)

   Defines the magnitude of the spindle values.

```VBScript

         The available types for Magnitude are:
         for Linear Magnitude , iMagnitudeName = LINEARSPINDLESPEED
         for Angular Magnitude , iMagnitudeName = ANGULARSPINDLESPEED

     **Example:**
     Dim Operation1 As ManufacturingOperation
     Set Operation1 = Program1.AppendOperation ("Drilling",1)
     Operation1.SetSpindleMagnitude("ANGULARSPINDLESPEED")

```

### Sub **SetStartPointGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryPosition`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  double  `iOffset`)

   Defines the geometry and the offset of a start point on POCKETING operation ONLY.

**Parameters:**

` iGeometryPosition`      **Legal values** : iGeometryPosition can be:

`"Outside"`, to set the Start point outside the pocket contour      `"Inside"`, to set the Start point inside the pocket contour
` iReference`      Geometry to be set. It can be a point.
` iProduct`      Product containing the geometry to be set.
` iOffset`      Offset set on the start point. (expressed in millimeters)
Offset is taken into account only if iGeometryPosition is set to "Outside".  **Example:**     The following example sets Point1 as Start point on the Pocketing operation Pocketing1

```VBScript
     Call Pocketing1.SetStartPointGeometry("Inside",Point1,PartMachined,0.00)

```

### Sub **SetTool**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolName`)

   Assign an already created tool to a Manufacturing Operation.
If the tool is not already created, or if it is not authorized for this kind of Manufacturing Operation, a default tool is created.

**Example:**     The following example assign a drill tool named `D-9.7` on the operation ` MO1` of the Manufacturing Program `Program1` A tool change with tool `D-9.7` has already been created in the Manufacturing Program.

```VBScript
     Dim Operation1 As ManufacturingOperation
     Set Operation1 = Program1.AppendOperation ("Drilling",1)
     Operation1.SetTool("D-9.7")

```