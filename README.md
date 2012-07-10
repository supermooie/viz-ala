viz-ala
=======

A standalone web application that interfaces with the Atlas of Living Australia

Installation on Ubuntu 12.04
==============================

Installation instructions on how to set up everything required for development on Atlas of Living Australia on Ubuntu 12.04.

Install grails
--------------

This installs the latest version (2.0.4) by default.

    sudo add-apt-repository ppa:groovy-dev/grails
    sudo apt-get update
    sudo apt-get install grails

Install groovy-2.0.3 (required by ALA)
-------------------------------------

    sudo apt-get install grails-2.0.3
    sudo update-alternatives --config grails

Select 2.0.3 as the active version.

Install groovy
-------------

    sudo add-apt-repository ppa:groovy-dev/groovy
    sudo apt-get update
    sudo apt-get install groovy-2.0

Install tomcat
--------------

    sudo apt-get install tomcat7

Install subversion
------------------

    sudo apt-get install subversion

Obtain ALA Groovy template (If not cloning from Git Repo)
--------------------------------------------------------

    svn co http://ala.googlecode.com/svn/trunk/getstarted viz-ala

Remove SVN fluff (If not cloning from Git Repo)
----------------------------------------------

    cd viz-ala
    find . -type d -name .svn -exec rm -r {} \;

For some reason, tomcat spawns itself after installing - kill it (it runs on port 8080 - the default port that grails runs on).

    sudo pkill tomcat7

Run the web app (on port 8080)
------------------------------

    grails run-app

To specify another port
-----------------------

    grails run-app -Dgrails.server.port.http=<another port>
