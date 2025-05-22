# AngularRepartition (Object)

**_Represents the angular repartition._**
It is used by the circular pattern. It is made up of a number of times the shape is copied and of an angular spacing between two consecutive copies of the shape along a crown. The number of times the shape is copied is accessible using the [Repartition.InstancesCount](../PartInterfaces/interface_Repartition_27263.htm#InstancesCount) property.

**See also:**      [CircPattern](../PartInterfaces/interface_CircPattern_26301.md)

## Properties

### Property **AngularSpacing**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the angle between two consecutive copies of a shape along the repartition crown.

**Example:**     The following example returns in `AngSpace1` the angular spacing of the angular repartition `firstRepartition`:

```VBScript
Set AngSpace1 = firstRepartition.AngularSpacing

```

### Property **InstanceSpacing**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the angle at which the pattern spacing is done for unequal angular spacing mode.

**Example:**     The following example returns in `AngSpace1` the angular spacing of the angular repartition `firstRepartition`:

```VBScript
Set AngSpace1 = firstRepartition.AngularSpacing

```