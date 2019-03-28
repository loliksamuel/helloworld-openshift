Prerequisites
================
In order to deploy the CoolStore microservices application, you need 
* brew cask install minishift 
* procees with https://docs.okd.io/latest/minishift/getting-started/quickstart.html
* oc cluster up
* https://192.168.64.2:8443/console

run Application
====================
* openshift cli tutorial : https://github.com/openshift/origin/blob/master/docs/cli.md
* minishift addons install /Users/samuelcardonis/Documents/projects/openshift/minishift-addons/add-ons/grafana/
* minishift addon apply grafana --addon-env namespace=kube-system
* oc new-app --name=helloworld wildfly~https://github.com/loliksamuel/openshift-helloworld.git --display-name="Web Team Development" --description="Development project for the web team."
* oc new-app -L
* oc get is -n openshift
* oc new-app helloworld~https://github.com/loliksamuel/helloworld-openshift.git
* oc status
* oc expose service hellosvc (expose a route or a load ballancer)
* oc start-build helloworld -n helloworld
* oc describe bc/helloworld -n helloworld
* oc tag dev/helloworld:latest test/helloworld (copy dev env to test env)
* oc get pod -n helloworld
* oc logs helloworld-6-krnq4 -f -n helloworld
* oc 
* oc whoami
* oc logout

blue green deployment
========================
* create another branch helloGermany
* change html to germany
* git commit -m "My application changes"
* git push origin master
* create another app germany
* create route
* oc start-build helloworld -n helloworlds
* curl http://helloworld-helloworld.192.168.64.2.nip.io/
* u should see germany
* curl http://helloworld-helloworld.192.168.64.2.nip.io/
* u should see israel
* note: it will not work from browser due to sticky sessions. only from cli

Troubleshooting
================
* https://learn.openshift.com

