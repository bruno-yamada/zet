# Kubernetes Pod placement

We have 5 basic methods:

## Node Selector
Assign pods to nodes based on labels, although Node Affinity might be better

## Node Affinity
Better syntax than nodeSelector

## Inter-pod affinity
Allocate pods based on other related pods

## Pod anti-affinity
Good for high-availability, ensuring pods are spread out across the nodes

## Taints and tolerations
Helps ensure nodes are used only for a certain purpose (eg. GPU enabled or BIG nodes)

> tags: k8s; kubernetes; pods;

> uid: 20220126205927Z

> links: 

