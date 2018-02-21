# groovyoscp - Examples using the Openshift Jenkins Pipeline (DSL) plugin

## Overview
Repo for example Groovy Scripts for Jenkins [Openshift](https://openshift.com) [Pipeline](https://jenkins.io/solutions/pipeline) Client DSL plugin.

This repo contains some template buildconfig yaml for setting up the buildconfigs, and then some clean
groovy scripts that can either be added manually to the pipeline *or* can be setup as direct git pulls
as part of a pipeline strategy buildconfig (this is the suggested way to do it)

## Installation
Follow the instructions for setting up the plugin [here](https://github.com/openshift/jenkins-client-plugin) - I cloned and built the 
plugin, then added it via the Plugin Manager tab on the Jenkins UI. The only issue I had is that you should disable the existing Openshift Pipeline
plugin, then update the Pipeline plugin to 2.5. I run the Jenkins pod via the official 3.7 template available [here](https://github.com/openshift/openshift-ansible/blob/master/roles/openshift_examples/files/examples/v3.7/quickstart-templates/jenkins-persistent-template.json)

![Jenkins Configuration](screenshots/jenkins.png "Plugin configuration for Jenkins (note, I built the plugin myself)")

## Examples
These are a work in progress, but there are a number of example scripts in the examples folder. To run these, use the template.yaml from the templates folder
to create a buildconfig with the pipeline strategy (change the name of the build in the file then run 'oc create -f (filename)' in the appropriate namespace), then edit the buildconfig in the Openshift UI and cut and paste the entire script into the pipeline.
