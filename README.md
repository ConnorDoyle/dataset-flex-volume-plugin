# dataset-flex-volume-plugin

Experimental flex volume plugin for Kubernetes to manage machine learning datasets.

## Install

Place the `dataset` file in the Kubelet flex volume plugin path on each compute host:

`/usr/libexec/kubernetes/kubelet-plugins/volume/exec/ml~dataset/dataset`

## Use

```yaml
volumes:
  - name: trainingData
    flexVolume:
      driver: "ml/dataset"
      options:
        url: "https://example.com/data.tgz"
```
