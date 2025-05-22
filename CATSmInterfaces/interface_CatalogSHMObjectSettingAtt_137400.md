# CatalogSHMObjectSettingAtt (Object)

**_Represents the CATIA Sheet Metal Aerospace General setting controller object._**
**Role** : The CATIA Sheet Metal Aerospace setting General controller object deals with the setting attributes displayed in the Aerospace Sheet Metal Design General property page. To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **Mechanical Design** to unfold the workbench list
  * Click **General**

The Sheet Metal Aerospace General setting controller object can be retrieved as an item of the setting controller collection using its name "CATIStmCatalogSHMObjectSettingCtrl" as follows:

```VBScript
Dim settingControllers1 As SettingControllers
Set settingControllers1 = CATIA.SettingControllers
Dim CATIAStmCatalogSHMObjectSettingAtt1 As SettingController
Set CATIAStmCatalogSHMObjectSettingAtt1 = settingControllers1.Item("CATIStmCatalogSHMObjectSettingCtrl")

```

## Properties

### Property **SHMStdProfPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the SHMStdProfPath setting parameter value.
**Role** : The SHMStdProfPath setting parameter stores the path to the CATIA Catalog file used by the Catalog Browser whenever it is involved in Aerospace Sheet Metal commands, such as cutout or corner relief.
**Legal values** : a valid path to a CATIA Catalog file.  Methods

### Func **GetSHMStdProfPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the SHMStdProfPath setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMStdProfPathLock**( boolean  `iLocked`)

Locks or unlocks the SHMStdProfPath setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.