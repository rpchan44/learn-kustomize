## kudos to the original author DevOPS Journey in YT

## Check your version of kubectl
```
kubectl version # recommended
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
kubectl apply -k bases/
kubectl apply -k overlays/dev/
kubectl apply -k overlays/prod/
```
Note: This is just tip of the iceberg will update this repo once i find something more interesting on this


## Creating Namespaces if you dont have them already
```
kubectl create namespace development; kubectl create namespace production;
```


## Accessing the application (minikube)
```
minikube service kustom-mywebapp-v1
minikube service kustom-mywebapp-v1 -n dev
minikube service kustom-mywebapp-v1 -n prod
```

## Accessing the application with your favorite k8s flavors (k3s,k8s)
```
kubectl port-forward svc/devel-mywebapp-v1 8080:80
kubectl port-forward svc/devel-mywebapp-v1 8080:80 -n development
kubectl port-forward svc/devel-mywebapp-v1 8080:80 -n production

```
## References:
https://github.com/kubernetes-sigs/kustomize/blob/master/README.md
https://kubectl.docs.kubernetes.io/guides/config_management/offtheshelf/
