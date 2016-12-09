# CLI Security Tools

## !!WARNING!!

You should not run these tools against any systems you don't own, or don't have
permission to test. These tools are for legitimate security testing only. Using
them against unauthorized systems could result in criminal penalties.

-----

## Infrastructure

### SSL

- [**testssl.sh**](https://testssl.sh/) - SSL configuration testing (bash)
- [**sslyze**](https://github.com/nabla-c0d3/sslyze) - SSL configuration testing (python)
- [**cipherscan**](https://github.com/jvehent/cipherscan) - get ciphers/etc used by an SSL/TLS endpoint
- [**TLSlayer**](https://github.com/thanasisk/TLSlayer) - get ciphers/etc used by an SSL/TLS endpoint

### General

- [**nmap**](http://nmap.org) - Port scanning
- [**enumXFF**](https://github.com/infosec-au/enumXFF) - Enumerate 'X-Forwarded-Headers' to bypass restrictions

## Security Misconfiguration / "Oopsies"

- [**Lynis**](https://cisofy.com/lynis/) - Test VMs/servers/etc. for CIS best practices
- [**Docker-Bench**](https://github.com/docker/docker-bench-security) - Test for Docker containers for CIS best practices
- [**gitrob**](https://github.com/michenriksen/gitrob) - Search git repositories for juicy info
- [**nsec3map**](https://github.com/anonion0/nsec3map) - Tool to enumerate resource records of a DNS zone using DNSSEC NSEC/NSEC3 chain

## Static Analysis

### JavaScript

- [**Retire.js**](http://bekk.github.io/retire.js/) - Look for out-of-date JS/Node.JS components
- [**Node Security Project**](https://nodesecurity.io/tools) - Look for out-of-date Node.JS dependencies

### Python

- [**Bandit**](https://wiki.openstack.org/wiki/Security/Projects/Bandit) - Python security static analyzer

### Ruby / Rails

- [**Brakeman**](http://brakemanscanner.org/) - Rails security static analyzer
- [**Bundler Audit**](https://github.com/rubysec/bundler-audit) - Find vulnerable Bundler dependencies

### PHP

- [**RIPS**](http://rips-scanner.sourceforge.net/) - PHP security static analyzer

### Java

- [**Victims**](https://securityblog.redhat.com/tag/victims/) - Find vulnerable Java dependencies

### System Configuration

- [**cve-check-tool**](https://github.com/ikeydoherty/cve-check-tool) - Look for CVEs affecting your package list
- [**clair**](https://github.com/coreos/clair) - Vulnerability static analysis for containers

## Blackbox Application Testing

#### Fuzzers
- [**commix**](https://github.com/stasinopoulos/commix/) - Try to find command injection bugs
- [**sqlmap**](https://github.com/sqlmapproject/sqlmap) - Try to find SQL injection bugs
- [**NoSQLMap**](https://github.com/tcstool/NoSQLMap) - Automated Mongo/NoSQL exploitation tool
- [**CSRFT**](https://github.com/PaulSec/CSRFT) - CSRF toolkit
- **syntribos** - A framework for fuzz-testing REST APIs for security defects

#### Brute Force
- [**nmap scripting engine**](http://nmap.org/book/nse.html) - Scripts for nmap to add bruteforce functionality

## Specific Platforms / Vulnerabilities

- [**WPScan**](https://github.com/wpscanteam/wpscan) - Scanner for WordPress vulnerabilities
- [**JDWP**](https://github.com/IOActive/jdwp-shellifier) - Scanner for Java Debug Wire Protocol vulnerabilities
- [**Jetty - Jetleak**](https://github.com/GDSSecurity/Jetleak-Testing-Script) - Scanner for the Jetleak vulnerability in the Jetty webserver
- [**MySQL - mysslstrip/BACKRONYM**](https://github.com/duo-labs/mysslstrip) - Tool for performing man-in-the-middle attacks on MySQL
- [**OpenSSL - Heartbleed**](https://github.com/FiloSottile/Heartbleed) - Tool to test for Heartbleed, a vulnerability in OpenSSL
- [**OpenSSL - DROWN**](https://github.com/nimia/public_drown_scanner) - Scanner for the DROWN vulnerability in SSL/TLS that affects multiple products
