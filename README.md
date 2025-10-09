# iac-demo
Infrastructure-as-Code demo repo for ArgoCD

\
Prerequisites:
- ArgoCD FQDN (argocd.site-a.vcf.lab) is in DNS
- You are alrady connected to the Supervisor context (vcf context use sup-wld)

```
cd ~/Downloads
gzip -d argocd-cli-linux-amd64-v2.14.15-vcf.gz
sudo install argocd-cli-linux-amd64-v2.14.15-vcf /usr/local/bin/argocd
argocd admin initial-password  #copy the password from the output
argocd login argocd.site-a.vcf.lab --username admin  #paste the password when prompted
argocd account update-password --account admin
argocd cluster add sup-wld --namespace argocd
