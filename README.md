# release-process 
### release - xxx project
1. we have master and develop branch. for every tasks and feature branch is created. pull created is created for the approval. we merge the feature with develop branch. 
2. tag is created eherever the release is ready. tagged artifacts includes war are to be installed first in dev / stage/ finally in prod.
3. jenkins is configured whenever there is a branch is created. automatic build happens and its artifacts with war is generated. 
4. war in dev branch is pointed to DEV environment / master war is pointed to stage/prod  environment automatically. -- we need to install or automatically installation happens???mostly this might be manual by executing terraform/packer scripts. these scripts will spin up deploy the artifacts into the instances.
5. Change request ticket - create CASD ticket to release management team in ensono ticketing system.
whenever there is new release, this is the process followed. ticket will go to release team. they will review the process like code not change last 1 week, code freeze time, CAB calls they setup and ask everything ready. if all ready they update the ticket as approved.
6. Release plan in excel is circulated by manager.  if any steps to be modified we can provide our comments.
7. during release day - scrum master or manager drives the release. 
8. QA team - gives sign off
