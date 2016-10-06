System testing
==============
Before a new version of Zonemaster can be released it must pass three levels of
system testing: Installation Testing, Smoke Testing and Acceptance Testing.
Each test level is described in a separate section below. A separate section is
reserved for the concept of Configurations, which is used by other sections.


## 1. Configurations

The purpose of configurations is to provide different contexts for the tests to
run in.

A configuration is a tuple of the following parameters:

* architecture (e.g. x86_64)
* operating system version (e.g. Ubuntu 14.04)
* database engine version (e.g. PostgreSQL 9.3)
* system locale (e.g. en_US.UTF-8)
* Perl version (e.g. 5.20)

The set of possible values for the following configuration parameters (except
for system locale) are declared in the README.md of the top-level zonemaster
repository.

The set of possible values for the system locale configuration parameter is:
* C
* sv_SE.UTF-8


## 2. Installation testing

This test level validates that all components of Zonemaster can be installed
according to their respective installation instructions.


### Configurations

The set of configurations must include at least:
* One configuration for each supported architecture.
* One configuration for each supported operating system version.
* One configuration for each supported database engine version.


### Procedure

For each configuration:

1. Prepare a machine
   1. Allocate a machine with the architecture specified by the configuration.
   2. Install the OS as specified by the configuration on the machine.

2. Install Zonemaster Engine
   1. Follow the installation instruction at zonemaster-engine/docs/installation.md
      to the letter.
   2. Perform a sanity check.

      ```
      time perl -MZonemaster -e 'print scalar Zonemaster->test_zone("zonemaster.net"), "\n"'
      ```

      The command is expected to take very roughly 15 seconds and print a number
      greater than one.

3. Install Zonemaster Backend
   1. Follow the installation instruction at zonemaster-backend/docs/installation.md
      to the letter.
   2. Perform a sanity check. 

      ```
      curl -s -H "Content-Type: application/json" -d '{"jsonrpc":"2.0","method":"version_info","id":"1"}' http://localhost:5000/ && echo
      ```

      The command is expected to give an immediate JSON response.

4. Install Zonemaster GUI
   1. Follow the installation instruction at zonemaster-gui/docs/installation.md
      to the letter.
   2. Perform a sanity check. Point your browser to this URL:

      ```
      http://localhost/
      ```

      You should be presented with a page showing, among other things the
      Zonemaster logotype.

5. Install Zonemaster CLI
   1. Follow the installation instruction at zonemaster-cli/docs/installation.md
      to the letter.
   2. Perform a sanity check.

      ```
      zonemaster-cli --version
      ```

      The command is expected to list various version number information.


## 3. Smoke testing

This test level validates that fundamental use cases:

* work independent of specific configurations
* weren't broken by new changes


### Configurations

... To be specified.


### Procedure

For each configuration:

1. Prepare an installation

2. Smoke test of Zonemaster CLI

   ... Test a number of basic/important use cases.

3. Smoke test of Zonemaster GUI

   ... Test a number of basic/important use cases.


## 4. Acceptance testing

This test level validates that new changes:

* work independent of specific configurations
* weren't broken by other new changes


### Configurations

...


### Procedure

1. Prepare an installation

2. Acceptance testing through Zonemaster CLI

   ... Test each new entry in the zonemaster-cli and zonemaster-engine components.

3. Acceptance testing through Zonemaster GUI

   ... Test each new entry in the zonemaster-gui, zonemaster-backend and zonemaster-engine components.
