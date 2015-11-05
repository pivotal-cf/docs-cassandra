---
title: DataStax Enterprise for Pivotal Cloud Foundry&reg;
---

Release notes for [DataStax Enterprise for Pivotal Cloud Foundry&reg;](https://network.pivotal.io/products/p-cassandra)

### 1.3.7
**Release Date: 30th October 2015**

Features included in this release:

* Updated stemcell to 3112
* Fixed bug where long URLs would cause the OpsCenter job to fail
* Updated NTPD to the latest package

### 1.3.6
**Release Date: 6th July 2015**

Features included in this release:

* Support for OpsManager 1.5.x or 1.4.x
* Support for Elastic Runtime 1.5.x or 1.4.x
* Support for HTTPS-only environments
* Support for vSphere or AWS Deployments
* Requires stemcell 2989

### 1.3.5
**Release Date: 17th April 2015**

Features included in this release:

* Support for vSphere & AWS
* Requires OpsManager 1.4.0 and Elastic Runtime 1.4.0 or greater

Known issues:

* On AWS, this version supports deployments in the US-East region. Multi-region support is coming in a future release.
* The experimental HTTPS-only feature in Elastic Runtime 1.5 may cause issues with this version of the product. Full support for HTTPS-only traffic is coming in a future release.

<p class="note"><strong>Note</strong>: BOSH Stemcell 2865.1 is required for installation on Ops Manager 1.5.x and above. </p>

### 1.3.4
**Release Date: 24th March 2015**

Features included in this release:

* Updated stemcell to 2889 to resolve [these OpenSSL CVE alerts](http://pivotal.io/security/usn-2537-1)

### 1.3.3
**Release Date: 11th February 2015**

Features included in this release:

* Updated stemcell to 2824 to resolve [CVE-2015-0235 Ghost](http://www.pivotal.io/security/cve-2015-0235)

### 1.3.2
**Release Date: 29th October 2014**

Features included in this release:

* General Availability release
* `development` service plan, providing a 4 node cassandra cluster
  * suitable for development and test workloads
