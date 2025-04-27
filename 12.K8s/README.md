# 12. Kubernetes. Data. Security

## Homework Assignment 1. Config maps and secrets
1. I've modified my previous file - nginx-deployment.yaml. Add init-container block which performs command and creates index.html for each pod
2. Run nginx-deployment.yaml
```
debian@vbox ~/i/12.K8s (master)> kubectl apply -f nginx-deployment.yaml
deployment.apps/nginx-deployment configured
service/nginx-service unchanged
ingress.networking.k8s.io/nginx-ingress unchanged
```
3. Check changes.
```
debian@vbox ~/i/12.K8s (master)> curl nginx-test.k8s-19.sa                                                                                                                                               
<h1>nginx-deployment-84b8778f85-4b29g</h1>
debian@vbox ~/i/12.K8s (master)> curl nginx-test.k8s-19.sa                                                                                                                                               
<h1>nginx-deployment-84b8778f85-flzl4</h1>
debian@vbox ~/i/12.K8s (master)> curl nginx-test.k8s-19.sa                                                                                                                                               
<h1>nginx-deployment-84b8778f85-4b29g</h1>
debian@vbox ~/i/12.K8s (master)> curl nginx-test.k8s-19.sa                                                                                                                                               
<h1>nginx-deployment-84b8778f85-kgv57</h1>
debian@vbox ~/i/12.K8s (master)> curl nginx-test.k8s-19.sa                                                                                                                                               
<h1>nginx-deployment-84b8778f85-flzl4</h1>
debian@vbox ~/i/12.K8s (master)> curl nginx-test.k8s-19.sa                                                                                                                                               
<h1>nginx-deployment-84b8778f85-kgv57</h1>
```
You may notice that the request goes to different pods  
4. 
