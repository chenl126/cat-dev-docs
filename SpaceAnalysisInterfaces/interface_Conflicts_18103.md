# Conflicts (Collection)

**_A collection of all Conflict objects currently detected by a Clash object._**

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iIndex`) As [CATIAConflict](../SpaceAnalysisInterfaces/interface_Conflict_14180.md)

   Returns a Conflict object using its index from the Conflicts collection.

**Parameters:**

` iIndex`      The index of the Conflict object to retrieve from the collection of Conflicts. As a numerics, this index is the rank of the Conflict in the collection. The index of the first Conflict in the collection is 1, and the index of the last Conflict is Count.

**Example:**      This example retrieves in `ThisConflict` the ninth Conflict from the `TheConflicts` collection.

```VBScript
        Dim ThisConflict As Conflict
        Set ThisConflict = TheConflicts.Item(9)

```