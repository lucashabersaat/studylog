# pfeedback.md

## setup

1. start frontend: in frontend folder `npm start`
2. start backend: in intellij build & run configuration

## structure

```
├── frontend
│   └── ...
├── backend
│   └── src
│   |   ├── app
|   |   |   ├── public
|   |   |   ├── secured
|   |   |   └── shared
│   |   ├── assets
|   |   |   └── i18n  //translations
│   |   ├── environments
|   |   ...
|   ├── ...
|   ...
...
└── ...
```

- to test external paths, send a invitation to an external and check the log of the backend for the url


## openshift

In the openshift folder are all the `.yml` that configure the containers.

To apply the config:
1. login with the openshift cli
2. go to the folder `pfeedback/openshift/scripts`
3. execute `./apply-env.sh prod` (or `test` or `dev`, depending which environment)

### metrics
Go to [Grafana](https://grafana.puzzle.ch/d/85a562078cdf77779eaa1add43ccec1e/k8s-compute-resources-namespace?orgId=1&refresh=10s&var-datasource=prometheus-k8s-cloudscale&var-namespace=pitc-pfeedback-test) to check the resources usage.

## questions
- how to generate a new component, such that it correctly generates stuff in the right subfolders?
-  where are the tests? do I need to write tests?
- security enabled doesn't work?
- angular persistend services -> unsubscribe component from service



## debug

- `$ ng.probe($$('app-new-pfeedback')[0]).componentInstance` life debugging of a component
