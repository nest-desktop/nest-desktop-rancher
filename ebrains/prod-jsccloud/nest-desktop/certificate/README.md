# How to request a certificate


### Requirements

- kubectl (https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)


### Steps

- Install `kubectl`

- Download the KubeConfig from Rancher (top right).

- Create certificate with `kubectl`

``` 
export KUBECONFIG=$PWD/prod-jsccloud.yaml 
kubectl apply -f certificate.yaml
```

-> certificate.cert-manager.io/nest-desktop-apps-tls on Rancher created

- Add the certificate `nest-desktop-apps-tls` in ingress `nest-desktop.apps.prod-jsccloud.ebrains.eu`.

### References

https://devops.handbook.ebrains.eu/about-kubernetes/networking/certificates/#requesting-a-certificate