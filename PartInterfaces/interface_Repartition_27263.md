# Repartition (Object)

**_Represents the repartition._**
A repartition is a set of objects used by the pattern shapes. It is the base object for linear and angular repartitions.

**See also:**      [LinearRepartition](../PartInterfaces/interface_LinearRepartition_62934.md), [AngularRepartition](../PartInterfaces/interface_AngularRepartition_70628.md)

## Properties

### Property **InstancesCount**(| ) As [CATIAIntParam](../KnowledgeInterfaces/interface_IntParam_13730.md) (Read Only)

   Returns the total number of copied shapes.

**Example:**     The following example returns in `Nb` the number of shapes of the repartition `firstRepartition`:

```VBScript
     Set Nb = firstRepartition.InstancesCount

```