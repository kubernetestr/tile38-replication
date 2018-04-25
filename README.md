## Tile38 follower-leader replication using Kubernetes

### First create a namespace:
- `kubectl create namespace tile38`

### Then create the service definitions:
- `kubectl apply -f 01-leader-service.yaml`
- `kubectl apply -f 02-follower-service.yaml`

### Create the deployment for the leader:
- `kubectl apply -f 03-leader-deployment.yaml`

### Wait for leader deployment to be ready. Then:
- `kubectl apply -f 04-follower-config.yaml`
- `kubectl apply -f 05-follower-deployment.yaml`