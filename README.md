viz-ala
=======

A standalone web application that interfaces with the Atlas of Living Australia

Installation from Ubuntu 12.04
------------------------------

Installation instructions on how to set up everything required for development on Atlas of Living Australia on Ubuntu 12.04.

Install grails

This installs the latest version (2.0.4) by default.

    sudo add-apt-repository ppa:groovy-dev/grails
    sudo apt-get update
    sudo apt-get install grails

Install groovy-2.0.3 (required by ALA)

    sudo apt-get install grails-2.0.3
    sudo update-alternatives --config grails

Select 2.0.3 as the active version.

Install groovy

    sudo add-apt-repository ppa:groovy-dev/groovy
    sudo apt-get update
    sudo apt-get install groovy-2.0

Install tomcat

    sudo apt-get install tomcat7
