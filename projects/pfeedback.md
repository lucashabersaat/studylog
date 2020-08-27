# pfeedback.md

## setup
1. start frontend: in frontend folder `npm start`
2. start backend: in intellij build & run configuration


## openshift
In the `openshift` folder are all the `.yml` that configure the containers.

To apply the config:
1. login with the openshift cli
2. checkout the right project (prod, dev or test)
3. go to the folder `pfeedback/openshift/scripts`
4. execute `./apply-env.sh prod` (or `test` or `dev`, depending which environment)


### metrics
Go to [Grafana](https://grafana.puzzle.ch/d/85a562078cdf77779eaa1add43ccec1e/k8s-compute-resources-namespace?orgId=1&refresh=10s&var-datasource=prometheus-k8s-cloudscale&var-namespace=pitc-pfeedback-test) to check the resources usage.

## database changes
To add database changes, a changeset must be created. Liquibase is used.
In the folder

`backend/src/main/resources/db/changelog/changelogs`

are the changelog files as xml. There is one for each month. To add a change, add a changeset tag in such a file. The id is year-month-numberofchangeset_in_month.

The syntax is (probably in Advanced Concepts): [https://docs.liquibase.com/concepts/home.html](https://docs.liquibase.com/concepts/home.html)

## tests
### unit tests
wip
### integration tests
(see run config)
1. backend needs to be running
2. `$ BASE_URI=http://localhost:8080 ./gradlew integrationTest clean test`

### e2e tests
wip
### tslint
- TSLint: `$ npm run lint`

## questions
-  where are the tests? do I need to write tests?
- security enabled doesn't work?

## debug
- `$ ng.probe($$('app-new-pfeedback')[0]).componentInstance` life debugging of a component
