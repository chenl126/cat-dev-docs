# UserRepartition (Object)

**_Represents the User Pattern repartition._**
It is made up of a number of times the shape is copied and the location of instances. The number of times the shape is copied is accessible using the [Repartition.InstancesCount](../PartInterfaces/interface_Repartition_27263.htm#InstancesCount) property.

## Properties

### Property **FeatureToLocatePositions**(| ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the collection of feature to locate instances.

**Example:**     The following example returns in `list` the list of feature to locate instances of the Pattern `firstPattern`:

```VBScript
     Set list = firstPattern.FeatureToLocatePositions

```

Methods

### Sub **AddFeatureToLocatePositions**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFeatureToLocatePositions`)

   Adds a new feature to locate instances.

**Parameters:**

` iFeatureToLocatePositions`      The new face to process  **Example:**     The following example adds the new feature `feature` to locate instances of the Pattern `firstPattern`:

```VBScript
     call firstPattern.AddFeatureToLocatePositions(face)

```