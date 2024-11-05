## kudos to the original author DevOPS Journey in YT

## Check your version of kubectl
```
$ kubectl version
Client Version: v1.31.0 Kustomize Version: v5.4.2
```

## Viewing Kustomize Configs - (Using kubectl kustomize integration)
```
kubectl kustomize bases/
kubectl kustomize overlays/dev/
kubectl kustomize overlays/prod/
```

## Applying Kustomize Configs - (Using kubectl kustomize integration)
```
kubectl apply -k overlays/dev/
kubectl apply -k overlays/prod/
```
Note: This is just tip of the iceberg will update this repo once i find something more interesting on this

## References:
https://github.com/kubernetes-sigs/kustomize/blob/master/README.md
https://kubectl.docs.kubernetes.io/guides/config_management/offtheshelf/
