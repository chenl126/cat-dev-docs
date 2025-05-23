# PspAttributeReport (Object)

**_Represents the Attribute Report._**

**Role** : To generate attributes report.

## Methods

### Func **GenerateReport**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iInputFormatFile`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iOutputfile`) As long

   Generate report (output format in html or CSV) and returns the status. It reports attribute data for all the selected objects in the document.

**Parameters:**

` iInputFormatFile`      Attribute report format filename. It should contain the directory path.

```VBScript
     Note:
       The format file is a text (.txt) file containing data in following
       order.
       Title=Title of the report
       TextFormat=HTML  or  TextFormat=CSV (Comma separated )
       Attrib=AttributeName likes Nominal size,EndStyle, Rating etc.
       Len=Integer value indicating length of attribute value
       and so on...
       Report format sample: Sample.txt
       Title=Piping parts report
       TextFormat=HTML
       Attrib=ID
       Len=15
       Attrib=Nominal size
       Len=10
       Attrib=Rating
       Len=10
       .... and so on

```

` iOutputfile`      Output filename. Full file name of the report output.

**Returns:**      0 or 1. **Legal values** :
`1 :` Report generation failed.
`0 :` Report generation succeeded.  **Example:**

```VBScript
     Dim objThisIntf As PspAttributeReport
     Dim strVar1 As CATBSTR
     Dim StrVar2 As CATBSTR
     Dim longRet    As Long
      ...
     olongRet = objThisIntf.GenerateReport (strVar1,strVar2 )

```