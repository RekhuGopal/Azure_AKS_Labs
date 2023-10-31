# Azure_AKS_Labs
This repo contains Terraform code to create AKS and Specification file to deploy example application AKS.


#AKS Monitroing Accessibility
1. az login --use-device-code
2. az aks get-credentials --resource-group "<rg>" --name "<cluster name>"
3. kubectl --namespace monitoring get pods -l "release=prometheus"
4. kubectl port-forward --namespace monitoring svc/prometheus-kube-prometheus-prometheus 9090
5. kubectl port-forward --namespace monitoring svc/prometheus-grafana 8080:80
6. grafan user name : "admin" , password : "prom-operator"