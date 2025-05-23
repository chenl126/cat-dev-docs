# Distance (Object)

**_Represents the Distance object._**
The Distance object is a specification of a distance computation between products or groups of products.

## Properties

### Property **Accuracy**(| ) As double

   Returns or sets the accuracy value for the computation. The accuracy value must be greater than 0.

**Example:**      The first example retrieves the accuracy value of `NewDistance` Distance.

```VBScript
        Dim AccuracyValue As double
        AccuracyValue = NewDistance.Accuracy

```

   The second example sets the accuracy value of `NewDistance` Distance.

```VBScript
        NewDistance.Accuracy = 10.

```

### Property **AnnotatedViews**( ) As [CATIAAnnotatedViews](../NavigatorInterfaces/interface_AnnotatedViews_42578.md) (Read Only)

   Returns the AnnotatedViews collection of the distance.

**Example:**      This example retrieves the AnnotatedViews collection of `NewDistance` Distance.

```VBScript
        Dim TheAnnotatedViewsList As AnnotatedViews
        Set TheAnnotatedViewsList = NewDistance.AnnotatedViews

```

### Property **ComputationType**( ) As [CatDistanceComputationType](../SpaceAnalysisInterfaces/enum_CatDistanceComputationType_143950.md)

   Returns or sets the computation type for the computation.

**Example:**      The first example retrieves the computation type of `NewDistance` Distance.

```VBScript
        Dim ComputationType As CatDistanceComputationType
        ComputationType = NewDistance.ComputationType

```

   The second example sets the computation type of `NewDistance` Distance.

```VBScript
        NewDistance.ComputationType = CatDistanceComputationTypeInsideOne

```

### Property **FirstGroup**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns or sets the first group used by the computation.

**Example:**      The first example retrieves the first group of `NewDistance` Distance.

```VBScript
        Dim FirstGroup As Group
        Set FirstGroup = NewDistance.FirstGroup

```

   The second example sets the first group of `NewDistance` Distance.

```VBScript
        Dim FirstGroup As Group
        NewDistance.FirstGroup = FirstGroup

```

### Property **FirstProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the product belonging to the first group that realizes the minimum distance.

**Example:**      This example retrieves the first product involved in the `NewDistance` Distance.

```VBScript
        Dim AProduct As Product
        Set AProduct = NewDistance.FirstProduct

```

### Property **IsDefined**( ) As long (Read Only)

   Returns a diagnosis on the distance. The diagnosis can take two values:

  * = 0: the distance is undefined (for example only one product) and the results are invalid.
  * = 1: the distance is defined and all results are valid.

**Example:**      This example retrieves the diagnosis on `NewDistance` Distance.

```VBScript
        If NewDistance.IsDefined = 1 Then

```

### Property **Marker3Ds**( ) As [CATIAMarker3Ds](../NavigatorInterfaces/interface_Marker3Ds_15928.md) (Read Only)

   Returns the Marker3Ds collection of the distance.

**Example:**      This example retrieves the Marker3Ds collection of `NewDistance` Distance.

```VBScript
        Dim TheMarker3DsList As Marker3Ds
        Set TheMarker3DsList = NewDistance.Marker3Ds

```

### Property **MaximumDistance**( ) As double

   Returns or sets the maximum distance value for the computation (valid only for band analysis). The maximum distance value must be greater than 0.

**Example:**      The first example retrieves the maximum distance value of `NewDistance` Distance.

```VBScript
        Dim MaximumValue As double
        MaximumValue = NewDistance.MaximumDistance

```

   The second example sets the maximum distance value of `NewDistance` Distance.

```VBScript
        NewDistance.MaximumDistance = 10.

```

### Property **MeasureType**( ) As [CatDistanceMeasureType](../SpaceAnalysisInterfaces/enum_CatDistanceMeasureType_101708.md)

   Returns or sets the type of distance that will be calculated.

**Example:**      The first example retrieves the type of `NewDistance` Distance.

```VBScript
        Dim MeasureType As CatDistanceMeasureType
        MeasureType = NewDistance.MeasureType

```

   The second example sets the Type of `NewDistance` Distance.

```VBScript
        NewDistance.MeasureType = CatDistanceMeasureTypeMinimum

```

### Property **MinimumDistance**( ) As double

   Returns or sets the minimum distance value for the computation (valid only for band analysis). The minimum distance value must be greater than 0.

**Example:**      The first example retrieves the minimum distance value of `NewDistance` Distance.

```VBScript
        Dim MinimumValue As double
        MinimumValue = NewDistance.MinimumDistance

```

   The second example sets the minimum distance value of `NewDistance` Distance.

```VBScript
        NewDistance.MinimumDistance = 10.

```

### Property **SecondGroup**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns or sets the second group used by the computation.

**Example:**      The first example retrieves the second group of `NewDistance` Distance.

```VBScript
        Dim SecondGroup As Group
        Set SecondGroup = NewDistance.SecondGroup

```

   The second example sets the second group of `NewDistance` Distance.

```VBScript
        Dim SecondGroup As Group
        NewDistance.SecondGroup = SecondGroup

```

### Property **SecondProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the product belonging to the second group that realizes the minimum distance.

**Example:**      This example retrieves the coordinates in the `NewDistance` Distance.

```VBScript
        Dim AProduct As Product
        Set AProduct = NewDistance.SecondProduct

```

### Property **Value**( ) As double (Read Only)

   Returns the distance value.

**Example:**      This example retrieves the value of `NewDistance` Distance.

```VBScript
        Dim MinimumValue As double
        MinimumValue = NewDistance.Value

```

Methods

### Sub **Compute**( )

   Computes the distance.

**Example:**      This example computes the distance of `NewDistance` Distance.

```VBScript
        NewDistance.Compute

```

### Sub **GetFirstPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point belonging to the first product, which realizes the distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the coordinates of the first point in `NewDistance` Distance.

```VBScript
        Dim Coordinates (2)
        NewDistance.GetFirstPointCoordinates Coordinates

```

### Sub **GetSecondPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point belonging to the second product, which realizes the distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the coordinates of the first point in `NewDistance` Distance.

```VBScript
        Dim Coordinates (2)
        NewDistance.GetSecondPointCoordinates Coordinates

```