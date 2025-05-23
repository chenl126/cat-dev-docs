# PspLogicalLine (Object)

**_Represents the logical line._**

**Role** : To query the logical line object's from/to members.

## Methods

### Sub **GetFromTo**(| [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) | `oListFromMajor`,| | [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) | `oListFromMinor`,| | [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) | `oListToMajor`,| | [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) | `oListToMinor`)

   Retrieves the lists of major and minor from/to members from this line.
The members retrieved are all [PspGroupable](../CATPlantShipInterfaces/interface_PspGroupable_31100.md) objects.

**Parameters:**

` oListFromMajor`      The list of major from members
` oListFromMinor`      The list of minor from members
` oListToMajor`      The list of major to members
` oListToMinor`      The list of minor to members

**Example:**

```VBScript
     Dim objThisIntf As PspLogicalLine
     Dim objArg1 As PspListOfObjects
     Dim objArg2 As PspListOfObjects
     Dim objArg3 As PspListOfObjects
     Dim objArg4 As PspListOfObjects
     ...
     objThisIntf.GetFromTo objArg1, objArg2, objArg3, objArg4

```

### Func **GetFromToInfoArrayMaxSize**( ) As long

   Returns the maximum possible size of the from-to information.

**Returns:**      The maximum possible size of the array to hold the information returned by GetFromToInformation **Example:**

```VBScript
     Dim objThisIntf As PspLogicalLine
     Dim intValueMaxSize As Integer
     ...
     intValueMaxSize = objThisIntf.GetFromToInfoArrayMaxSize

```

### Sub **GetFromToInformation**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFromToLabel`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFTMajor`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFTMinor`,  long  `oSizeOfOutput`)

   Retrieves the from/to information of a logical line.

**Parameters:**

` oFromToLabel`      The array of labels ("From" or "To")
` oFTMajor`      The array of from/to major IDs
` oFTMinor`      The array of from/to minor IDs
` The`      size of the output arrays

**Example:**

```VBScript
     Dim objThisIntf As PspLogicalLine
     Dim strFromToLabel(20) As String
     Dim strFromToMajor(20) As String
     Dim strFromToMinor(20) As String
     Dim intValueMaxSize As Integer
     intValueMaxSize = objThisIntf.GetFromToInfoArrayMaxSize
     ...
     '----  make sure the array size if big enough
     If (intValueMaxSize ≤ 20)  Then
        objThisIntf.GetFromToInformation _
          strFromToLabel, strFromToMajor, strFromToMinor, intValueMaxSize
     End If

     The following table can then be filled with the output arrays.

        From/To        |   F/T Major       |    F/T Minor
     strFromToLabel(i) | strFromToMajor(i) |  strFromToMinor(i)

```