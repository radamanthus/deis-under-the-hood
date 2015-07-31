# Create an application
-
`deis create`

- [http://docs.deis.io/en/latest/using_deis/deploy-application]()
- [http://docs.deis.io/en/latest/using_deis/using-buildpacks]()

1. `deis` client calls the controller API

  ![](https://raw.githubusercontent.com/radamanthus/deis-under-the-hood/master/assets/create-application-step-1.png)

2. `controller` creates a new row for the application in the `api_app` table of the `deis` database

  ![](https://raw.githubusercontent.com/radamanthus/deis-under-the-hood/master/assets/create-application-step-2.png)

3. `controller` creates the `/deis/services/<app_name>` key in `etcd`

  ![](https://raw.githubusercontent.com/radamanthus/deis-under-the-hood/master/assets/create-application-step-3.png)