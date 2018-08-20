# release-process 
### release - xxx project
1. we have master and develop branch. for every tasks and feature branch is created. pull request is created for the approval. we merge the feature with develop branch. 
2. tag is created wherever the release is ready. tagged artifacts includes war are to be installed first in dev / stage/ finally in prod.
3. jenkins is configured whenever there is a branch is created. automatic build happens and its artifacts with war is generated. 
4. war in dev branch is pointed to DEV environment / master war is pointed to stage/prod  environment automatically. -- we need to install or automatically installation happens???mostly this might be manual by executing terraform/packer scripts. these scripts will spin up deploy the artifacts into the instances.
5. Change request ticket - create CASD ticket to release management team in ensono ticketing system.
whenever there is new release, this is the process followed. ticket will go to release team. they will review the process like code not change last 1 week, code freeze time, CAB calls they setup and ask everything ready. if all ready they update the ticket as approved.
6. Release plan in excel is circulated by manager.  if any steps to be modified we can provide our comments.
7. during release day - scrum master or manager drives the release. 
8. QA team - gives sign off


# realease - yyy project
1. svn dev branch - for development in local and trunk dev
  when we done with features complete, we create a branch say xxx10.x etc
  this xxx10.x branch is points to stage and production.
  we use go-pipeline for CI/CD. shen we commit code dev branch pipelines are automatically built.
  for deploy we manually tigger.
2. when production, we trigger stage and production pipeline for build and deployment

# CI/CD 
AIm- these days code changes or new features to be in live as soon as possible. 
continuous integration - whenever there is change in code, it should be moved to particular version control system using git or svn. Then testing framework is built because new code shouldnt break any existing features.
CD - continuous deployment - this requires manual intervention to move the deployed code from stage to prod by trigger pipeline
CD - continuous delivery - usually refers even without manual interventions, code go to prod whenever stage is passed.
tools: jenkins, GO pipeline
