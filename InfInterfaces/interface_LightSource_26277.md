# LightSource (Object)

**_Represents the light source._**
The light source is the object that stores lighting data used by a viewer to display a scene where a document is presented. Two kinds of light sources are available: an infinite light source and a neon lighting system simulating a set of parallel neon tubes.

## Methods

### Sub **GetDirection**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `oDirection`)

   Returns the lighting direction as an array of 3 variants. This value is available with an infinite light source only.

**Example:**      This example gets the lighting direction of the `LightSource` light source to the direction with components (5,8,-2).

```VBScript
     Dim direction(2)
     LightSource.GetDirection direction

```

### Sub **PutDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

   Defines the lighting direction as an array of 3 variants. This value can be set with an infinite light source only.

**Example:**      This example defines the lighting direction of the `LightSource` light source to the direction with components (5,8,-2).

```VBScript
     LightSource.PutDirection Array(5,8,-2)

```