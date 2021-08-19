# tkg-concourse-pipelines

### Upgrade Management cluster to version 1.3.1
command to set up upgrade pipeline : 
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
