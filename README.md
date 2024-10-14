# DevOps-Project

Github Actions Workflow

Approach to use to authenticate b/w Google Cloud and Github 
: OIDC authentication, for authenticating to our Google Cloud 

for that we'll use this action 

```
    steps:
    - uses: 'actions/checkout@v3'
    - id: 'auth'
      name: 'Authenticate to Google Cloud'
      uses: 'google-github-actions/auth@v1'
      with:
        token_format: 'access_token'
        workload_identity_provider: 'projects/886257991781/locations/global/workloadIdentityPools/k8s-pool/providers/k8s-provider'
        service_account: 'tf-gke-test@$GCP_PROJECT_ID.iam.gserviceaccount.com'
```
