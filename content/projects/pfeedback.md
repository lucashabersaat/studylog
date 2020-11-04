---
description: A feedback tool developed by Puzzle ITC.
---

# pfeedback

`web-app` `angular` `spring` 

## setup development environment

1. start frontend: in frontend folder `npm start`
2. start backend: in intellij build & run configuration

## openshift

### apply the config

1. login with the openshift cli
2. checkout the right project \(prod, dev or test\)
3. go to the folder `pfeedback/openshift/scripts`
4. execute `./apply-env.sh prod` \(or `test` or `dev`, depending which environment\)

To apply the config: 1. login with the openshift cli 2. checkout the right project \(prod, dev or test\) 3. go to the folder `pfeedback/openshift/scripts` 4. execute `./apply-env.sh prod` \(or `test` or `dev`, depending which environment\)

### metrics

Go to [Grafana](https://grafana.puzzle.ch/d/85a562078cdf77779eaa1add43ccec1e/k8s-compute-resources-namespace?orgId=1&refresh=10s&var-datasource=prometheus-k8s-cloudscale&var-namespace=pitc-pfeedback-test) to check the resources usage.

## database changes

To add database changes, a **changeset** must be created. Liquibase is used. In the folder

`backend/src/main/resources/db/changelog/changelogs`

are the changelog files as `xml`. There is one for each month. To add a change, add a changeset tag in such a file. The _id_ is year-month-numberofchangeset\_in\_this\_month.

The syntax is \(probably in Advanced Concepts\): [https://docs.liquibase.com/concepts/home.html](https://docs.liquibase.com/concepts/home.html)

### on deployed db

To change something on the deployed db on the postgres pod, login with psql in the pod terminal: `psql -U pfeedback`

or general when having the pfeedback database locally on the machine \(cross reference postgres commands...\) `psql -U pfeedback -d pfeedback -h localhost -p 5432`

## tests

### unit tests

wip

### integration tests

\(see run config\) 1. backend needs to be running 2. `$ BASE_URI=http://localhost:8080 ./gradlew integrationTest clean test`

### e2e tests

To run tests, execute in _/frontend_ `$ ng e2e` will run the e2e tests defined in _/frontend/e2e_. It will first start the frontend server, `ng serve` and then run the tests. The backend needs to run aswell. The e2e tests are run using **Protractor** and run configs can be created for Protractor. It also uses the **Jasmine** test library.

{% embed url="https://www.protractortest.org/\#/api?view=ProtractorBrowser" %}

{% embed url="https://jasmine.github.io/index.html" %}

### tslint

* TSLint: `$ npm run lint`

## questions

* where are the tests? do I need to write tests?
* security enabled doesn't work?

## swagger ui

This is an automatically generated documentation of the api. [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

[http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

## debug

* `$ ng.probe($$('app-new-pfeedback')[0]).componentInstance` life debugging of a component in browser
