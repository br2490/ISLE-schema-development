Current setup does this:

## Network

Uses a defined network to contain sql for all

`docker network create isle-static` 

## SQL

In the main directory there is a docker-compose.yml to launch a single instance of mysql.

`docker-compose up -d` 

## Default folder's role.

In the `default` directory the default configurations from the relevant containers for the CURRENT TASK are placed.

Open this docker-compose, take note of the PORTS. localhost:8080 for fedora, localhost:8081 for solr.

`docker-compose up -d` runs SOLR and FEDORA images.  The configurations that are loaded for this are the config-sets folder. 

Browse to http://localhost:8080/fedoragsearch/rest - DEFAULT username/password: fedoraAdmin / ild_fed_admin_2018


## Make copies of `test-master` named something you will remember as you add more tests (e.g., `test-01, test-02, test-03`)

In the "`test-01`" directory (and all others you created)

Open this docker-compose, take note of the PORTS. localhost:8082 for fedora, localhost:8083 for solr. - ADVANCE THESE AS YOU ADD MORE TESTS.

 The configurations that are loaded for this are the config-sets folder. **Make changes to files on the host as you would normally.**

`docker-compose up -d` runs SOLR and FEDORA images with your settings.

Browse to http://localhost:8082/fedoragsearch/rest - DEFAULT username/password: fedoraAdmin / ild_fed_admin_2018

`updateIndex from foxml`


Repeat!

