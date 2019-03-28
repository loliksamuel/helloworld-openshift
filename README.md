Prerequisites
================
In order to deploy the CoolStore microservices application, you need 
* brew cask install minishift 
* procees with https://docs.okd.io/latest/minishift/getting-started/quickstart.html
* oc cluster up


run Application
====================

This is a sample application for the book, Getting Started with OpenShift
blue green deployment:
* create another branch helloGermany
* change html to germany
* commit
* create another app germany
* create route
* curl http://helloworld-helloworld.192.168.64.2.nip.io/
* u should see germany
* curl http://helloworld-helloworld.192.168.64.2.nip.io/
* u should see israel
* note: it will not work from browser due to sticky sessions

openshift cli tutorial : https://github.com/openshift/origin/blob/master/docs/cli.md
* minishift addons install /Users/samuelcardonis/Documents/projects/openshift/minishift-addons/add-ons/grafana/
* minishift addon apply grafana --addon-env namespace=kube-system
* oc new-app --display-name="Web Team Development" --description="Development project for the web team."
* oc new-app -L
* oc get is -n openshift
* oc new-app helloworld~https://github.com/loliksamuel/helloworld-openshift.git
* oc status
* oc expose service sinatra (expose a route)
* oc start-build helloworld -n helloworld
* oc describe bc/helloworld -n helloworld
* oc tag dev/helloworld:latest test/helloworld (copy dev env to test env)
* oc get pod -n helloworld
* oc logs helloworld-6-krnq4 -f -n helloworld
* oc 
* oc whoami
* oc login
