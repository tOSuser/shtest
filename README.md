# Shtest - A simple test framework for shell scripts such as sh/bash/groovy

## License
license AGPL-3.0 This code and the package of Shtest are free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License, version 3, as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License, version 3, along with this program. If not, see http://www.gnu.org/licenses/

## A short background
I use to recode times sepent for stories/cards when I work on a project by using time tracker tools.
It helps to analyze jobs and improving way of workings for next steps and future projects.

During a test automation job to automate E2E tests/ and improving a continuous testing flow I realize
that the time spent to fix shell scripts bugs and issues (in this case the scripts that mostly were coded on
bash and groovy) is more than 40% of the total recoded times.

Scripts usually are not so complicated. The main idea of using a script is to packaging a group of commands
needed to be run together to have a certain output.
In the case of scripts for a automation flow such as CI flow, CD or CT flow, most challenges are
values used by scripts.
Most of values and parameters are generated by hosts (such as Jenkins, gerrit...) that scripts run under.
Moreover accesses and permissions can make it little bit more complicated, for example when a script is run by Jenkins
that the Jenkins it self is run under Tomcat.

Anyways a WOW optimization was started and the first idea was to use a real test system for scripts to decrease numbers of faced issues after being implemented to the main flow.

## What Shtest is
Shtest is a practical framework to develop tests for shell scripts such as sh/bash/groovy.
The framework contains several principals and also a set of pre-coded tools to write and running tests.
Currently Shtest is published as a part of RepoUtils (a multi languages CI/CD/CT flow manager) and can be not installed
as a separated package.

# An overview of Shtest
Shtest is based on a very simple idea and the tools provided Shtest helps to automate steps to make it faster and more structured.

Using Shtest framework itself does not need necessary to install Shtest package but having Shtest package can automate several of the steps on the simple example below. 
The test framework is mostly about following principles.

## Jenkinsjob - A very simple example
This example shows how to test a script that is developed to use with in a groovy script.
The groovy script used by this example is only one line that calls a bash script and it is not considered by this example.

* `jenkinsjob.sh` - The main script
* `jenkinsjobshelper.shinc` - provide some helper functions used by `jenkinsjob.sh`
* `jenkinsjob.test.sh` - `jenkinsjob.sh` tests

need-to-be-updated
