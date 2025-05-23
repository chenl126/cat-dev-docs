# SceneWorkbench (Object)

**_Represent the access point to scenes management._**

## Properties

### Property **WorkScenes**(| ) As [CATIAWorkScenes](../OSMInterfaces/interface_Scenes_8092.md) (Read Only)

   Returns the Scenes collection.

**Example:**      This example retrieves the WorkScenes collection of the active document.

```VBScript
        Dim TheWorkSceneWorkbench As Workbench
        Set TheWorkSceneWorkbench = CATIA.ActiveDocument.GetWorkbench ( "SceneWorkbench" )
        Dim TheScenesList As WorkScenes
        Set TheScenesList = TheWorkSceneWorkbench.WorkScenes

```