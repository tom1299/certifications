## Resources
* https://github.com/cncf/curriculum/blob/master/CGOA_Curriculum.pdf
* https://github.com/otkd/CGOA-Study-Guide

## Diary
`14.10.2024`
Look at some of the resources provided:
https://cd.foundation/

## Introduction to GitOps (LFS169)
* Flux in cluster is reconciler agent
* flux fleet repository => What is that => Managed by SRE team / platform contains clusters. Is multitenant
* Reonciler models:
  * Pull model: Watch and apply
    * No external credentials needed (credentials can remain in the cluster)
  * Push model: Hoock and apply
    * Sequencing / Ordering easier
## Ideas
* Setup fleet repo and common infratsructure repo in github => put helm releases there
  * Use air gapped installation method: https://fluxcd.io/flux/installation/configuration/air-gapped/
* User Flagger https://docs.flagger.app/usage/how-it-works for more complex types of deployments
  * Flagger with nginx: https://docs.flagger.app/tutorials/nginx-progressive-delivery
* Flux boostrap cluster and then add components as needed as ingress (with overlays or basee ?)
  * Teams could include components just by adding a kustomization for the component in infra  
  * Mono repo or multi repo => Access rights
  * Problematic: Git history, lots of team members => Git sub modules might help
* Use a local kind cluster with a local registry
* Look at Tekton again
* Continue working on these examples: https://github.com/tom1299/kind-examples