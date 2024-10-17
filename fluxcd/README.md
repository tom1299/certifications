## Repository structure:
### Pros and cons
* Self-service <-> Manual
=> For multi tenancy use this:
https://github.com/fluxcd/flux2-multi-tenancy

## Delivery management 
> New app release can be automatically delivered to staging using Flux’s image updates to Git. For production, you may choose to manually approve app version bumps by configuring Flux to push the changes to a new branch from which you can create a pull request. You can limit the impact of an issue that escaped staging testing by using Flagger’s canary releases.

Implement above
Try watching for changes: https://fluxcd.io/flux/gitops-toolkit/source-watcher/