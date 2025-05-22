# LicenseSettingAtt (Object)

**_Interface to handle the licensing settings._**
**Role** : This interface is implemented by a component which represents the controller of the static Licenses.
To access this property page:
* Click the Options command in the Tools menu
* Click General
* Click the Licensing Property Page

This interface defines:
* A method to set each License
* A method to get the value of each License
* A method to lock/unlock each parameter
* A method to retrieve the information concerning each parameter

## Properties

### Property **DemoMode**( ) As boolean

Retrieves or Sets the demo mode.
**Role** : Retrieves or sets the value of the parameter describing if the demo mode is active.  
### Property **Frequency**( ) As float

Retrieves or Sets the contact frequency.
**Role** : Retrieves or sets the value of the parameter describing the server contact frequency in minutes. Note that a null value represents the maximum contact frequency value. For more information about the range and maximum, refers to the Infrastructure documentation.  
### Property **NodelockAlert**( ) As long

Retrieves or Sets the license expiry alert.
**Role** : Retrieves or sets the value of the parameter describing the lthe license expiry alertt in days. For more information about the range and maximum, refers to the Infrastructure documentation.  
### Property **ServerTimeOut**( ) As float

Retrieves or Sets the server time out.
**Role** : Retrieves or sets the value of the parameter describing the licensing server time out in minutes. For more information about the range and maximum, refers to the Infrastructure documentation.  
### Property **ShowLicense**( ) As boolean

Retrieves or Sets the show license .
**Role** : Retrieves or sets the value of the parameter describing the complete license information. When the parameter is set, the user gets more information about the reason of the failure to request a license.  Methods

### Func **GetDemoModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DemoMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFrequencyInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the Frequency setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGrantedLicensesList**( long  `iDefaultLicenses`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

**Deprecated:**      V5R15 CATSysLicenseSettingAtt#GetLicensesList  
### Func **GetLicense**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLicense`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves the value of the license.
**Role** : Retrieves the mapping between a name of a license and the value of the license. The license does not need to be returned by GetLicensesList(). But if the license is not installed the license will be "NotRequested"

**Parameters:**

` iLicense`      the name of the License: "PMG.prd", "_MD2.slt+", "_MD2.slt+GSD" for example.
"PMG.prd" represent the license of the product PMG.
"_MD2.slt+" represent the license of the solution MD2.
"_MD2.slt+GSD" represent the license of the solution MD2, with the AddOn product GSD.
**Returns:**      the value of the License:
` NotRequested :` License is not Requested
` key :` the name of the license, the default available license has been chosen by the user. License is Requested.
` License Number :` a specific license number has been chosen by the user. License is Requested.  
### Func **GetLicenseInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLicense`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the License setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLicensesList**( long  `iDefaultLicenses`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Retrieves the list of the requested or locked licenses.
**Role** : Retrieves the list of the requested or locked licenses. There is no SetLicensesList() because the list is initialized using LUM.

**Parameters:**

` iDefaultLicenses`      If iDefaultLicenses!=0 and the settings are empty, returns the default licenses, that is, the visible nodolocked licenses. If iDefaultLicenses == 0 and the settings are empty, returns the selected licenses (not yet stored, because not yet validated by OK button).
**Returns:**
* The array of Licenses.
* character meaning in license name:
* "_": internal notation for a license configuration
* "+": you chose "Any license" mode, example of returned value: _ME1.slt+FS1
* When the return value is a serial number (_ME1.slt_SerialNumber), you have chosen the "Explicit" license mode. In this case the add on product is not indicated in the license name.

### Func **GetLicensesListInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLock`) As boolean

Retrieves information about the LicensesList setting parameter.
**Role** : Retrieves information about the LicensesList setting locking state (global lock for the LicensesList). It is used to get the lock status of the List of the Licenses. If the LicensesList is locked all the licenses are locked. When the licenses are locked, it means that an administrator has locked the attribute. It does not means that an administrator has changed the value of the attribute. The value of the setting is not updatable because it refers to a lock on a list. That is why the return value is false.

**Parameters:**

` ioAdminLevel:`      Level of administrator.
` ioLock:`      Locked/Unlocked.
**Returns:**      False
Information returned in the dump:
* Parameter 1 : "Value taken in case of reset" : useless. Default value : "Default value"
* Parameter 2 : "Locking state" value : unlocked / locked / locked at Admin Level n
* Parameter 3 : "Returned value" : useless, default value : False

Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetNodelockAlertInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the license expiry alert setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetServerTimeOutInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the TimeOut setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetShowLicenseInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the ShowLicense setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDemoModeLock**( boolean  `iLock`)

Locks or unlocks the DemoMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFrequencyLock**( boolean  `iLock`)

Locks or unlocks the Frequency setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLicense**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLicense`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`)

Sets the License.
**Role** : Sets the value of the license.

**Parameters:**

` iLicense`      the name of the License: "PMG.prd", "_MD2.slt+", "_MD2.slt+GSD" for example.
"PMG.prd" represent the license of the product PMG.
"_MD2.slt+" represent the license of the solution MD2.
"_MD2.slt+GSD" represent the license of the solution MD2, with the AddOn product GSD.
` iValue`
the value of the License:
` NotRequested :` License is not Requested
` key :` the name of the license, the default available license has been chosen by the user. License is Requested.
` License Number :` a specific license number has been chosen by the user. License is Requested.

### Sub **SetLicenseLock**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLicense`,  boolean  `iLock`)

Locks or unlocks the License setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLicensesListLock**( boolean  `iLock`)

Locks or unlocks the LicensesList setting parameter.
**Role** :Locks or unlocks the LicensesList setting parameter. Locks or unlocks the parameter describing the list of installed licenses, if the operation is allowed in the current administrated environment. It is the global lock on all the licenses. When the LicenseList is locked all the licenses are locked. When the LicenseList is unlocked all the licenses are unlocked.

**Parameters:**

` iLock`      the locking operation to be performed:
`True:` to lock the parameter.
`False:` to unlock the parameter.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetNodelockAlertLock**( boolean  `iLock`)

Locks or unlocks the license expiry alert setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetServerTimeOutLock**( boolean  `iLock`)

Locks or unlocks the TimeOut setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetShowLicenseLock**( boolean  `iLock`)

Locks or unlocks the ShowLicense setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.