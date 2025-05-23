# Shuttle (Object)

**_The interface to access a CATIAShuttle._**

**Role:** The shuttle object is used to define a grouping of products. Once products have been placed in the shuttle then they can be moved all at once. Also the shuttle has a base location defined by the shuttle axis.

## Properties

### Property **AngleLimit**(| ) As double

   Returns/Stores the angle limit attribute. **Role:/b> Retrieves/stores the shuttle's angle limit attribute. 
### Property **AngleValidation**( ) As boolean

   Returns/Stores the angle validation attribute. **Role:/b> Retrieves/stores the shuttle's angle validation attribute. 
### Property **Group**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns or sets the associated group object. **Role:/b> Retrieves/stores the objects within the shuttle as a group, that is a CATIAGroup. 
### Property **Move**( ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

   Returns the shuttle's move object. The move object is aggregated by the shuttle object and itself aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves your shuttle according to this isometry.

**Example:**      This example retrieves the move object for the `Engine` shuttle.

```VBScript
     Dim EngineMoveObject As Move
     Set EngineMoveObject = Engine.Move

```

### Property **MoveMode**( ) As [CatShuttleMoveMode](../FittingInterfaces/enum_CatShuttleMoveMode_67700.md)

   Returns/Stores the shuttle move mode. **Role:/b> Retrieves/stores the shuttle move mode. This can be either shuttle mode (to move the shuttle) or axis mode (to simply move the shuttle axis). 
### Property **Position**( ) As [CATIAPosition](../InfInterfaces/interface_Position_14692.md) (Read Only)

   Returns the shuttle's position object. The position object is the object aggregated by the ahuttle object that holds the position of the shuttle in the space.

**Example:**      This example retrieves the position object for the `Engine` shuttle.

```VBScript
     Dim EnginePositionObject As Position
     Set EnginePositionObject = Engine.Position

```

### Property **Reference**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns or sets the associated reference object. **Role:/b> Retrieves/stores the shuttle's reference object. 
### Property **SubShuttles**( ) As [CATIAShuttles](../FittingInterfaces/interface_Shuttles_14802.md) (Read Only)

   Returns any shuttles that are contained within the current shuttle. **Role:/b> Returns any shuttles that are contained within the current shuttle. 
### Property **Vector**( ) As [CatShuttleVector](../FittingInterfaces/enum_CatShuttleVector_55318.md)

   Returns/Stores the validation vector attribute. **Role:/b> Retrieves/stores the validation vector attribute.