# IUnknown (Object)

**_Base interface for all interfaces._**
**Role** : All interfaces derive from `IUnknown` which replaces for UNIX the native Microsoft(R) `IUnknown` interface. This interface supplies the three basic methods QueryInterface, AddRef and Release to be COM (Microsoft(R) Component Object Model) compliant. These methods cannot be used in a macro.