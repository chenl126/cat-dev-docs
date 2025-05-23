# Conflict (Object)

**_Represents the Conflict object._**

One Conflict object exists for each couple of products that are colliding.

## Properties

### Property **Comment**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets a comment on the conflict.

**Example:**      The first example gets the comment of `NewConflict` Conflict.

```VBScript
        Dim aComment As String
        aComment = NewConflict.Comment

```

   The second example sets a comment on the `NewConflict` Conflict.

```VBScript
        NewConflict.Comment = "OK : plastic part"

```

### Property **ComparisonInfo**( ) As [CatConflictComparison](../SpaceAnalysisInterfaces/enum_CatConflictComparison_93987.md) (Read Only)

   Returns the information on the comparison between the conflict and the previous one.

**Example:**      This example retrieves the comparison information of the `NewConflict` Conflict.

```VBScript
        Dim anInfo As CatConflictComparison
        anInfo = NewConflict.ComparisonInfo

```

### Property **FirstProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the first product involved in the conflict.

**Example:**      This example retrieves the first product involved in the `NewConflict` Conflict.

```VBScript
        Dim aProduct As Product
        Set aProduct = NewConflict.FirstProduct

```

### Property **SecondProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the second product involved in the conflict.

**Example:**      This example retrieves the second product involved in the `NewConflict` Conflict.

```VBScript
        Dim aProduct As Product
        Set aProduct = NewConflict.SecondProduct

```

### Property **Status**( ) As [CatConflictStatus](../SpaceAnalysisInterfaces/enum_CatConflictStatus_62234.md)

   Returns or sets the status of the conflict.

**Example:**      The first example gets the status of `NewConflict` Conflict.

```VBScript
        Dim aStatus As CatConflictStatus
        aStatus = NewConflict.Status

```

   The second example sets the status of `NewConflict` Conflict.

```VBScript
        NewConflict.Status = CatConflictStatusIrrelevant

```

### Property **Type**( ) As [CatConflictType](../SpaceAnalysisInterfaces/enum_CatConflictType_47830.md) (Read Only)

   Returns the type of the conflict.

**Example:**      This example retrieves the type of the `NewConflict` Conflict.

```VBScript
        Dim conflictType As CatConflictType
        conflictType = NewConflict.Type

```

### Property **Value**( ) As double (Read Only)

   Returns the conflict value. This value is the penetration lengh in case of a clash or the minimum distance in case of clearance violation.

**Example:**      This example retrieves the value of the `NewConflict` Conflict.

```VBScript
        Dim conflictValue As double
        conflictValue = NewConflict.Value

```

Methods

### Sub **GetFirstPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point on the first product which realizes the penetration or minimum distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the first product involved in the `NewConflict` Conflict.

```VBScript
        Dim Coordinates (2)
        NewConflict.GetFirstPointCoordinates Coordinates

```

### Sub **GetSecondPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point on the second product which realizes the penetration or minimum distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the coordinates in the `NewConflict` Conflict.

```VBScript
        Dim Coordinates (2)
        NewConflict.GetSecondPointCoordinates Coordinates

```