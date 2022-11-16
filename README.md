## Deploy image on EKS 

This workflow will help you to automatically push image to ECR with unique tags on each code push on Github repository and then deploy that image on EKS . 

You need to integrate this workflow on your repo and chnage the *branch-name* accordingly.
Update the file according to your requirements and also update these secrets on your Github Secrets
- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- KUBE_CONFIG_DATA_DEV

KUBE_CONFIG_DATA – A base64-encoded kubeconfig file with credentials for Kubernetes to access the cluster. You can get it by running the following command:
```cat $HOME/.kube/config | base64 ```
Make sure that your `$HOME/.kube/config` doesn't contain a AWS_PROFILE, i.e. remove the following section if it exists before doing the base64 encoding
Update the file according to your requirements.
