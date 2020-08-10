Sample GitOps repo for automated deployments to Kubernetes. This project uses [Flux](https://github.com/fluxcd/flux). It is set up to automatically scan for any update on `mohtar/hello-world` repository and roll out the appropriate deployment (it is assumed that the Docker image is produced under a proper CI/CD pipeline with rigorous reviews and tests).

Live deployment is available here: http://188.166.206.110/

[Traefik](https://containo.us/traefik/) is used as ingress, providing compression and TLS termination.

For cost reasons, the following techniques are not employed, but the necessary config is provided and commented out:

* Node affinity
* TLS
* Auto-scaling

The following are also nice-to-haves in a Kubernetes cluster but missing:

* Central logging
* Monitoring
