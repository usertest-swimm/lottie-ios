---
id: gr4np5yx
title: Value Providers
file_version: 1.1.3
app_version: 1.12.1
---

`AnyValueProvider` is a protocol that return animation data for a property at a given time. Every fame an `AnimationView` queries all of its properties and asks if their ValueProvider has an update. If it does the AnimationView will read the property and update that portion of the animation.

Value Providers can be used to dynamically set animation properties at run time.

### Primitives

ValueProviders work with a few Primitive data types.

*   **Color**: A primitive that describes a color in R G B A (0-1)

*   **Vector1D**: A single float value.

*   **Vector3D**: A three dimensional vector. (X, Y, Z)

    ### strongPrebuilt Providers

    Lottie comes with a handful of prebuilt providers for each Primitive Type. Each Provider can be initialized with a single value, or a block that will be called on a frame-by-frame basis.

Example

```

/// A Color Value provider that returns a reddish color.
let redValueProvider = ColorValueProvider(Color(r: 1, g: 0.2, b: 0.3, a: 1))

/// A keypath that finds the color value for all `Fill 1` nodes.
let fillKeypath = AnimationKeypath(keypath: "**.Fill 1.Color")
/// Set the provider on the animationView.
animationView.setValueProvider(redValueProvider, keypath: fillKeypath)

/// Later...
/// Changing the value provider will update the animation.
redValueProvider.color = Color(r: 0, g: 0.2, b: 1, a: 1)
```

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBbG90dGllLWlvcyUzQSUzQXVzZXJ0ZXN0aW5nLXN3aW1t/docs/gr4np5yx).