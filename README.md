# ocp-deploy-test

## deploy application
```
oc new-project eap-demo
oc replace --force -f https://raw.githubusercontent.com/jboss-openshift/application-templates/master/eap/eap71-image-stream.json
oc new-app https://github.com/ataranai/ocp-deploy-test --image-stream=jboss-eap71-openshift:latest
```

## delete application
```
oc delete all -l app=ocp-deploy-test
```
