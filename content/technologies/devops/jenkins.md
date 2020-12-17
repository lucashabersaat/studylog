# jenkins

## resources

* Techlab: [https://github.com/carlbalmer/jenkins-techlab](https://github.com/carlbalmer/jenkins-techlab)
* Official: [https://www.jenkins.io/doc/](https://www.jenkins.io/doc/)

## pipelines

* from code to users
* in simple text file, Jenkinsfile

## agent

Agent directive tells Jenkins in which environment to execute the pipeline.

* `agent any`
* `agent { docker { image 'node:14-alpine' } }`

## puzzle best practices

* in post, delete directory:

  ```text
          always {
              deleteDir()
          }
  ```

* `scm checkout` not necessary
* archiveArtefact

  * in options give permissions:  `copyArtifactPermission("/${env.JOB_NAME}")`
  * to save: `archiveArtifacts 'path/todir/or/file/*'`
  * to load:

  ```text
  script {
      step([
          $class: 'CopyArtifact',
          filter: 'path/to/dir/*',
          fingerprintArtifacts: true,
          projectName: env.JOB_NAME,
          selector: [$class: 'SpecificBuildSelector', buildNumber: env.BUILD_NUMBER],
          target: '.'
      ])
  }
  ```

## stages

Stages define phases of the pipeline and consist of single steps.

