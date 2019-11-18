$ kubectl apply -f jumpod.yml  
pod/jumpod created  

$ kubectl exec -it jumpod ping 10.244.0.149  
PING 10.244.0.149 (10.244.0.149): 56 data bytes  