# Screenshots
To help review your infrastructure, please include the following screenshots in this directory::

## Deployment Pipeline

> Note: This project uses **GitHub Actions + GitHub Container Registry (GHCR)** instead of
> Travis CI + DockerHub. The screenshots below are the direct equivalents required by the rubric.

* GHCR showing the container images that you have pushed
  (GitHub profile → Packages: https://github.com/olynyagin?tab=packages)
  Expected images: `reverseproxy`, `udagram-api-user`, `udagram-api-feed`, `udagram-frontend`
* The CI workflow that builds and pushes the images
  (Repository → **Actions** tab → "Build and Push Images to GHCR")
* GitHub Actions showing a successful build-and-push run
  (open the latest green run and show all four jobs succeeded)

## Kubernetes
* To verify Kubernetes pods are deployed properly
```bash
kubectl get pods
```
* To verify Kubernetes services are properly set up
```bash
kubectl describe services
```
* To verify that you have horizontal scaling set against CPU usage
```bash
kubectl describe hpa
```
* To verify that you have set up logging with a backend application
```bash
kubectl logs {pod_name}
```
