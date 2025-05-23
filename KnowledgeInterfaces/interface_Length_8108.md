# Length (Object)

**_Represents the length parameter._**
The following example shows how to create it:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim Width As Length
     Set width   = part1.Part.Parameters.CreateDimension("width", "LENGTH", 20.)

```

By default the units are the default units of the IS of units.