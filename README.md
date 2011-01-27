cuke4php
========

This project implements the cucumber wire protocol for PHP projects.
Information about the wire protocol: http://wiki.github.com/aslakhellesoy/cucumber/wire-protocol

Using this protocol it is possible to directly interact with PHP code at any level without the need for a web server.  To accomplish this, when cucumber is running against a directory containing feature files and it cannot resolve a particular step definition, it will ask a known wire server (as defined in a .wire file) to interpret and run those steps.

Install
-------
To install Cuke4Php, follow these steps:

* clone
* install dependencies with bundler
* run rake build
* install gem under pkg/ folder

Usage
-----
* run 'cuke4php path/to/features' from the command line
* make sure your cucumber features has a 'Cuke4Php.wire' file containing the appropriate information (copy the one in cuke4php/features/step_definitions)
* you can write both Ruby and PHP steps
* you should load phpunit from a file in step_definitions/support/

Roadmap
-------

### bin/cuke4php

* support an option like 'cuke4php --init' which will generate the directory structure and support files necessary to use cuke4php with a php project.
* autodetect an available port and then use it to run the cuke4php server pass this on to cucumber by setting an environment variable (requires a modification to cucumber)

### Rakefile

* once the patch for erb templating in .wire files is released, we should set a minimum version for it

Dependencies
------------
* PHPUnit >= 3.0 (see http://www.phpunit.de/)

Goals
-----
This project utilizes PHPUnit because it has a robust set of assertions, has good mocking, and is widely used.  This will facilitate adoption by developers who are already familiar with it.

This project was developed against the 5.2.x versions of PHP, to ensure compatibility with older PHP projects.

Support
-------
	Support for this project was provided by iContact, inc.  (http://www.icontact.com)

Contributors
------------
	Kevin Olbrich, Ph.D. (kevin.olbrich+cuke4php@gmail.com)
	Alessandro Dal Grande (aledelgrande@gmail.com)