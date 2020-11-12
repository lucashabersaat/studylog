---
description: container application platform
---

# openshift

## references

* E-Book [Openshift for Developers](https://www.openshift.com/resources/ebooks/openshift-for-developers)

## session mit raffi

_12.11.2020_

Template: sammlung von resource, 

* containers, docker, docker-compose
  * VM have own OS, container share one and only have differences
* openshift: orchestriert wie container zusammenarbeitet
  * Vorteil: skalierbarkeit
  * deployment config: sagt wie deployment aussieht
  * deployment 
  * deployment is finally in a pod
  * pod can be one or more containers
* Resource
  * deployment config
    * apiVersion
    * metadata
    * name: alles kann name haben
    * labels: vereinfacht verwaltung
      * zb application label
      * zb database label
    * spec: eigentliche daten
      * replica: \#þods
      * sekectir; einfacher zum anwählen
      * strategy: wie deployed wird
        * recreate: alt komplett down, dann neue up \(gut wenn man kein downtime will\)
        * rolling: ohne unterbrüche, ein nach em anderen down dann up \( heikel bei zb db\)
      * template: was wir ddeployed
        * spec:
          * container: hier sind alle container drin
            * env: env variablee
            * image
            * liveness/readiness probes:
            * ports
            * resources: welche ein Pod brauchen kann
    * triggers: wenn automatisches deploy getriggered wird
      * zb image change, configf change
  * image
  * service
    * einfach ein Netzwerkabstraktion von pods oder dep-conf
    * können dann innerhalb im subntz mit namen ansprechen
  * routes
  * imagestream
    * platz ide registry
  * persistenvolumeclaim

## questions

* mal ein Secrets

## commands

* oc project
* oc help
* oc process \(
* oc process -f \[filepath.yml\] \| oc apply -f -
* oc get \[pods\|secrets\|projects\] \[-w\]
* `oc apply -f [filepath] --dry-run` _simulate apply to check for syntax error_



imagestream fehlt

* docker pull 
* docker login registry.ocp.puzzle.ch -u lhabersaat -p $\(oc whoami -t\)
* docker tag postgres:11.9 registry.ocp.puzzle.ch/lh-openshift-test/postgres:11.9

\_\_

\_\_

