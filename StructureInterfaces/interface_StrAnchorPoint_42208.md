# StrAnchorPoint (Object)

**_Represents an anchor point._**
An anchor point is a point used to place the section on the support in the design model.

## Methods

### Sub **GetCoordinates**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `oCoord`)

   Retrieves the coordinates of the anchor point. These coordinates are expressed in the section local coordinate system.

**Parameters:**

` oCoord`      The 2D coordinates of the anchor point.

**Example:**

```VBScript
     Dim coord(1)
     anchor_1.GetCoordinates(coord)

```