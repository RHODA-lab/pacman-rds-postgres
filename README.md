# pacman-rds-postgresql
## To install and run demo
1. Deploy a ROSA cluster on AWS
2. Install the RHODA operator from https://console.redhat.com
3. Get the Access and Secret Key for your Amamzon AWS account and import the a RDS database provider account into RHODA by following by following [this](https://access.redhat.com/documentation/en-us/red_hat_openshift_database_access/1/html-single/quick_start_guide/index#find-your-cockroachdb-account-credentials_rhoda-qsg) guide.
4. Use the RDS Provider Account to create a database instance with DB engine type "Postgresql". This will launch the creation of a Postgresql database under RDS services free-tier services and usually takes around 5 minutes.
5. Create an OpenShift project and create a running Pacman (NodeJS) pod using this repository.
6. Add the RHODA DBaaS Connection into the project and create a Service Binding to the running pod. 
7. Use the route to the Pacman pod and open the game using a web browser. 
