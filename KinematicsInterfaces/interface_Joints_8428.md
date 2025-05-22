# Joints (Collection)

**_A collection of all Joint entities currently managed by the application._**

## Methods

### Func **Add**( ) As [CATIAJoint](../KinematicsInterfaces/interface_Joint_5842.md)

Create a new Joint and adds it to the Joints collection.

**Returns:**      The created Joint  **Example:**      This example creates a new Joint in the `TheJoints` collection.

```VBScript
   Dim NewJoint As Joint
   Set NewJoint = TheJoints.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAJoint](../KinematicsInterfaces/interface_Joint_5842.md)

Returns a Joint using its index or its name from the Joints collection.

**Parameters:**

` iIndex`      The index or the name of the Joint to retrieve from the collection of Joints. As a numerics, this index is the rank of the Joint in the collection. The index of the first Joint in the collection is 1, and the index of the last Joint is Count. As a string, it is the name you assigned to the Joint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Joint  **Example:**      This example returns in `ThisJoint` the third Joint in the collection, and in `ThatJoint` the Joint named `MyJoint`.

```VBScript
Dim ThisJoint As Joint
Set ThisJoint = TheJoints.Item(3)
Dim ThatJoint As Joint
Set ThatJoint = CATIA.Joints.Item("MyJoint")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Remove a Joint from the Joints collection.

**Parameters:**

` iIndex`      The index or the name of the Joint to retrieve from the collection of Joints. As a numerics, this index is the rank of the Joint in the collection. The index of the first Joint in the collection is 1, and the index of the last Joint is Count. As a string, it is the name you assigned to the Joint.
**Returns:**      Nothing  **Example:**      The following example removes the tenth Joint and the Joint named `JointTwo` from the `TheJoints` collection.

```VBScript
   TheJoints.Remove(10)
   TheJoints.Remove("JointTwo")

```