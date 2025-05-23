# SchAppEnvironment (Object)

**_Manage the application environment in a schematic session._**

## Methods

### Sub **AppCleanUpWhenApplicationEnds**(| )

   Initialize environment when schematic application ends.

**Example:**

```VBScript
     Dim objThisIntf As SchAppEnvironment
      ...
     objThisIntf.AppCleanUpWhenApplicationEnds

```

### Sub **AppInitWhenApplicationStarts**( )

   Initialize environment when schematic application starts.

**Example:**

```VBScript
     Dim objThisIntf As SchAppEnvironment
      ...
     objThisIntf.AppInitWhenApplicationStarts

```

### Sub **AppLoadFeatFiles**( )

   Load all the necessary feat files.

**Example:**

```VBScript
     Dim objThisIntf As SchAppEnvironment
      ...
     objThisIntf.AppLoadFeatFiles

```