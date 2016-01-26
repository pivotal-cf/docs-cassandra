---
title: DataStax Enterprise for Pivotal Cloud Foundry&reg;
---

Release notes for [DataStax Enterprise for Pivotal Cloud Foundry&reg;](https://network.pivotal.io/products/p-cassandra)

### 1.4.0
**Release Date: xx January 2015**

Features included in this release:

* Updated stemcell to xxxx
* DataStax Enterprise is automatically upgraded when moving to this tile version. Including executing all of the recommend upgrade steps, see the upgrade documentation for more details
* Support for rolling deployments
* DataStax Enterprise updated to 4.8.2
* DataStax OpsCenter updated to 5.2.2
* Suitable for workloads that do not require dedicated resources.

**Known issue:**

* On AWS we have observed that the arp cache on nodes which have being updated go stale and therefore whilst the VM is online and the Cassandra process is running, the node has not yet successfully rejoined the cluster
* We have implemented workarounds, but we have observed this taking up to 10 minutes to resolve itself
* There is a risk that with the default 4 node cluster setup, you can lose quorum in the cluster which depending upon your chosen settings in your application could result in you being able to read / write data.
* To workaround this we recommend first scaling the cluster to 5 nodes, by increasing the number of `Multitenant Cassandra Node` to 2 nodes and deploying successfully, giving a total of 5 nodes in the cluster
* Before then upgrading to this `1.4.0` tile we recommend you log into DataStax OpsCenter and validate that all 5 nodes are online and healthy and are now fully replicated.

### 1.3.8
**Release Date: 11th November 2015**

Features included in this release:

* Updated stemcell to 3130. Resolves CVE USN-2806-1.

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

**Known issues:**

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
