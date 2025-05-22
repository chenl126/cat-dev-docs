# Check (Object)

**_Represents the check relation._**
The following example shows how to create a check which checks if a given mass is less than 10kg. The mass should be defined previously:

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim mass As RealParam
Set mass         = part1.Part.Parameters.CreateReal("mass", 5.)
Dim maximummass As Check
Set maximummass = part1.Relations.CreateCheck
                   ("maximummass",
                    "Ensures that mass is less than 10 kg",
                    "mass<10kg")

```

## Properties

### Property **Diagnosis**( ) As boolean (Read Only)

Returns the check diagnosis. True if the condition of the check is verified. False otherwise.
```

### Property **Severity**( ) As long

Returns or sets the check severity. The severity is the way the check will manifest itself:
* Silent (1)
* Information (2)
* Warning (3)
```