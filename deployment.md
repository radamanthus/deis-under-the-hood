# Deis Deployment
-
`git push deis master`

Deis deployment is described in these documents:

- [Using Buildpacks](http://docs.deis.io/en/latest/using_deis/using-buildpacks/)
- [Understanding Deis: Concepts - Build, Release, Run](http://docs.deis.io/en/latest/understanding_deis/concepts/#build-release-run)

![](http://docs.deis.io/en/latest/_images/DeisGitPushWorkflow.png)

The documentation for the [Builder] (http://docs.deis.io/en/latest/understanding_deis/components/#builder) component describes what goes on in Builder during deployment. Let's use that as a starting point and dig into what goes on under the hood during deployment:

1. Builder receives the git push and triggers the pre-receive git hook

  ![](https://raw.githubusercontent.com/radamanthus/deis-under-the-hood/master/assets/deployment-step-1.png)

2. Builder creates a new Docker image

  asdf
  
3. Builder retreives the latest Config from Controller, and adds it to the Docker image

  asdf

4. Builder pushes the new Docker image to the Registry

  asdf

5. Triggers a new Release through the Controller

  asdf