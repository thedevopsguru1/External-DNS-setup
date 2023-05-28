# External-DNS-setup-helm
### Helm chart
```
helm repo add my-repo https://charts.bitnami.com/bitnami
```
```
helm repo update
```
#### Create namespace
```
kubectl create ns external-dns
```
```
helm repo add bitnami https://charts.bitnami.com/bitnami
```
##### For linode add the tocken:
```
helm upgrade --install external-dns bitnami/external-dns --namespace external-dns --create-namespace --set provider=linode --set linode.apiToken=$LINODE_API_TOKEN
```
#### Test it by following this link:
https://github.com/thedevopsguru1/external-dns/blob/master/docs/tutorials/linode.md
