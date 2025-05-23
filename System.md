# System Framework

## Object Index

  * [AccesslogStatisticsSettingAtt](System/interface_AccesslogStatisticsSettingAtt_178800.md)
  * [AnyObject](System/interface_AnyObject_17321.md)
  * [CATBaseDispatch](System/interface_CATBaseDispatch_45333.md)
  * [CATBaseUnknown](System/interface_CATBaseUnknown_40786.md)
  * [CacheSettingAtt](System/interface_CacheSettingAtt_47207.md)
  * [Collection](System/interface_Collection_22150.md)
  * [CommandStatisticsSettingAtt](System/interface_CommandStatisticsSettingAtt_154823.md)
  * [DLNameSettingAtt](System/interface_DLNameSettingAtt_52772.md)
  * [DisconnectionSettingAtt](System/interface_DisconnectionSettingAtt_112813.md)
  * [DynLicenseSettingAtt](System/interface_DynLicenseSettingAtt_84204.md)
  * [ErrorlogStatisticsSettingAtt](System/interface_ErrorlogStatisticsSettingAtt_167778.md)
  * [GeneralStatisticsSettingAtt](System/interface_GeneralStatisticsSettingAtt_154832.md)
  * [GlobalStatisticsSettingAtt](System/interface_GlobalStatisticsSettingAtt_143462.md)
  * [IDispatch](System/interface_IDispatch_17333.md)
  * [IUnknown](System/interface_IUnknown_14460.md)
  * [LicenseSettingAtt](System/interface_LicenseSettingAtt_61302.md)
  * [MemoryWarningSettingAtt](System/interface_MemoryWarningSettingAtt_112572.md)
  * [PCSStatisticsSettingAtt](System/interface_PCSStatisticsSettingAtt_111088.md)
  * [ServerStatisticsSettingAtt](System/interface_ServerStatisticsSettingAtt_144736.md)
  * [SessionStatisticsSettingAtt](System/interface_SessionStatisticsSettingAtt_156130.md)
  * [SettingController](System/interface_SettingController_63320.md)
  * [SystemService](System/interface_SystemService_36846.md)
  * [WorkbenchStatisticsSettingAtt](System/interface_WorkbenchStatisticsSettingAtt_178981.md)

## Enumerated Types Index

  * [CATScriptLanguage](System/enum_CATScriptLanguage_59191.md)
  * [CatScriptLibraryType](System/enum_CatScriptLibraryType_85292.md)

## Typedef Index

  * [CATBSTR](System/typedef_CATBSTR_8129.md)
  * [CATSafeArrayVariant](System/typedef_CATSafeArrayVariant_73843.md)
  * [CATVariant](System/typedef_CATVariant_20656.md)

---

# CATScriptLanguage (Enumeration)

**_Types of macro libraries defined in the V5 architecture._**

**Values:**

` CATVBScriptLanguage`      VB Script language.
` CATVBALanguage`      VBA language.
` CATBasicScriptLanguage`      BasicScript language.
` CATJavaLanguage`      Java language.
` CATJScriptLanguage`      JScript language. (reserved for future use)

---

# CatScriptLibraryType (Enumeration)

**_Types of macro libraries defined in the V5 architecture._**

**Values:**

` catScriptLibraryTypeDocument`
` catScriptLibraryTypeDirectory`
` catScriptLibraryTypeVBAProject`

---

# AccesslogStatisticsSettingAtt (Object)

**_Interface for Accesslog statistic Controler._**

**Role** : the accesslog statistics controler manages the values of all or only a part of the attributes available for the thematic.**
For the definitions of methods and variables common to every thematic, see the [GeneralStatisticsSettingAtt](../System/interface_GeneralStatisticsSettingAtt_154832.md).

---

# AnyObject (Object)

**_Represents the base object for all other objects except collection and reference objects._**
As a base object, it provides properties shared by any other object.

## Properties

### Property **Application**( ) As [CATIAApplication](../InfInterfaces/interface_Application_26636.md) (Read Only)

   Returns the application. The application is the root object of the object structure and can be retrieved from any object in this object structure using the Application property. The root object, also called top-level object, is the object located at the top of the application's object structure. It is used by clients to retrieve and navigate across all the application's subordinate objects. If the client runs in-process, it retrieves the object at the top of the object structure. If the client runs out-process, it should call the GetApplication method to retrieve the object at the top of the object structure, which is the only object accessible from outside. The Application property is thus the way to jump from any object up to the root of the object structure, allowing then to navigate downwards. For in-process scripting, the application is always referred to as `CATIA`. Note that the Application property of the Application object returns the Application object itself.

**Example:**      This example retrieves in `CurrentApplication` the application object, root of the object structure, from a given object of this structure: a document refered to using the `MyDoc` variable.

```VBScript
     Dim CurrentApplication As Application
     Set CurrentApplication = MyDoc.Application

```

### Property **Name**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the name of the object. The name is a character string automatically assigned to any object to handle it easier. Even if the Name property allows you to reassign an object name, this is not advised. Many objects, such as the application and the collections, have names that you must not change, and it's safer to use Name as a read only property. When an object is part of a collection, the object name can often be used in place of the object rank to retrieve or remove the object, providing the Item and Remove methods of the collection feature an argument with the Variant type. A name must start with a letter. It can include numbers, but it can't include spaces. If the object has no name set, the default name returned is the object type. For example, the Name property of a Viewer3D object with no name set returns Viewer3D.

**Example:**      This example retrieves in `MyObjectName` the name of the `MyObject` object.

```VBScript
     MyObjectName = MyObject.Name

```

### Property **Parent**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md) (Read Only)

   Returns the parent object. The parent object of a given object is the object just above in the object structure, usually the object that created this object and that aggregates it. In the case of an object part of a collection, the parent object can be the collection object itself or the object that aggregates the collection object. The Parent property is the way to step upwards in the object structure. Note that the Parent property of the Application object returns the Application object itself.

**Example:**      This example retrieves in `ParentObject` the parent object of the `GivenObject` object.

```VBScript
     Dim ParentObject As AnyObject
     Set ParentObject = GivenObject.Parent

```

Methods

### Func **GetItem**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `IDName`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns an object from its name.

**Role** : To retrieve an object when only its name is available.

**Parameters:**

` IDName`      The searched obect name

**Returns:**      The searched object

---

# CacheSettingAtt (Object)

**_Represents the base object to handle the parameters of the cache._**

## Properties

### Property **ActivationMode**( ) As boolean

   Returns or sets the activation state of cache.

**Role** : Returns or sets the value of cache activation.  
### Property **CacheMaxSizeMo**( ) As long

   Returns or sets the value of the cache maximum size.

**Role** : Returns or sets the value of the maximum allowed cache size in Mo  
### Property **LODMode**( ) As boolean

   Returns or sets the LOD generation mode parameter.

**Role** : Returns or sets the value of the LOD generation mode.  
### Property **LocalPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the cache local path.

**Role** : Retrieves or sets the value of the cache local path. If the local path is defined with environment variables then this method return the unexpansed form.  
### Property **ReleasedVoxel**( ) As float

   Returns or sets the released voxel parameter.

**Role** : Returns or sets the value of the released voxel parameter.  
### Property **SizeControl**( ) As boolean

   Return or sets the cache size control.

**Role** : Returns or sets the cache size control. The cache use this parameter in conjunction with the maxixum allowed cache size. If it is turned off, the cache size has no limit.  
### Property **TimestampMode**( ) As boolean

   Retrieves or sets the timestamp control.

**Role** : If the timestamp control is turned on, the cache will verify if the cached object is uptodate with the master object. If not a new cached view will be generated.
If the timestamp control is turned off, the cache will consider that the cached views are always uptodate with their master object.  
### Property **UTCTimeFormat**( ) As boolean

   Retrieves or sets the the cache timestamp format.

**Role** : If the timestamp format is set to TRUE, then the time used used as timestamp by the cache is expressed in UTC format (GMT), in the other case the local time is used. The default format is local time.  Methods

### Func **GetActivationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Cache activation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetCacheMaxSizeMoInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the Cache maximum size.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetLODModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the LOD generation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetLocalPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the Cache local path.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetReleasePath**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retieves the cache release paths.

**Role** : Sets the cache release paths in a symbolic format.

**Parameters:**

` ioRelPath`      a CATSafeArrayVariant of CATBSTR.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetReleasePathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `Locked`) As boolean

   Retrieves environment informations for the Cache release path.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetReleasedVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the Cache released voxel.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSizeControlInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the size control mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetTimestampModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the timestamp control mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetUTCTimeFormatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the timestamp control mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **PutReleasePath**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iRelPath`)

   Sets the cache release paths.

**Role** : Sets the cache release paths in a symbolic format.

**Parameters:**

` iRelPath`      a CATSafeArrayVariant of CATBSTR.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetActivationModeLock**( boolean  `iLocked`)

   Locks or unlocks the Cache Activation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetCacheMaxSizeMoLock**( boolean  `iLocked`)

   Locks the paramater Cache maximum size.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetLODModeLock**( boolean  `iLocked`)

   Locks or unlocks the LOD generation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetLocalPathLock**( boolean  `iLocked`)

   Locks or unlocks the cache local path parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetReleasePathLock**( boolean  `iLocked`)

   Locks or unlocks the cache local path parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetReleasedVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the released voxel parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetSizeControlLock**( boolean  `iLocked`)

   Locks or unlocks the cache size control parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetTimestampModeLock**( boolean  `iLocked`)

   Locks or unlocks the timestamp control in cache.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetUTCTimeFormatLock**( boolean  `iLocked`)

   Locks or unlocks the timestamp format.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.

---

# CATBaseDispatch (Object)

**_Base class for Automation interfaces._**

**Role** : All Automation interfaces must inherit from the `CATBaseDispatch` interface. They usually do not inherit directly from `CATBaseDispatch`, but rather from one of its subclasses: [AnyObject](../System/interface_AnyObject_17321.md) for individual objects or [Collection](../System/interface_Collection_22150.md) for collection objects. Some methods may however have arguments of type `CATBaseDispatch` when they accept both individual objects or collection objects. The interface provides no functionalities per se.

---

# CATBaseUnknown (Object)

**_Base class for creating interfaces and for implementing interfaces._**

**Role** : CATBaseUnknown supplies the infrastructure and the basic mechanisms to create interface abstract classes and to manage interface pointers. It is also the base class for classes which implements interfaces and for their extension classes because it supplies the code for the interface methods QueryInterface, AddRef and Release.

---

# Collection (Collection)

**_Represents the base object for collections._**
As a base object, it provides properties and methods shared by any other object.

## Properties

### Property **Application**( ) As [CATIAApplication](../InfInterfaces/interface_Application_26636.md) (Read Only)

   Returns the application. The application is the root object in the object structure and can be retrieved from any object in the object structure using the Application property. The Application property is the way to jump from any object up to the root of the object data structure, allowing then to navigate downwards. For in-process scripting, the application is always referred to as `CATIA`. Note that the Application property of the Application object returns the Application object itself.

**Example:**      This example retrieves in `CurrentApplication` the application object, root of the object structure, from a given object of this structure: a document refered to using the `MyDocCollecion` variable.

```VBScript
     Dim CurrentApplication As Application
     Set CurrentApplication = MyDocCollecion.Application

```

### Property **Count**( ) As long (Read Only)

   Returns the number of objects in the collection. This is handy to scan all the objects in a collection.

**Example:**      This example retrieves in `ObjectNumber` the number of objects currently gathered in `MyCollection`.

```VBScript
     ObjectNumber = MyCollection.Count

```

### Property **Name**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns or sets the name of the object. The name is a character string you can assign to any object to handle it easier. In the case of an object part of a collection, the name can often be used in place of the object rank to retrieve or remove the object, providing the Item and Remove methods of the collection feature an argument with the Variant type. If the object has no name set, the name returned is the one of its parent.

**Example:**      This example sets to `MyObject` the name `Nice and Handy Object Name`.

```VBScript
     MyObject.Name("Nice and Handy Object Name")

```

### Property **Parent**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md) (Read Only)

   Returns the parent object. The parent object of a given object is the object that created this object, usually the object just above in the object tree structure and that aggregates it. In the case of an object part of a collection, the parent object is not the collection object itself, but the object that aggregates the collection object. The Parent property is the way to step upwards in the object data structure. Note that the Parent property of the Application object returns the Application object itself.

**Example:**      This example retrieves in `ParentObject` the parent object of the `GivenObject` object.

```VBScript
     Dim ParentObject As AnyObject
     Set ParentObject = GivenObject.Parent

```

Methods

### Func **GetItem**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `IDName`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns an object from its name.

**Role** : To retrieve an object when only its name is available. **You should not use this method** , but you can find it in the macros generated by the Tools->Macro command.

**Parameters:**

` IDName`      The searched obect name

**Returns:**      The searched object

---

# CommandStatisticsSettingAtt (Object)

**_Interface for Command statistic Controler

**Role** : the command statistics controler manages the values of all or only a part of the attributes available for the thematic._**

For the definitions of methods and variables common to every thematic, see the [GeneralStatisticsSettingAtt](../System/interface_GeneralStatisticsSettingAtt_154832.md)

---

# DisconnectionSettingAtt (Object)

**_Represents the base object to handle the parameters of automatic disconnection._**
If the automatic disconnection is enable, the V5 session will be kill after a user-defined duration of inactivity.

## Properties

### Property **ActivationState**( ) As boolean

   Returns or sets the activation state of automatic disconnection.

**Role** :Returns or sets the activation mode of automatic disconnection.  
### Property **InactivityDuration**( ) As long

   Returns or sets the inactivity duration.

**Role** : Returns or sets the timeout in seconds before the automatic disconnection when no activity has been detected, if the mechanism is enabled.  Methods

### Func **GetActivationStateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the activation mode of automatic disconnection.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetInactivityDurationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for inactivity duration.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetActivationStateLock**( boolean  `iLocked`)

   Locks or unlocks the activation mode of automatic disconnection.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetInactivityDurationLock**( boolean  `iLocked`)

   Locks or unlocks the inactivity duration.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.

---

# DLNameSettingAtt (Object)

**_Interface to handle the DLNames._**

**Role** : This interface is implemented by a component which represents the controller of the DLNames.
This interface defines:

  * A method to set each DLName
  * A method to get the value of each DLName
  * A method to lock/unlock each parameter
  * A method to retrieve the informations concerning each parameter

## Properties

### Property **DLNameCreationRight**( ) As boolean

   Returns or set the right to create new DLNames.

**Role** : Retrieves or set the right to create new DLNames.  
### Property **RootDLNameCreationRight**( ) As boolean

   Returns or set the right to create new Root DLNames.

**Role** : Retrieves or set the right to create new Root DLNames.  Methods

### Sub **GetDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameUnix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameNT`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oFather`)

   Retrieves the mapping between a logical name and the physical path.

**Role** : Retrieves the mapping between a logical name and the physical path.

**Parameters:**

` iDLName`      the logical name.
` oRealNameUnix`      the real physical path corresponding to the logical name on Unix.
` oRealNameNT`      the real physical path corresponding to the logical name on Windows.
` iFather`      if applicable the Name of the parent DLName

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDLNameCreationRightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves the state of the parameter DLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **GetDLNameExp**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameUnix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameNT`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oFather`)

   Retrieves the mapping between a logical name and the physical path.

**Role** : Retrieves the mapping between a logical name and the physical path in a litteral form.

**Parameters:**

` iDLName`      the logical name.
` oRealNameUnix`      the real physical path corresponding to the logical name on Unix.
` oRealNameNT`      the real physical path corresponding to the logical name on Windows.
` iFather`      if applicable the Name of the parent DLName

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDLNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves the state of the for a given DLName.

**Role** : This information defines the state of the setting parameter and is made up of:

  * The administration level that sets the current value or the value used to reset it
  * The administration level that has locked the setting parameter.
  * A flag to indicate whether the setting parameter was modified.

**Parameters:**

` iDLName`      a DLname.
` ioAdminLevel`      [inout] The administration leve that defines the value used when resetting the setting parameter. **Legal values** :

  * **Default value** if the DLName has never been defined in the administration concatenation.
  * **Admin Level n** if the setting parameter has been administered,
where n is an integer starting from 0 representing the rank of the administration level.

` ioLocked`      [inout] A character string to indicate whether the parameter is locked and the level of administration where the locking has been proceeded.

**Legal values** :

  * **Locked at Admin Level n** if the setting parameter is locked by then administration level n,
where n is an integer starting from 0.
  * **Upper Locked** if the setting parameter is locked by the current administration level
  * **Unlocked** if the setting parameter is not locked

**Returns:**          **True** to indicate that the DLName value has been defined at the current administrator or user level. This is only possible with unlocked DLNames. **False** means that the DLName is inherited from the administration.

### Func **GetDLNameList**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retrieves the list of the DLNames.

**Role** : Retrieves the list of the defined DLNames.

**Parameters:**

` oTabDLName`      a CATSafeArrayVariant of CATBSTR of nb elements.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDLNameSubList**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retrieves the list of the Sub-DLNames.

**Role** : Retrieves the list of the DLNames created in a given DLName.

**Parameters:**

` iDLName`      The Father DLName. if iDLName=NULL all DLNames created at the root level are return.
` oNbDLname`      The number of defined DLNames.
` oTabDLName`      The array of DLNames

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_OUTOFMEMORY:` on allocation failure
`E_FAIL:` on other failures  
### Func **GetRootDLNameCreationRightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves the state of the parameter RootDLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **RemoveDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`)

   Remove a logical name.

**Role** : Remove a DLName in the current set if it is possible.

**Parameters:**

` iDLName`      the logical name.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **RenameDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNewName`)

   Rename an existing DLName.

**Role** : Rename a DLName in the current set if it is possible.

**Parameters:**

` iDLName`      the logical name to rename.
` iNewName`      the new logical name.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRealNameUnix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRealNameNT`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFather`,  boolean  `iVerifDirectory`)

   Sets the mapping between a logical name and the physical path.

**Role** : Sets the value of the cache maximum size in Mo

**Parameters:**

` iDLName`      the logical name.
` oRealNameUnix`      the real physical path corresponding to the logical name on Unix.
` oRealNameNT`      the real physical path corresponding to the logical name on Windows.
` iFather`      if applicable the Name of the parent DLName
` iVerifDirectory`      if VerifDirectory is set the existence of the directory on the current platform will be check.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDLNameCreationRightLock**( boolean  `iLocked`)

   Locks or unlocks the parameter DLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetDLNameLock**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  boolean  `iLocked`)

   Locks or unlocks the DLName.

**Role** : Locks or unlocks the given DLName if the operation is allowed in the current administrated environment. In user mode this method will always return E_FAIL.

**Parameters:**

` iDLname`      the DLname to be locked.
` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetRootDLNameCreationRightLock**( boolean  `iLocked`)

   Locks or unlocks the parameter RootDLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.

---

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

---

# ErrorlogStatisticsSettingAtt (Object)

**_Interface for Errorlog statistic Controler._**

**Role** : the errorlog statistics controler manages the values of all or only a part of the attributes available for the thematic.
For the definitions of methods and variables common to every thematic, see the [GeneralStatisticsSettingAtt](../System/interface_GeneralStatisticsSettingAtt_154832.md)

## Properties

### Property **ABND**( ) As boolean

   Returns or sets the state ot the abend severity level field.

**Role** : Returns or sets the state ot the abend severity level field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **CERR**( ) As boolean

   Returns or sets the state ot the critical error severity level field.

**Role** : Returns or sets the state ot the critical error severity level field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **CMND**( ) As boolean

   Returns or sets the state ot the command name field.

**Role** : Returns or sets the state ot the command name field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **COMT**( ) As boolean

   Returns or sets the state ot the abend comment level field.

**Role** : Returns or sets the state ot the comment severity level field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **MSGE**( ) As boolean

   Returns or sets the state ot the message field.

**Role** : Returns or sets the state ot the message field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **UREP**( ) As boolean

   Returns or sets the state ot the user report severity level field.

**Role** : Returns or sets the state ot the user report severity level field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **WARN**( ) As boolean

   Returns or sets the state ot the warning severity level field.

**Role** : Returns or sets the state ot the warning severity level field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **WKBN**( ) As boolean

   Returns or sets the state ot the workbench name field.

**Role** : Returns or sets the state ot the workbench name field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

---

# GeneralStatisticsSettingAtt (Object)

**_Interface for General statistic Controler._**

**Role** : the General statistics controler is a generic interface for all the thematics. One should never use it as a statistics thematic.

## Properties

### Property **Activation**( ) As boolean

   Returns or sets the activation state of the statistics thematic.

**Role** : Returns or sets the value of statistics thematic activation.  
### Property **CPUS**( ) As boolean

   Returns or sets the state ot the cpu time field.

**Role** : Returns or sets the state ot the cpu time field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **CumulationMode**( ) As boolean

   Returns or sets the cumulation state of the statistics thematic.

**Role** : Returns or sets the value of statistics thematic cumulation.  
### Property **DateFormat**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the state ot the date format field.

**Role** : Returns or sets the state ot the date format field.

**Parameters:**

` iDateFormat`      **Legal values** :
`StandardDate :` default date format (Mon Jan 1 08:00.00 2000)
`NumericalDate:` numerical date format(2000.001.08.00.00)
`NumericalDateMilliecond:` numerical date format(2000.001.08.00.00.000)

### Property **ELPS**( ) As boolean

   Returns or sets the state ot the elapsed time field.

**Role** : Returns or sets the state ot the elapsed time field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **HOST**( ) As boolean

   Returns or sets the state ot the host name field.

**Role** : Returns or sets the state ot the host name field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **Output**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the output format of the statistics thematic.

**Role** : Returns or sets the output format of the statistics thematic.

**Parameters:**

` oOutputType`      **Legal values** :
`File :` statistics are outputed in a file
`Console:` statistics are outputed on the console (if available)

### Property **OutputFile**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path of the statistics thematic file.

**Role** : Returns or sets the path of the statistics thematic file.  
### Property **OutputFormat**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the state ot the output format field.

**Role** : Returns or sets the state ot the output format field.

**Parameters:**

` iOutputFormat`      **Legal values** :
`StandardOutput:` default format
`NoThematics :` the thematic name is not repeated on each line

### Property **RTIM**( ) As boolean

   Returns or sets the state ot the response time field.

**Role** : Returns or sets the state ot the response time field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **THEM**( ) As boolean

   Returns or sets the state ot the thematic field.

**Role** : Returns or sets the state ot the thematic field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **TIME**( ) As boolean

   Returns or sets the state ot the time and date field.

**Role** : Returns or sets the state ot the time and date field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **TimeUnit**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the state ot the time unit field.

**Role** : Returns or sets the state ot the time unit field.

**Parameters:**

` iTimeUnit`      **Legal values** :
`Second :` durations are in seconds
`Millisecond:` durations are in milliseconds

### Property **UPID**( ) As boolean

   Returns or sets the state ot the user pid field.

**Role** : Returns or sets the state ot the user pid field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **USER**( ) As boolean

   Returns or sets the state ot the user name field.

**Role** : Returns or sets the state ot the user name field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated
Methods

### Func **GetFormatMode**( long  `flag`) As boolean

   Returns the format mode of the statistics thematic.

**Role** : Returns or sets the format mode of the statistics thematic.

**Parameters:**

` oFormatMode`      **Legal values** :
`TRUE :` the thematic output is formated (field="value").
`FALSE:` the thematic output is not formated ("value").

### Func **GetThematicsParameterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the general statistics parameters.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetFormatMode**( boolean  `iFormatMode`,  long  `flag`)

   Sets the format mode of the statistics thematic.

**Role** : Returns or sets the format mode of the statistics thematic.

**Parameters:**

` iFormatMode`      **Legal values** :
`TRUE :` the thematic output is formated (field="value").
`FALSE:` the thematic output is not formated ("value").

### Sub **SetThematicsParameterLock**( boolean  `iLocked`)

   Locks or unlocks the general statistics parameters.

**Role** :Locks or unlocks the statistics parameters.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure

---

# GlobalStatisticsSettingAtt (Object)

**_Interface for Global statistic Controler

**Role** : the global statistics controler manages the values of all or only a part of the attributes available for all the statistics thematics._**

## Properties

### Property **BufferSize**( ) As long

   Returns or sets the size of buffer.

**Role** : Returns or sets the size of the buffer.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  
### Property **CopyDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path of the copy directory.

**Role** : Returns or sets the path of the directory where the copy files are located.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  
### Property **MaxCopyFile**( ) As long

   Returns or sets the maximum number of copy files.

**Role** : Returns or sets the value of the maximum number of statistics files copies.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  
### Property **MaxSizePerFile**( ) As long

   Returns or sets the maximum size per file.

**Role** : Returns or sets the value of the maximum size of statistics files.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  Methods

### Func **GetThematicsParameterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the global statistics parameters.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetThematicsParameterLock**( boolean  `iLocked`)

   Locks or unlocks the global statistics parameters.

**Role** :Locks or unlocks the global statistics parameters.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure

---

# IDispatch (Object)

**_Base interface for all Automation interfaces._**

**Role** : All Automation interfaces derive from `IDispatch` which replaces for UNIX the native Microsoft(R) `IDispatch` interface. This interface supplies basic methods to be Microsoft(R) Automation compliant.

---

# IUnknown (Object)

**_Base interface for all interfaces._**

**Role** : All interfaces derive from `IUnknown` which replaces for UNIX the native Microsoft(R) `IUnknown` interface. This interface supplies the three basic methods QueryInterface, AddRef and Release to be COM (Microsoft(R) Component Object Model) compliant. These methods cannot be used in a macro.

---

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

---

# MemoryWarningSettingAtt (Object)

**_Represents the base object to handle the parameters of memory warning mechanism._**
This mechanism informs the user when the process memory use exceeds a given percentage of the address space usage. This mechanism warns you that because the amout of remaining memory is becoming low, you should save your data and leave the session.

## Properties

### Property **ActivationState**( ) As boolean

   Returns or sets the activation state of the memory warning mechanism.

**Role** : Returns or sets the value of of the memory warning.  
### Property **MemoryStopperState**( ) As boolean

   Returns or sets the activation state of the memory stopper mechanism.

**Role** : Returns or sets the value of of the memory stopper.  
### Property **UsageLimit**( ) As long

   Returns or sets the alert percentage.

**Role** : Returns or sets the percentage of the address space usage that can be used by the process before sending the warning.  Methods

### Func **GetActivationStateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the memory warning mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetMemoryStopperStateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the memory stopper mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetUsageLimitInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the alert percentage.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetActivationStateLock**( boolean  `iLocked`)

   Locks or unlocks the activation mode of the memory warning mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetMemoryStopperStateLock**( boolean  `iLocked`)

   Locks or unlocks the activation mode of the memory stopper mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetUsageLimitLock**( boolean  `iLocked`)

   Locks or unlocks the the alert percentage.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.

---

# PCSStatisticsSettingAtt (Object)

**_Interface for PCS statistic Controler

**Role** : the PCS statistics controler manages the values of all or only a part of the attributes available for the thematic._**

For the definitions of methods and variables common to every thematic, see the [GeneralStatisticsSettingAtt](../System/interface_GeneralStatisticsSettingAtt_154832.md)

## Properties

### Property **MemUse**( ) As boolean

   Returns or sets the state ot the memory field.

**Role** : Returns or sets the state ot the workbench name field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

---

# ServerStatisticsSettingAtt (Object)

**_Interface for Server statistic Controler

**Role** : the server statistics controler manages the values of all or only a part of the attributes available for the thematic._**

For the definitions of methods and variables common to every thematic, see the [GeneralStatisticsSettingAtt](../System/interface_GeneralStatisticsSettingAtt_154832.md)

---

# SessionStatisticsSettingAtt (Object)

**_Interface for Session statistic Controler

**Role** : the session statistics controler manages the values of all or only a part of the attributes available for the thematic._**

For the definitions of methods and variables common to every thematic, see the [GeneralStatisticsSettingAtt](../System/interface_GeneralStatisticsSettingAtt_154832.md)

---

# SettingController (Object)

**_Represents the base object for setting controllers._**

**Role** : A setting controller manages all or only a part of the parameters available in a property page of the dialog displayed using the Options command of the Tools menu. Each setting parameter may be represented by one or several setting attribute in the underlying setting repository.

All setting controllers share the five methods of the SettingController object to deal with the whole set, or a subset of the setting attributes:

  * `Commit` to make a memory copy of the setting attribute values
  * `Rollback` to restore the last memory copy of the setting attribute values
  * `ResetToAdminValues` to restore the administered values of all the attributes
  * `ResetToAdminValuesByName` to restore the administered values of a subset of the attributes
  * `SaveRepository` to make a persistent copy of the setting attribute values on file.

In addition, each setting controller exposes four methods per setting parameter: two methods to access the setting attribute values, that usually make up a read/write property if the setting parameter is represented by a single setting attribute, a method to manage the setting parameter lock, and a method to retrieve the state of the setting parameter. The first two methods are parameter-specific and are fully described in the setting controller object that managing the setting parameter. The last two methods have always the same signature and the same behavior whatever the setting parameter. They are described below. PARAMETER is used in place of the actual setting parameter name.

  * **Managing the Setting Parameter Lock**

```VBScript
```

Locks or unlocks the PARAMETER setting parameter.

**Role** : Locking a setting parameter prevents the end user, or the administrators below the current one, from changing the setting parameter value. Locking or unlocking the PARAMETER setting parameter is an administrator task and is possible when running a session in the administration mode only.

**Parameters**

`iLocked`
    [in] A flag to indicate whether the PARAMETER setting parameter should be locked.

**Legal values** : `True` to lock, and `False` to unlock.

  * **Retrieving the Setting Parameter State**

```VBScript
                                        inout CATBSTR ioLocked,
                                        out  /*IDLRETVAL*/ boolean oModified);
```

Retrieves information about the PARAMETER setting parameter.

**Role** : This information defines the state of the setting parameter and is made up of:

    * The administration level that sets the current value or the value used to reset it
    * The administration level that has locked the setting parameter.
    * A flag to indicate whether the setting parameter was modified.

**Parameters**

`ioAdminLevel`
    [inout] The administration leve that defines the value used when resetting the setting parameter.

**Legal values** :

    * **Default value** if the setting parameter has never been explicitly set in the administration concatenation.
    * **Set at Admin Level n** if the setting parameter has been administered,
where n is an integer starting from 0 representing the rank of the administration level.
`ioLocked`
    [inout] A character string to indicate whether the parameter is locked and the level of administration where the locking has been proceeded.

**Legal values** :
    * **Locked at Admin Level n** if the setting parameter is locked by then administration level n,
where n is an integer starting from 0. The setting parameter can not be modified at the current level.
    * **Locked** if the setting parameter is locked by the current administration level. Only an admistrator can get this value.
    * **Unlocked** if the setting parameter is not locked

**Returns**

    **True** to indicate that the setting parameter value has been explicitely modified at the current administrator or user level. This is only possible with unlocked parameters. **False** means that it inherits the administered value.

## Methods

### Sub **Commit**( )

   Makes a memory copy of the setting attribute values.

**Role** : `Commit` saves the current values of the setting attributes managed by the setting controller in a specific memory area. Successive calls to `Commit` overwrite the memory area. The values saved by the last call to `Commit` can be restored from that memory area using the Rollback method.  
### Sub **ResetToAdminValues**( )

   Restores the administrated values of the all attributes.

**Role** : `ResetToAdminValues` restores all the values of the setting attributes managed by the setting controller to either the values set by the setting administrator, or to their default values if the setting administrator did not change them.  
### Sub **ResetToAdminValuesByName**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAttList`)

   Restores the administrated values of a subset of the attributes.

**Role** : `ResetToAdminValuesByName` restores the values of a subset of the setting attributes managed by the setting controller to either the values set by the setting administrator, or to their default values if the setting administrator did not change them.

**Parameters:**

` iAttList`      The attribute subset to which the administrated values are to be restored

### Sub **Rollback**( )

   Restores the last memory copy of the setting attribute values.

**Role** : `Rollback` restores the values of the setting attributes managed by the setting controller from the memory area. All values of the setting attributes managed by the setting controller modified since the last call to Commit are restored to the values they had when this last Commit was called.  
### Sub **SaveRepository**( )

   Makes a persistent copy of the setting attribute values on file.

**Role** : `SaveRepository` saves the current values of the setting attributes managed by the setting controller in a setting repository file. To avoid inconsistencies, `SaveRepository` first saves the values in the memory area used by the Commit method by calling Commit before writing the values in the setting repository file.

---

# SystemService (Object)

**_Represents an object which provides system services._**

## Methods

### Func **Environ**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iEnvString`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the value of an environment variable.

**Parameters:**

` iEnvString`      The name of the environment variable  **Example:**      This example retrieves the value of the `PATH` variable in the `Value` string.

```VBScript
     Value = CATIA.SystemService.Environ("PATH")

```

### Func **Evaluate**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iScriptText`,  [CATScriptLanguage](../System/enum_CATScriptLanguage_59191.md)  `iLanguage`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFunctionName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iParameters`) As [CATVariant](../System/typedef_CATVariant_20656.md)

   Evaluates a scripted function.

**Parameters:**

` iScriptText`      The program text
` iLanguage`      The language the program is written in
` iFunctionName`      The name of the function to invoke
` iParameters`      An array of parameters for the function
` oResult`      The value returned by the function (if any)  **Example:**      This example executes the function CATMain in the program Macro1.catvbs contained by Part1.CATPart

```VBScript
     Dim params()
     CATIA.SystemService.Evaluate"Sub CATMain\nMsgBox \"Hello, World\"\nEnd Sub", CATVBScriptLanguage, "CATMain", params

```

### Func **ExecuteBackgroundProcessus**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExecutablePath`) As long

   Executes an asynchronous process. This process is launched in background and `ExecuteBackgroundProcess` doesn't wait for it to complete. If the executable to run needs a specific environment to works correctly (for example environment variables like PATH or LD_LIBRARY_PATH correctly set), this environment must have been set in order to make this method succeed. If this executable needs to be launched from a window, this method will fail.

**Parameters:**

` iExecutablePath`      The path of the executable to run and its arguments If the executable is not present in the PATH environment variable, you must specify its complete absolute path. If this path contains blanks, you must enclose it with the simple quote character ''' : for example CATIA.SystemService.ExecuteBackgroundProcess "'C:\Program Files\myApp\myApp.exe' myArg".

**Returns:**      Non significative return code. It's never the asynchronous process return code  **Example:**      This example executes the command located at
```

```VBScript
and doesn't wait the end of its execution.

```VBScript
     CATIA.SystemService.ExecuteBackgroundProcessus ""

```

### Func **ExecuteProcessus**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExecutablePath`) As long

   Executes a synchronous process. If this process is succesfully launched, `ExecuteProcessus` waits for it to terminate and returns the process return code. If the executable to run needs a specific environment to works correctly (for example environment variables like PATH or LD_LIBRARY_PATH correctly set), this environment must have been set in order to make this method succeed. If this executable needs to be launched from a window, this method will fail.

**Parameters:**

` iExecutablePath`      The path of the executable to run and its arguments. If the executable is not present in the PATH environment variable, you must specify its complete absolute path. If this path contains blanks, you must enclose it with the simple quote character ''' : for example CATIA.SystemService.ExecuteProcessus "'C:\Program Files\myApp\myApp.exe' myArg".

**Returns:**      The synchronous process return code  **Example:**      This example executes the command located at
```

```VBScript
waits for it to end, and returns its return code.

```VBScript
     ReturnCode = CATIA.SystemService.ExecuteProcessus("")

```

### Func **ExecuteScript**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLibraryName`,  [CatScriptLibraryType](../System/enum_CatScriptLibraryType_85292.md)  `iType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProgramName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFunctionName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iParameters`) As [CATVariant](../System/typedef_CATVariant_20656.md)

   Executes a scripted function.

**Parameters:**

` iLibraryName`      The library in which the script is contained
` iLibraryType`      The type of the library
` iProgramName`      The name of the program in the library
` iFunctionName`      The name of the function to invoke
` iParameters`      An array of parameters for the function
` oResult`      The value returned by the function (if any)  **Example:**      This example executes the function CATMain in the program Macro1.catvbs contained by Part1.CATPart

```VBScript
     Dim params()
     CATIA.SystemService.ExecuteScript"Part1.CATPart", catScriptLibraryTypeDocument, "Macro1.catvbs", "CATMain", params

```

### Sub **Print**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iString`)

   Prints a string on stdout.

**Parameters:**

` iString`      The string to print  **Example:**      This example prints the string "Hello world!".

```VBScript
     CATIA.SystemService.Print("Hello world!")

```

---

# WorkbenchStatisticsSettingAtt (Object)

**_Interface for Workbench statistic Controler._**

**Role** : the workbench statistics controler manages the values of all or only a part of the attributes available for the thematic.
For the definitions of methods and variables common to every thematic, see the [GeneralStatisticsSettingAtt](../System/interface_GeneralStatisticsSettingAtt_154832.md)

---

# System Typedef CATBSTR

**_Defines the string type to be used by Automation interfaces._**

---

# System Typedef CATSafeArrayVariant

**_Defines a` CATSafeArrayVariant` type to be used by Automation interfaces._**
`CATSafeArrayVariant` are one-dimensional arrays of `CATVariants`.

---

# System Typedef CATVariant

**_Defines the variant type to be used by Automation interfaces._**