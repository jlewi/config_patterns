This package illustrates that patches must be in lower directories.

In this example `mixins/deployment_patch.yaml` defines a patch that
we would like to apply in the overlays. But if we run kustomize build
in the overlays we get an error.

```
cd overlays
kustomize build
Error: builtin PatchStrategicMergeTransformer config: [112 97 116 104 115 58 10 45 32 46 46 47 109 105 120 105 110 115 47 100 101 112 108 111 121 109 101 110 116 95 112 97 116 99 104 46 121 97 109 108 10]: security; file '/home/jlewi/git_jlewi-config_patterns/kustomize/broken-app/mixins/deployment_patch.yaml' is not in or below '/home/jlewi/git_jlewi-config_patterns/kustomize/broken-app/overlays'

