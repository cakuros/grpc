[This code's documentation lives on the grpc.io site.](https://grpc.io/docs/quickstart/python.html)


# Deploying to Kubernetes with Ambassador

The Dockerfile in this directory can be used to containerize the `greeter_server.py` for deployment to kubernetes.

After packaging and pushing the greeter_client container, you will need to edit the `m.yaml` file which holds the `Deployment` and `Mapping` YAML for the server


Use `kubectl` to deploy this to your cluster with Ambassador installed.

After deploying it to your cluster, edit the `greeter_client.py` to use the domain name or IP address of your Ambassador service to connect to the server running in your cluster

**Note:** At the moment, the client expects only a cleartext connection. You will either have to edit the client to use a secure channel or make sure Ambassador is able to serve cleartext
