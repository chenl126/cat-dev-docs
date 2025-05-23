# LinearRepartition (Object)

**_Represents the linear repartition._**
It is used by the rectangular and circular patterns. It is made up of a number of times the shape is copied and of a spacing distance between two consecutive copies of this shape along a direction. The number of times the shape is copied is accessible using the [Repartition.InstancesCount](../PartInterfaces/interface_Repartition_27263.htm#InstancesCount) property.

**See also:**      [RectPattern](../PartInterfaces/interface_RectPattern_26504.md), [CircPattern](../PartInterfaces/interface_CircPattern_26301.md)

## Properties

### Property **Spacing**(| ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the distance between two consecutive shapes along the repartition direction.

**Example:**     The following example returns in `space1` the spacing distance of the linear repartition `firstRepartition`:

```VBScript
     Set space1 = firstRepartition.Spacing

```