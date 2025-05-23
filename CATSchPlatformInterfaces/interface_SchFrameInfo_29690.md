# SchFrameInfo (Object)

**_Manage the background view of a schematic viewer._**

## Methods

### Sub **GetLabelCode**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oLabel`,| | boolean | `iBHoriz`)

   Get the frame label code.

**Parameters:**

` oLabel`      Label code.
` iBHoriz`      If TRUE, then the labels are for horizontal spacing, else, they are for vertical spacing.

**Example:**

```VBScript
     Dim objThisIntf As SchFrameInfo
     Dim strVar1 As String
     Dim bVar2 As boolean
      ...
     objThisIntf.GetLabelCodestrVar1,bVar2

```

### Sub **GetOriginCornerCode**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oOriginCorner`)

   Get the frame origin corner code.

**Parameters:**

` oOriginCorner`      Origin corner code.

**Example:**

```VBScript
     Dim objThisIntf As SchFrameInfo
     Dim strVar1 As String
      ...
     objThisIntf.GetOriginCornerCodestrVar1

```

### Sub **GetSpacingCode**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oSpacing`,  boolean  `iBHoriz`)

   Get the frame spacing code.

**Parameters:**

` oSpacing`      Spacing code.
` iBHoriz`      If TRUE, then the spacing is for horizontal, else, the spacing is for vertical.

**Example:**

```VBScript
     Dim objThisIntf As SchFrameInfo
     Dim strVar1 As String
     Dim bVar2 As boolean
      ...
     objThisIntf.GetSpacingCodestrVar1,bVar2

```

### Sub **SetLabelCode**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  boolean  `iBHoriz`)

   Set the frame label code.

**Parameters:**

` iLabel`      Label code.
` iBHoriz`      If TRUE, then the labels are for horizontal spacing, else, they are for vertical spacing.

**Example:**

```VBScript
     Dim objThisIntf As SchFrameInfo
     Dim strVar1 As String
     Dim bVar2 As boolean
      ...
     objThisIntf.SetLabelCodestrVar1,bVar2

```

### Sub **SetOriginCornerCode**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iOriginCorner`)

   Set the frame origin corner code.

**Parameters:**

` iOriginCorner`      Origin corner code.

**Example:**

```VBScript
     Dim objThisIntf As SchFrameInfo
     Dim strVar1 As String
      ...
     objThisIntf.SetOriginCornerCodestrVar1

```

### Sub **SetSpacingCode**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSpacing`,  boolean  `iBHoriz`)

   Set the frame spacing code.

**Parameters:**

` iSpacing`      Spacing code.
` iBHoriz`      If TRUE, then the spacing is for horizontal, else, the spacing is for vertical.

**Example:**

```VBScript
     Dim objThisIntf As SchFrameInfo
     Dim strVar1 As String
     Dim bVar2 As boolean
      ...
     objThisIntf.SetSpacingCodestrVar1,bVar2

```