# Easy deploy for test


`kubectl run hello-kubernetes --replicas=3 --image=paulbouwer/hello-kubernetes:1.5 --port=8080`
# ควรจะใช้ 
`kubectl create deployment hello-kubernetes --image=paulbouwer/hello-kubernetes:1.5`
หรือ
`kubectl run --generator=run-pod/v1 hello-kubernetes --replicas=3 --image=paulbouwer/hello-kubernetes:1.5 --port=8080`
# expose service
`kubectl expose deployment hello-kubernetes --type=LoadBalancer --port=80 --target-port=8080 --name=hello-kubernetes`

