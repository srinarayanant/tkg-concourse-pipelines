# tkg-concourse-pipelines

### Upgrade Management cluster to version 1.3.1
command to set up management cluster upgrade pipeline : 
```
fly -t tkg set-pipeline \
    -p pipe \
    -c tkg-mgmt-cluster-upgrade.yml \
    -v github.mgmt_ctx.repo.url=<<mgmt_context_github_repo_url>> \
    -v github.mgmt_ctx.repo.branch=<<mgmt_context_github_branch_name>> \
    -v github.username=<<github_username>> \
    -v github.personal_access_token=<<github_personal_access_token>> \
    -v github.mgmt_ctx.file_name=<<mgmt_cluster_context_filename>> \
    -v tkg.mgmt_cluster.ctx.name=<<mgmt_cluster_context_name>> \
    -v tkg.mgmt_cluster.name=<<mgmt_cluster_name>>
```

### Upgrade Kubernetes cluster to version 1.3.1
command to set up kubernetes upgrade pipeline : 
```
ly -t tkg set-pipeline \
    -p pipe \
    -c tkg-k8s-cluster-upgrade.yml \
    -v github.mgmt_ctx.repo.url=https://github.com/nkumar5-vmw/context \
    -v github.mgmt_ctx.repo.branch=main \
    -v github.username=nkumar5-vmw \
    -v github.personal_access_token=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 \
    -v github.mgmt_ctx.file_name=tkg-mgmt-ctx \
    -v tkg.mgmt_cluster.ctx.name=tkg-mgmt-admin@tkg-mgmt \
    -v tkg.mgmt_cluster.name=tkg-mgmt \
    -v tkg.k8s_cluster.name=nkm \
    -v tkg.k8s_cluster.namespace=nkm 
```
