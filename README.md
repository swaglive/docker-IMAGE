This template will:
1. Trigger workflow when
    - git push to branch `v*.*.**` and `master`
    - git tag
2. Build a docker image from this repo.
3. Push docker images to different Docker Registry:
  - [Docker Hub]()
  - [GitHub Package](#gitHub-package)
  - [Google Cloud Registry](#google-cloud-registry)

## [GitHub Package](https://github.com/features/packages)
No need to configure.

## [Google Cloud Registry](https://cloud.google.com/container-registry)
- [with `GOOGLE_SA_GCR_JSON`](https://cloud.google.com/container-registry/docs/advanced-authentication#json-key)
    - Need to add `secrets.GOOGLE_SA_GCR_JSON`: Setting -> Secrets -> New secret
- default to `gcr.io/${{ env.GCP_PROJECT_ID }}/${{ github.event.repository.name }}`
