# CatClippingMode (Enumeration)

**_Depth effects._**
They are used by the [Viewer3D](../InfInterfaces/interface_Viewer3D_12290.md) object.

**Values:**

` catClippingModeClear`      The clear depth effect. All objects are displayed.
` catClippingModeNear`      The scene is clipped by the near plane only. Any object between the eye and the near plane is not visible.
` catClippingModeFar`      The scene is clipped by the far plane only. Any object beyond the far plane is not visible.
` catClippingModeNearAndFar`      The foggy depth effect. Fog is added in the background to progressively dissimulate far objects. This increases the display performance when a great number of objects are displayed.