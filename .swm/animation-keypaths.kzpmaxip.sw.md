---
id: kzpmaxip
title: Animation Keypaths
file_version: 1.1.3
app_version: 1.12.1
---

`AnimationKeypath` is an object that describes a keypath search for nodes in the animation JSON. `AnimationKeypath` matches views and properties inside of `AnimationView` to their backing `Animation` model by name.

A keypath can be used to set properties on an existing animation, or can be validated with an existing `Animation`. `AnimationKeypath` can describe a specific object, or can use wildcards for fuzzy matching of objects. Acceptable wildcards are either "\*" (star) or "\*\*" (double star). Single star will search a single depth for the next object. Double star will search any depth.

An `AnimationKeypath` can be initialized with a dot-separated keypath, or with an array of keys.

Keypath Examples:

```
/// Represents a specific color node on a specific stroke.
@"Layer.Shape Group.Stroke 1.Color"
```

```
/// Represents the color node for every Stroke named "Stroke 1" in the animation.
@"**.Stroke 1.Color"
```

Code Example:

```
/// A keypath that finds the color value for all `Fill 1` nodes.  
let fillKeypath =  AnimationKeypath(keypath:  "**.Fill 1.Color")
```

<br/>

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBbG90dGllLWlvcyUzQSUzQXVzZXJ0ZXN0aW5nLXN3aW1t/docs/kzpmaxip).