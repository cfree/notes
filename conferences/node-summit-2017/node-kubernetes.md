# CICD with Node and K8s

CI - merge all developer workingcopies to a shared mainline several times a day

CDelivery - Ensure that your code can be shipped at any time. Requires CI
CDeployment - Every change is automatically deployed to prod. Requires CDelivery

Goal - have updated code in prod asap.

Spinnaker - CD for everyone. Multi-cloud, open source CD platform

Canary - metrics to determine if red or black. Fallback if failing
TravisCI + Spinnaker vs Jenkins?

Container Builder to build container 
Cloudbuild.yaml

Cloud Launcher - deploy VMs. Add to k8s cluster
Create load balancer
    Staging env
    Production env

Create pipelines
    Deploy to stage
    Validate stage
    Deploy to prod
    
Where does Spinnaker live?

spinnaker.io/guides/tutorials/codelabs/gcp-kubernetes-source-to-prod
medium.com/@sandeepdinesh
twitter.com/sandeepdinesh

