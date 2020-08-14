This template will:
1. Trigger workflow when
    - git push to branch `dev`
    - git tag
2. Build a docker image from this repo.
3. Push docker images to [Google Cloud Registry](https://cloud.google.com/container-registry)
    - with `GOOGLE_SA_GCR_JSON`
    - to `asia.gcr.io/swag-2c052/${{ github.event.repository.name }}`

## Prerequisites
- Add `secrets.GOOGLE_SA_GCR_JSON`: Setting -> Secrets -> New secret
