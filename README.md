# repo-backup
A simple kubernetes cronjob that backs up a github repository in a GCS-bucket in GCP.

## Prerequisites:
- Enable Workload Identity on your GKE cluster: https://cloud.google.com/kubernetes-engine/docs/how-to/workload-identity#enable
- Github Deploy Key for target repository (or an SSH key with read access to the repo): https://docs.github.com/en/developers/overview/managing-deploy-keys#deploy-keys
- A kubernetes secret containing the Private Key from the step above (default name repo-backup-deploy-key)