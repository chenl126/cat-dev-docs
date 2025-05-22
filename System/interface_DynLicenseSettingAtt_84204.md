# DynLicenseSettingAtt (Object)

**_Interface to handle the dynamic licensing settings._**
**Role** : This interface is implemented by a component which represents the controller of the dynamic Licenses.
To access this property page:
* Click the Options command in the Tools menu
* Click General
* Click the Shareable Products Property Page

This interface defines:
* A method to lock/unlock each parameter
* A method to retrieve the information concerning each parameter
* Note that when a license is selected, no information is written in the settings, only the lock status is written in the settings.

## Methods

### Func **GetLicense**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLicense`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

The method is not relevant for the settings.
**Role** : The method is not relevant for the settings, because a dynamic license is only taken in account for the current session. That is why GetLicense() does not appears in the dump, even when GetLicenseInfo() appears. The output oValue will always be "".

**Parameters:**

` iLicense`      the name of the License.
**Returns:**      the value of the License.
` License "" ` 
### Func **GetLicenseInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLicense`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves the state of a given License.
**Role** : Retrieves the state of a given License. It it is used to get the lock status of a specific license. When the license is locked, it means that an administrator has locked the attribute. It does not means that an administrator has changed the value of the license.

**Parameters:**

` iLicense:`      the name of the License.
` ioAdminLevel:`      Level of administrator.
` ioLocked:`      Locked/Unlocked.
**Returns:**      False.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.
Dump information:
* Parameter 1 : the name of the License.
* Parameter 2 : "Default value".
* Parameter 3 : locking state of the licenses Unlocked / Locked / Locked at Admin Level j.
* Return value : Always false, because the status of the license is not modified, only the lock status is modified.  
### Func **GetLicensesList**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Retrieves the List of the Licenses.
**Role** : Retrieves the list of the locked Licenses. There is no SetLicenseList() because the list is initialized using LUM.

**Returns:**
* The array of Licenses.  
### Func **GetLicensesListInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the LicensesList setting locking state (global lock for the LicensesList).
**Role** : Retrieves information about the LicensesList setting locking state (global lock for the LicensesList) It is used to get the lock status of the List of the Licenses. If the LicenseList is locked all the licenses are locked. When the licenses are locked, it means that an administrator has locked the attribute. It does not means that an administrator has changed the value of the attribute. The value of the setting is not updatable because it refers to a lock on a list. That is why the return value is false.

**Parameters:**

` ioAdminLevel:`      Level of administrator.
` ioLocked:`      Locked/Unlocked.
**Returns:**      False.

* Parameter values in dump:
* Parameter 1 : "Value taken in case of reset" : useless. Default value: "Default value".
* Parameter 2 : "Locking state" value : unlocked / locked / locked at Admin Level n
* Parameter 3 : "Returned value" : useless, default value : False

Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLicenseLock**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLicense`,  boolean  `iLock`)

Locks or unlocks the License setting parameter.
**Role** : Locks or unlocks the given License if the operation is allowed in the current administrated environment.

**Parameters:**

` iLicense:`      the name of the License.
` iLock`      the locking operation to be performed:
`True:` to lock the parameter.
`False:` to unlock the parameter.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLicensesListLock**( boolean  `iLock`)

Locks or unlocks the LicensesList setting parameter.
**Role** : Locks or unlocks the parameter describing the list of installed licenses, if the operation is allowed in the current administrated environment. When the LicenseList is locked all the licenses are locked. When the LicenseList is unlocked all the licenses are unlocked.

**Parameters:**

` iLock`      the locking operation to be performed:
`True:` to lock the parameter.
`False:` to unlock the parameter.
Refer to
[SettingController](../System/interface_SettingController_63320.md) for a detailed description.