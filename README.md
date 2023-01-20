# repo-backup
A simple kubernetes cronjob that backs up a private github repository in a GCS-bucket in GCP.

## Prerequisites:
- Enable Workload Identity on your GKE cluster: https://cloud.google.com/kubernetes-engine/docs/how-to/workload-identity#enable
- Github Deploy Key for target repository (or an SSH key with read access to the repo): https://docs.github.com/en/developers/overview/managing-deploy-keys#deploy-keys
- A kubernetes secret containing the Private Key from the step above (default name repo-backup-deploy-key)
- a GCP bucket created where you'll store the backups

## How to use
Use this repo as a kustomize base, applying patches in your own repositories to specify which repository and which bucket to back up.

Example of how to use this exists in the directory `kustomize_example/`
