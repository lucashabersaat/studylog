# jenkins

## resources
- Techlab: [https://github.com/carlbalmer/jenkins-techlab](https://github.com/carlbalmer/jenkins-techlab)
- Official: [https://www.jenkins.io/doc/](https://www.jenkins.io/doc/)

## pipelines
- from code to users
- in simple text file, Jenkinsfile

## agent

Agent directive tells Jenkins in which environment to execute the pipeline.
- `agent any`
- `agent { docker { image 'node:14-alpine' } }`

## stages

Stages define phases of the pipeline and consist of single steps.
