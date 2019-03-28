Getting Started with OpenShift Sample Application
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

** oc new-app 
** oc new-app -L
