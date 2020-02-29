This package demonstrates combining two existing kustomizaiton patches.

This only works if a given resource is only defined in or other the package.
Defining the same resource in multiple packages will result in a name conflict.

This means it can't be used for creating patches to be mixed into different overlays.

```
cd overlays
kustomize build
```