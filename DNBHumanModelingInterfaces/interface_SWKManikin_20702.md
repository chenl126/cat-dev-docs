# SWKManikin (Object)

**_This interface groups the methods directly related to the definition of a manikin._**

Its main purpose is to provide bridges to the other interfaces related to a manikin.
Once these interfaces are recovered, it is possible to have access to their specific functionalities.

## Properties

### Property **Anthro**(| ) As SWKIAAnthro (Read Only)

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