## Install uptime-kuma helm
#### [Document](https://dirsigler.github.io/uptime-kuma-helm/)
 
### Helm add repo

    helm repo add uptime-kuma https://dirsigler.github.io/uptime-kuma-helm

### Helm install

    helm install my-uptime-kuma uptime-kuma/uptime-kuma

### Creater file VirtualService 

    apiVersion: networking.istio.io/v1beta1
    kind: VirtualService
    metadata:
      name: kuma-vs
      namespace: default
    spec:
      gateways:
      - unicloud-api-gateway       
      hosts:
      - health.unicloud.com.vn
      http:
      - match:
        - uri:
            prefix: /    
        name: kuma-vs
        route:
        - destination:
            host: my-uptime-kuma.default.svc.cluster.local
            port:
              number: 3001

### Apply file VirtualSeervice

    kubectl apply -f <file>