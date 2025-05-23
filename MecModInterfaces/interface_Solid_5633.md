# Solid (Object)

**_Represents an imported solid object._**

**Role** : the imported solid is a solid obtained from copy/paste with link or design in context.
The solid object has a link to a source element obtained from SourceElement and a source product obtained from SourceProduct .

## Properties

### Property **Move**(| ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

   Returns the move object of the solid.

**Role** : The move object is aggregated by the solid object and itself aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves the solid according to this isometry.

**Example:**      This example retrieves the move object `EngineMoveObject` for the `Engine` product.

```VBScript
     Dim EngineMoveObject As Move
     Set EngineMoveObject = Engine.Move

```

**See also:**      [Move](../InfInterfaces/interface_Move_3742.md) 
### Property **SourceElement**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the source element of the imported solid.

**Role** : returns the linked element in the source part.

**Example:**     The following example returns in `element` the source element of the imported solid `importedSolid`:

```VBScript
     Set element = importedSolid.SourceElement

```

### Property **SourceProduct**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the source product instance of the imported solid.

**Role** : returns the product instance which was selected when the import was created.

**Example:**     The following example returns in `prod1` the source product instance of the imported solid `importedSolid`:

```VBScript
     Set prod1 = importedSolid.SourceProduct

```