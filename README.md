# Local Istio Gateway

This repo contains configuration to run a completely local Istio with an ingressgateway.
Typically, even when running Istio components outside of Kubernetes, there is still some Kubernetes api-server running somewhere, used as a configuration store.

However, this is not a hard requirement; Istio can run entirely on local configuration.

In this example, we have a local Istiod, a local ingressgateway, and a demo application to handle our ingress request.
Note the demo application does not have a sidecar, although this is also possible.

The demo runs in `docker-compose`. To run it, run `docker-compose up`.
Then, you can run `curl localhost:80` and should see a response.
