### To install MetalLB
```
kubectl apply -f https://raw.githubusercontent.com/google/metallb/v0.7.3/manifests/metallb.yaml
kubectl apply -f https://raw.githubusercontent.com/google/metallb/v0.8.3/manifests/metallb.yaml
```

### Apply Configuration(edit subnet before apply)
```
kubectl apply -f https://github.com/gonhvvjvo/K8S/raw/master/InstallMetalLB/MetalLB-ConfigMap.yaml
```

### To view configuration & subnet
```
kubectl describe configmaps -n metallb-system
```

### Links
https://kubernetes.github.io/ingress-nginx/deploy/baremetal/
