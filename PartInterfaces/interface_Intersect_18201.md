# Intersect (Object)

**_Represents the intersect boolean operation._**
It is performed between a body and the current shape.

**Example**

The following example shows how to create a new shape by intersecting two existing pads `Pad1` and `Pad2`, created in two different bodies `Body1` and `Body2` respectively, using the existing shape factory named `shapeFactory`.

```VBScript
' Make Pad1 the current shape
CATIA.ActiveDocument.Part.CurrentShape = Pad1
'
' Create the intersection between Pad1 and Body2
Set NewShape      = shapeFactory.AddNewIntersect(Body2)

```