- [Basic kubectl commands](#basic-kubectl-commands)
  - [minicube cluster](#minicube-cluster)
  - [kubectl commands](#kubectl-commands)
  - [debugging](#debugging)
  - [create deployment](#create-deployment)
    - [nginx](#nginx)
    - [mongo](#mongo)
  - [delete deployment](#delete-deployment)
- [Advanced kubectl commands](#advanced-kubectl-commands)
  - [create or edit config file](#create-or-edit-config-file)
  - [create or edit service](#create-or-edit-service)
  - [create or edit secret](#create-or-edit-secret)
  - [create or edit config map](#create-or-edit-config-map)
  - [create or edit persistent volume](#create-or-edit-persistent-volume)
  - [create or edit persistent volume claim](#create-or-edit-persistent-volume-claim)
  - [create or edit ingress](#create-or-edit-ingress)
  - [create or edit network policy](#create-or-edit-network-policy)
  - [create or edit pod security policy](#create-or-edit-pod-security-policy)
  - [create or edit role](#create-or-edit-role)
  - [create or edit role binding](#create-or-edit-role-binding)
  - [create or edit service account](#create-or-edit-service-account)
  - [create or edit custom resource definition](#create-or-edit-custom-resource-definition)
  - [create or edit custom resource](#create-or-edit-custom-resource)
  - [create or edit job](#create-or-edit-job)
  - [create or edit cron job](#create-or-edit-cron-job)
  - [create or edit daemon set](#create-or-edit-daemon-set)
  - [create or edit stateful set](#create-or-edit-stateful-set)
  - [create or edit pod disruption budget](#create-or-edit-pod-disruption-budget)
  - [metrics server](#metrics-server)

# Basic kubectl commands

## minicube cluster
`minikube start`
`minikube status`
`minikube stop`
`minikube delete`

## kubectl commands
`kubectl version`
`kubectl get nodes`
`kubectl get pod`
`kubectl get services`
`kubectl get deployment`
`kubectl get replicaset`
`kubectl get deployment  nginx-deployment -o yaml > nginx-deployment.yaml`


## debugging
`kubectl logs {pod-name}`
`kubectl exec -it {pod-name} -- bin/bash`

## create deployment
### nginx
`kubectl create deployment nginx-depl --image=nginx`
`kubectl edit deployment nginx-depl`
### mongo
`kubectl create deployment mongo-depl --image=mongo`
`kubectl edit deployment mongo-depl`
`kubectl logs mongo-depl-{pod-name}`

## delete deployment
`kubectl delete deployment mongo-depl`
`kubectl delete deployment nginx-depl`
`kubectl delete deployment {deployment-name}`

---

# Advanced kubectl commands

## create or edit config file
`kubectl apply -f nginx-deployment.yaml`
`kubectl apply -f mongo-deployment.yaml`
`kubectl apply -f {config-file}.yaml`

## create or edit service
`kubectl apply -f nginx-service.yaml`
`kubectl apply -f mongo-service.yaml`
`kubectl apply -f {service-file}.yaml`

## create or edit secret
`kubectl apply -f secret.yaml`
`kubectl apply -f {secret-file}.yaml`

## create or edit config map
`kubectl apply -f configmap.yaml`
`kubectl apply -f {configmap-file}.yaml`

## create or edit persistent volume
`kubectl apply -f pv.yaml`
`kubectl apply -f {pv-file}.yaml`

## create or edit persistent volume claim
`kubectl apply -f pvc.yaml`
`kubectl apply -f {pvc-file}.yaml`

## create or edit ingress
`kubectl apply -f ingress.yaml`
`kubectl apply -f {ingress-file}.yaml`

## create or edit network policy
`kubectl apply -f networkpolicy.yaml`
`kubectl apply -f {networkpolicy-file}.yaml`

## create or edit pod security policy
`kubectl apply -f podsecuritypolicy.yaml`
`kubectl apply -f {podsecuritypolicy-file}.yaml`

## create or edit role
`kubectl apply -f role.yaml`
`kubectl apply -f {role-file}.yaml`

## create or edit role binding
`kubectl apply -f rolebinding.yaml`
`kubectl apply -f {rolebinding-file}.yaml`

## create or edit service account
`kubectl apply -f serviceaccount.yaml`
`kubectl apply -f {serviceaccount-file}.yaml`

## create or edit custom resource definition
`kubectl apply -f crd.yaml`
`kubectl apply -f {crd-file}.yaml`

## create or edit custom resource
`kubectl apply -f cr.yaml`
`kubectl apply -f {cr-file}.yaml`

## create or edit job
`kubectl apply -f job.yaml`
`kubectl apply -f {job-file}.yaml`

## create or edit cron job
`kubectl apply -f cronjob.yaml`
`kubectl apply -f {cronjob-file}.yaml`

## create or edit daemon set
`kubectl apply -f daemonset.yaml`
`kubectl apply -f {daemonset-file}.yaml`

## create or edit stateful set
`kubectl apply -f statefulset.yaml`
`kubectl apply -f {statefulset-file}.yaml`

## create or edit pod disruption budget
`kubectl apply -f pdb.yaml`
`kubectl apply -f {pdb-file}.yaml`

## metrics server
`kubectl top nodes`
`kubectl top pods`
`kubectl top pods --all-namespaces`
