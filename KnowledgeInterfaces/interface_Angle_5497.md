# Angle (Object)

**_Represents the angle parameter._**
The following example shows how to create it:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim angle1 As Angle
     Set angle1  = part1.Parameters.CreateDimension("angle1", "ANGLE", 40.)

```