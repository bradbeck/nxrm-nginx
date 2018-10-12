# bradbeck/nxrm-nginx

## Description
An example nginx reverse proxy for an nxrm service running in a docker swarm overlay network. Nginx interacts with the overlay load balancer to access the nxrm service. This approach allows for a static nginx configuration as the number nxrm replicas is changed.

## Running
```
docker service create --name nginx --replicas 1 --network appnetwork -p 8081:8081 bradbeck/nxrm-nginx
```
