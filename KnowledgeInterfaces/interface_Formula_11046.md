# Formula (Object)

**_Represents the formula relation._**
The following example shows how to create a formula that computes the mass of a cuboid, given its geometric dimensions and the density of the material it is made of:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim width As RealParam
     Set width        = part1.Part.Parameters.CreateReal("width", 1.)
     Dim height As RealParam
     Set height       = part1.Part.Parameters.CreateReal("height", 2.)
     Dim depth As RealParam
     Set depth        = part1.Part.Parameters.CreateReal("depth", 3.)
     Dim density As RealParam
     Set density      = part1.Part.Parameters.CreateReal("density", 1.5)
     Dim mass As RealParam
     Set mass         = part1.Part.Parameters.CreateReal("mass", 0.)
     Dim computemass As RealParam
     Set computemass = part1.Part.Relations.CreateFormula
                        ("computemass",
                         "Computes the cuboid mass",  mass,
                         "(width*height*depth)*density")

```