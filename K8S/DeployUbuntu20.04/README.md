$ `kubectl apply -f https://raw.githubusercontent.com/gonhvvjvo/Public/master/K8S/DeployUbuntu20.04/Ubuntu20.04.yaml`
pod/jumpod created  

$ `kubectl exec -it jumpod ping 10.244.0.149`  
PING 10.244.0.149 (10.244.0.149): 56 data bytes  