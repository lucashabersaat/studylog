# cryptopus

## Local Containering

* [x] merge messages to stable
* [ ] Bug: Account Show does not hide PW
  * [x] fixed
  * [x] test int
  * [ ] merge
* Bugs:
  * Login CSS not loading and after login not redirecting.
  * rails frontend resources not loaded, because hash is missing
  * works on integration

### docker cry

im Docker-compose auf :stable docker-compose up -d

* dockerfile anpassen: SERET\_KEYBASE='airgendwers'
* docker build -t local\_image\_name:stable .
* docker-compose.yml im image den namen von oben
* Um zu Bash im container auszuführen:
  * docker exec -it cryptopus-sqlite \bin\bash
* Im: config/docker/mysqli/docker-comose.yml
  * Rails\_HOST\_SSL auskommentieren
  * unter ports: localhost rausnehmen
  * config/docker/mysqli/mysql-pred.env, tempt raushemen umbennnen
* railsdbpw aund mysq\_ root\_passwrd üssen gleich sein
* secret key base vom docker-compose.yml von cry
* 10&11 im container ausführen.

_Siehe branch stable-testing_

### rollback:

* [Rollback Doc](https://docs.openshift.com/container-platform/3.11/dev_guide/deployments/basic_deployment_operations.html#rolling-back-a-deployment)

