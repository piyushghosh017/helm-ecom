apt install nginx 
helm repo add bitnami https://charts.bitnami.com/bitnami
helm search repo bitnami | grep nginx
helm install nginxv1 bitnami/nginx --set pdb.create=false 
#Instance of a release

helm repo add eks https://aws.github.io/eks-charts
helm repo update eks
helm search repo eks
helm search repo eks | grep load

helm uninstall nginxv1

helm package payment
helm package shipping


# helm status
kubectl get secrets -n aurmlyurzmebyygcle | grep helm
helm status nginxv1 -n aurmlyurzmebyygcle

