# REDIS Helm chart

## Info

* This is a very simple chart intented to be used during development only in a local environemnt containing K8s deployment into docker-desktop
* Setup does not use perstistent storage

## Usage

* Run `helm install test-redis .`
* Use `kubectl get svc` to list services
  * `test-redis-service                                      LoadBalancer   10.110.173.242   localhost     6379:31901/TCP    3m7s`
  * From within the cluster use DNS resolution `test-service.default.svc.cluster.local`
  * `default` refers to K8s namespace used for deployment
  * `test-redis` refers to helm deployment name
  * REDIS is exposed as a service on localhost port 6379 as well so can be used directly during development
