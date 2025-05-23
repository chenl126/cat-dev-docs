# BoolParam (Object)

**_Represents the boolean parameter._**
The following example shows how to create it:

```VBScript
    	Dim CATDocs As Documents
      Set CATDocs      = CATIA.Documents
    	Dim part1 As Document
      Set part1        = CATDocs.Add("CATPart")
    	Dim availability As BooleanParam
      Set availability = part1.Parameters.CreateBoolean("availability", True)

```

## Properties

### Property **Value**(| ) As boolean

   Returns or sets the value of the boolean parameter.

**Example:**      This example sets the `availability` boolean parameter value to True if its value is False:

```VBScript
     If (availability.Value = False)  Then
         availability.Value = True
     End If

```