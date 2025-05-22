# Rule (Object)

**_Represents the program relation._**
The following example shows how to create a program that selects a depth with respect to a mass value. The depth and mass parameters should exist before the creation of the program (also called Rule) object.

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim mass As RealParam
Set mass         = part1.Part.Parameters.CreateReal("mass", 5.)
Dim depth As RealParam
Set depth        = part1.Part.Parameters.CreateReal("depth", 0.)
Dim selectdepth As Relation
Set selectdepth = part1.Part.Relations.CreateProgram
                   ("select_depth",
                    "Select depth with respect to mass",
                    "if (mass>2kg) { depth=2mm } else { depth=1mm }")

```