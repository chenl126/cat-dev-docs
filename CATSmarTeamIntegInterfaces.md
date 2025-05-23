# CATSmarTeamIntegInterfaces Framework

## Object Index

  * [StiDBChildren](CATSmarTeamIntegInterfaces/interface_StiDBChildren_34351.md)
  * [StiDBItem](CATSmarTeamIntegInterfaces/interface_StiDBItem_16075.md)
  * [StiEngine](CATSmarTeamIntegInterfaces/interface_StiEngine_17314.md)

---

# StiDBItem (Object)

**_Represents the SmarTeam Integration Object, that is to say the Document coming from SmarTeam database._**

**Role** : It retrieves SmarTeam Document information. It is managed by [StiEngine](../CATSmarTeamIntegInterfaces/interface_StiEngine_17314.md).

**See also:**      [StiEngine](../CATSmarTeamIntegInterfaces/interface_StiEngine_17314.md)

## Methods

### Func **GetChildren**( ) As [CATIAStiDBChildren](../CATSmarTeamIntegInterfaces/interface_StiDBChildren_34351.md)

   Returns both all the Children of the CATIA Document -associated to the CATIAStiDBItem- and their corresponding Link Types with their Father CATIA Document.

**See also:**      [StiDBChildren](../CATSmarTeamIntegInterfaces/interface_StiDBChildren_34351.md) **Returns:**      This ouptut corresponds to the retrieved CATIAStiDBChildren from the Father CATIAStiDBItem.  **Example:**      The following example returns in `ochildrenList` both all the Children and their Link Types with their CATIAStiDBItem Father `oStiDBItem`.

```VBScript
     Dim oStiDBItem As StiDBItem
     Dim ochildrenList As StiDBChildren
     Set ochildrenList = oStiDBItem.GetChildren
     Dim lChildrenNumber As long
     lChildrenNumber = ochildrenList.Count
     For i = 1 To lChildrenNumber
        Dim oChildStiDBItem As StiDBItem
        Set oChildStiDBItem = ochildrenList.Item(i)
        Dim sChildLinkType As CATBSTR
        sChildLinkType = ochildrenList.LinkType(i)
     Next

```

### Func **GetDocument**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Returns the CATIA Document associated to the CATIAStiDBItem -the SmarTeam Integration Object.

**Returns:**      This ouptut corresponds to the retrieved CATIA Document.  **Example:**      The following example returns in `oDocument` the CATIA Document corresponding to the CATIAStiDBItem `oStiDBItem`.

```VBScript
     Dim oStiEngine As StiEngine
     Set oStiEngine = CATIA.GetItem("CAIEngine")
     Dim oStiDBItem As StiDBItem
     Set oStiDBItem = oStiEngine.GetStiDBItemFromCATBSTR("E:\CATIAFiles\Engine.CATProduct")
     Dim oDocument As Document
     Set oDocument = oStiDBItem.GetDocument

```

### Func **GetDocumentFullPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the Full Path of the CATIA Document associated to the CATIAStiDBItem.

**Returns:**      This ouptut corresponds to the retrieved Full Path of the CATIAStiDBItem.  **Example:**      The following example returns in `oFullPath` the full path corresponding to the CATIAStiDBItem `oStiDBItem`.

```VBScript
     Dim oStiDBItem As StiDBItem
     Dim oFullPath As string
     oFullPath = oStiDBItem.GetDocumentFullPath

```

### Func **IsCFOType**( ) As boolean

   Returns if the CATIA Document -associated to the CATIAStiDBItem- is a Component File or not.

**Returns:**      This ouptut corresponds to the boolean 'oIsCFOType'. 'oIsCFOType' is True when the CATIAStiDBItem is a Component File, False otherwise.  **Example:**      The following example tests if the CATIAStiDBItem is a Component File.

```VBScript
     Dim oStiEngine As StiEngine
     Set oStiEngine = CATIA.GetItem("CAIEngine")
     (...)
     Dim oIsCFOType As boolean
     oIsCFOType = oStiEngine.IsCFOType

```

### Func **IsRoot**( ) As boolean

   Returns if the CATIA Document -associated to the CATIAStiDBItem- is a Root. This method returns True if the Document is a Root, False otherwise.

**Returns:**      This ouptut corresponds to the boolean 'oIsRootCFO'.  **Example:**      The following example tests if the CATIAStiDBItem is a Root component file.

```VBScript
     Dim oStiEngine As StiEngine
     Set oStiEngine = CATIA.GetItem("CAIEngine")
     (...)
     Dim oIsRootCFO As boolean
     oIsRootCFO = oStiEngine.IsRoot

```