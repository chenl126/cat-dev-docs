# Inertia (Object)

**_Represents the Inertia object._**
The Inertia object can be associated with any relevant object of a document in order to get or compute its inertia data.

This version allows you to compute the following data:

  * mass
  * density
  * position of the center of gravity
  * inertia matrix
  * principal axes
  * principal moments
of a product.

The units are:

  * Kilogram (Kg) for Mass
  * Square meter (M^2) for Wet Area
  * Cubic meter (M^3) for Volume
  * Meter (M) for Position
  * Square Kilogram meter ((KgM)^2) for Inertia Matrix and Principal Moments
  * Kilogram per cubic meter (Kg/M^3) for Density

The method `GetTechnologicalObject("Inertia")` on the product to analyze, allows you to retrieve this object.

## Properties

### Property **Density**( ) As double

Returns or sets the density for the computation. The density value is set to:

  * 0: the computation must use densities attached to each object.
  * any positive value: the computation has to use this value.
The density value is returned as:

  * 1: a default value is used (there is no density attached to objects).
  * -1: the density is not homogeneous for each object.
  * other positive values: the density attached to all objects.

**Example:**      The first example gets the density of `NewInertia` inertia.

```VBScript
   Dim ADensity As double
   ADensity = NewInertia.Density

```

The second example sets the density of `NewInertia` inertia.

```VBScript
   NewInertia.Density = 10.

```

### Property **Mass**( ) As double (Read Only)

Returns the mass.

**Example:**      This example retrieves the mass of `NewInertia` inertia.

```VBScript
   Dim AMass As double
   AMass = NewInertia.Mass

```

Methods

### Sub **GetCOGPosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

Retrieves the position of the center of gravity.

**Parameters:**

` oCoordinates`      The position of the center of gravity with respect to the product coordinate system:

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the position of the center of gravity of `NewInertia` inertia.

```VBScript
   Dim Coordinates (2)
   NewInertia.GetCOGPosition Coordinates

```

### Sub **GetInertiaMatrix**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oMatrix`)

Retrieves the matrix of inertia.

**Parameters:**

` oMatrix`      The matrix of inertia array:

  * oMatrix(0) is the Ixx component
  * oMatrix(1) is the Ixy component
  * oMatrix(2) is the Ixz component
  * oMatrix(3) is the Iyx component
  * oMatrix(4) is the Iyy component
  * oMatrix(5) is the Iyz component
  * oMatrix(6) is the Izx component
  * oMatrix(7) is the Izy component
  * oMatrix(8) is the Izz component

**Example:**      This example retrieves the matrix of inertia of `NewInertia` inertia.

```VBScript
   Dim Matrix (8)
   NewInertia.GetInertiaMatrix Matrix

```

### Sub **GetPrincipalAxes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oComponents`)

Retrieves the the principal axes of inertia.

**Parameters:**

` oComponents`      The principal axes of inertia array (A1, A2 and A3 are the principal axes of inertia):

  * oComponents(0) is the A1x component
  * oComponents(1) is the A2x component
  * oComponents(2) is the A3x component
  * oComponents(3) is the A1y component
  * oComponents(4) is the A2y component
  * oComponents(5) is the A3y component
  * oComponents(6) is the A1z component
  * oComponents(7) is the A2z component
  * oComponents(8) is the A3z component

**Example:**      This example retrieves the principal axes of inertia of `NewInertia` inertia.

```VBScript
   Dim Components (8)
   NewInertia.GetPrincipalAxes Components

```

### Sub **GetPrincipalMoments**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oValues`)

Retrieves the principal moments of inertia.

**Parameters:**

` oValues`      The principal moments of inertia array:

  * oValues(0) is the M1 value with respect to the first principal exes of inertia
  * oValues(1) is the M2 value with respect to the second principal exes of inertia
  * oValues(2) is the M3 value with respect to the third principal exes of inertia

**Example:**      This example retrieves principal moments of inertia of `NewInertia` inertia.

```VBScript
   Dim Values (2)
   NewInertia.GetPrincipalMoments Values

```