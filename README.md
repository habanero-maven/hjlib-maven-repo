Maven repository hosted in Github for COMP 322 @ Rice University.

If you have push access to this repo, the process for deploying a new version of
HJlib to it is as follows:

1. Make sure you have the version of HJlib you want to deploy and cd to its root
   folder, which contains the pom.xml.
2. Verify that the pom.xml for the HJlib version you are working with is using
   the site-maven-plugin Maven plugin targeting the hjlib-maven-repo Github
   repo. If it does not, you may be using a version of HJlib that does not
   currently support deploying to Github.
3. Update the pom.xml to a new version number by changing the value inside the
   <version> tags. This will automatically change the version number of both the
   generated JAR and the target Github repo.
4. Run 'mvn deploy' to send the latest bits up to Github.
5. Update any pom.xml files for local projects to point to the new Github branch.
