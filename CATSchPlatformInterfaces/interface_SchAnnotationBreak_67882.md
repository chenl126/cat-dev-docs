# SchAnnotationBreak (Object)

**_Manage an annotation break operations._**

## Methods

### Sub **FlipOverLine**( )

Mirror the symbol over the route segment line that ends in the connector on which the symbol is placed.

**Example:**

```VBScript
Dim objThisIntf As SchAnnotationBreak
 ...
objThisIntf.FlipOverLine

```

### Sub **FlipOverOrthogonalLine**( )

Mirror the symbol over the line orthogonal to the route segment line that ends in the connector on which the symbol is placed and going through the connector's position.

**Example:**

```VBScript
Dim objThisIntf As SchAnnotationBreak
 ...
objThisIntf.FlipOverOrthogonalLine

```

### Sub **Scale**( double  `iDbScaleFactor`)

Scale the symbol.

**Parameters:**

` iDbScaleFactor`      The scale factor to scale the symbol by.
**Example:**

```VBScript
Dim objThisIntf As SchAnnotationBreak
Dim dbVar1 As Double
 ...
objThisIntf.ScaledbVar1

```