# DNBHumanModelingInterfaces Framework

## Object Index

  * [SWKIKConstraint](DNBHumanModelingInterfaces/interface_SWKIKConstraint_46742.md)
  * [SWKManikin](DNBHumanModelingInterfaces/interface_SWKManikin_20702.md)
  * [SWKManikinPart](DNBHumanModelingInterfaces/interface_SWKManikinPart_40524.md)

---

# SWKIKConstraint (Object)

**_This interface manages the constraint of the manikin._**
It provides access to the constraints data (ID, EndEffector, StartSegment,...)

## Properties

### Property **Active**( ) As boolean

   Returns or sets the constraint activity.
A constraint being active means that the constraint is taken into
account during the resolution.

If the constraint is not active,then it is ignored during the resolution.  
### Property **AngleCriteria**( ) As double

   Returns or sets the angle criteria that will be used to evaluate success or failure of the constraint resolution. If, after resolution, the agle between the constraint and the target is lower than the criteria, then the constraint will be considered resolved. This criteria must be specified in radians.  
### Property **AngleToTarget**( ) As double (Read Only)

   Returns the angle (in radians) from the constraint end effector to the target.  
### Property **DistanceCriteria**( ) As double

   Returns or sets the distance criteria that will be used to evaluate success or failure of the constraint resolution. If, after resolution, the distance between the constraint and the target is lower than the criteria, then the constraint will be considered resolved. This criteria must be specified in millimeters.  
### Property **DistanceToTarget**( ) As double (Read Only)

   Returns the distance (in mm) from the constraint end effector to the target.  
### Property **EndEffector**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the end effector of the IK chain of the constraint. The string in this property is the short name of the last segment (or line of sight) to be driven by this constraint  
### Property **Identifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the identifier(ID) of the constraint.  
### Property **IsSuccess**( ) As boolean (Read Only)

   Returns whether the resolution of this constraint is a success or a failure, given the current criteria.  
### Property **Manikin**( ) As [SWKIAManikin](../DNBHumanModelingInterfaces/interface_SWKManikin_20702.md) (Read Only)

   Returns the manikin which owns this IK constraint.  
### Property **Priority**( ) As long

   Returns or sets the priority of the constraint.
When using that property, the number returned or set
is an integer and must be between 1 and 4 inclusive.
The lower the priority, the more prioritary the constraint becomes.  
### Property **RotationOffsetAngle**( ) As double

   Returns or sets the rotation offset angle for the 3D plane constraint.
This rotation offset angle(rad) is used to adjust 3D plane constraint.
When using that property, the number returned or set
must be between -PI and PI inclusive.

### Property **StartSegment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the first segment of the body to be driven by this constraint.  
### Property **TransferWithTarget**( ) As boolean

   Returns or sets the Transfer With Target property.  
### Property **UserType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the user type of the constraint. The user type returned will be one of the following: ("Contact", "Coincidence", "Fix", or "FixOn"),  Methods

### Func **GetConstraintElement**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns a reference to the target object of the constraint (if any).  
### Func **GetEndEffector**( ) As SWKIABodyElement

   Returns the end effector of the IK chain of the constraint.  
### Func **GetStartSegment**( ) As SWKIASegment

   Returns the start segment of the IK chain of the constraint.  
### Sub **GetTargetLine**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `poTargetLineCoord`)

   Get the target points coordinates of a line This method retrieves the origin point coordinates as (x, y, z) data and the direction value of a line.

**Parameters:**

` poTargetLineCoord`      The array of 6 data containing target point coordinates as x, y, z respectively and the x, y, z direction values for the target line.

### Sub **GetTargetPlane**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `poTargetPlaneCoord`)

   Get the target points coordinates of a line This method retrieves the origin point coordinates as (x, y, z) data and the direction value of a line.

**Parameters:**

` poTargetLineCoord`      The array of 9 data containing origin point coordinates as x, y, z, the first normalized direction as x, y, z coordinates and the x, y, z ortho-normalized direction values for the target plane.

### Sub **GetTargetPoint**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `poTargetPtCoord`)

   Get the target point coordinates. This method retrieves the target point coordinates as (x, y, z) data under an array form.

**Parameters:**

` poTargetPtCoord`      The array containing target point coordinates as x, y, z respectively, the x coordinate being the first data in the array.

### Sub **ResetTarget**( )

   Reset the offset of the target object (i.e. set the offset to the end effector's current position).  
### Sub **SetConstraintElement**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `piConstraintElement`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `piConstraintType`)

   Set the target object to follow. This method establishes a **part relation** between the end effector and an object to follow.

**Parameters:**

` piConstraintElement`      A reference to the target object
This target object can be either a wireframe
[GeometricElement](../SketcherInterfaces/interface_GeometricElement_54654.md) object such as a plane or a line, or a boundary representation object such as a face, a vertex or an edge. In the case of a 'Fix on' constraint, the target object must be the product ( CATIAProduct) associated with the constraint. ` piConstraintType`      The type of the constraint.
This parameter can take the following values: "Coincidence", "Contact", "Contact2D", "Contact3D", "FixPositon", "FixOrientation", "FixPositonAndOrientation", "FixOnPositon", "FixOnOrientation" and "FixOnPositonAndOrientation".

### Sub **SetTargetLine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `piObject`,  double  `piStartPointX`,  double  `piStartPointY`,  double  `piStartPointZ`,  double  `piEndPointX`,  double  `piEndPointY`,  double  `piEndPointZ`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `piConstraintType`)

   Set the target line to follow. This method establishes a **contact** or **coincidence** constraint between the end effector and the line.

**Parameters:**

` piConstraintElement`      A reference to the target object
This target object must be the product (
CATIAProduct) associated with the constraint. ` piStartPointX`      The x coordinate of the start point of the line, relatively to the father object.
` piStartPointY`      The y coordinate of the start point of the line, relatively to the father object.
` piStartPointZ`      The z coordinate of the start point of the line, relatively to the father object.
` piEndPointX`      The x coordinate of the end point of the line, relatively to the father object.
` piEndPointY`      The y coordinate of the end point of the line, relatively to the father object.
` piEndPointZ`      The z coordinate of the end point of the line, relatively to the father object.
` piConstraintType`      The type of the constraint.
This parameter can take the values "Contact", "Contact2D", "Contact3D" or "Coincidence".

### Sub **SetTargetPlane**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `piObject`,  double  `piOriginX`,  double  `piOriginY`,  double  `piOriginZ`,  double  `piNormalX`,  double  `piNormalY`,  double  `piNormalZ`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `piConstraintType`)

   Set the target plane to follow. This method establishes a **contact** or **coincidence** constraint between the end effector and the plane.

**Parameters:**

` piConstraintElement`      A reference to the target object
This target object must be the product (
CATIAProduct) associated with the constraint. ` piOriginX`      The x coordinate of the origin of the plane, relatively to the father object.
` piOriginY`      The y coordinate of the origin of the plane, relatively to the father object.
` piOriginZ`      The z coordinate of the origin of the plane, relatively to the father object.
` piNormalX`      The x coordinate of the normal vector of the plane, relatively to the father object.
` piNormalY`      The y coordinate of the normal vector of the plane, relatively to the father object.
` piNormalZ`      The z coordinate of the normal vector of the plane, relatively to the father object.
` piConstraintType`      The type of the constraint.
This parameter can take the values "Contact", "Contact2D", "Contact3D" or "Coincidence".

### Sub **SetTargetPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `piObject`,  double  `piCoordX`,  double  `piCoordY`,  double  `piCoordZ`)

   Set the target point to follow. This method establishes a **contact constraint** between the end effector and the point.

**Parameters:**

` piConstraintElement`      A reference to the target object
This target object must be the product (
CATIAProduct) associated with the constraint. ` piCoordX`      The x coordinate of the point, relatively to the father object.
` piCoordY`      The y coordinate of the point, relatively to the father object.
` piCoordZ`      The z coordinate of the point, relatively to the father object.

---

# SWKManikin (Object)

**_This interface groups the methods directly related to the definition of a manikin._**

Its main purpose is to provide bridges to the other interfaces related to a manikin.
Once these interfaces are recovered, it is possible to have access to their specific functionalities.

## Properties

### Property **Anthro**( ) As SWKIAAnthro (Read Only)

   Returns the anthropometry of the current manikin. The anthropometry can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "Anthro" as an argument.  
### Property **Body**( ) As SWKIABody (Read Only)

   Returns the body of the current manikin. The body can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "Body" as an argument.  
### Property **BodyNode**( ) As SWKIASegmentNode (Read Only)

   Returns the body node of the current manikin. The body node is the node named "Body", as it appears underneath the manikin in the specification tree. This body node can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "BodyNode" as an argument.  
### Property **Ergo**( ) As SWKIAErgo (Read Only)

   Returns the ergonomic analysis of the current manikin. The ergo can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "Ergo" as an argument.  
### Property **IKManager**( ) As SWKIAIKManager (Read Only)

   Returns the inverse kinematics (IK) engine of the current manikin. The IK manager can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "IKManager" as an argument.  
### Property **LineOfSightNode**( ) As SWKIALineOfSightNode (Read Only)

   Returns the Line of sight node of the current manikin. The Line of sight node can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "LineOfSightNode" as an argument.  
### Property **Move**( ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

   Returns the manikin's move object. The move object is aggregated by the manikin object and itself aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves the manikin's representation according to this isometry.

**Example:**      This example retrieves the move object for the manikin `myManikin`.

```VBScript
     Dim myManikinMoveObject As Move
     Set myManikinMoveObject = myManikin.Move

```

### Property **ProfilesNode**( ) As SWKIANode (Read Only)

   Returns the Profiles node of the current manikin. The Profiles node can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "ProfilesNode" as an argument.  
### Property **SettingsNode**( ) As SWKIANode (Read Only)

   Returns the settings node of the current manikin. The Settings node can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "SettingsNode" as an argument.  
### Property **Vision**( ) As SWKIAVision (Read Only)

   Returns the vision of the current manikin. The vision can also be obtained by invoking method GetItem (from `AnyObject`) with the character string "Vision" as an argument.

---

# SWKManikinPart (Object)

**_This interface represents any part of the manikin that is persistent._**

## Properties

### Property **Memo**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or records miscellaneous user-added information about the part.