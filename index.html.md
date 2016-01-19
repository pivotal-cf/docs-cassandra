---
title: DataStax Enterprise for Pivotal Cloud Foundry&reg;
---

This is documentation for the [DataStax Enterprise service for Pivotal Cloud Foundry&reg;](https://network.pivotal.io/products/p-cassandra), which provides a Cassandra key-value and table store.

## Product snapshot

<dl>
<dt>Current DataStax Enterprise for Pivotal Cloud Foundry&reg; Details</dt>
<dd><strong>Version</strong>: 1.4.0 </dd>
<dd><strong>Release Date</strong>: xx January 2016</dd>
<dd><strong>Software component version</strong>: DataStax Enterprise 4.8.2</dd>
<dd><strong>Compatible Ops Manager Version(s)</strong>: 1.6.x, 1.5.x, 1.4.x</dd>
<dd><strong>Compatible Elastic Runtime Version(s)</strong>: 1.6.x, 1.5.x, 1.4.x</dd>
<dd><strong>vSphere support?</strong> Yes</dd>
<dd><strong>AWS support?</strong> Yes</dd>
<dd><strong>OpenStack support?</strong> Yes</dd>
</dl>

## Upgrading to the Latest Version

Consider the following compatibility information before upgrading DataStax Enterprise for [Pivotal Cloud Foundry&reg;](https://network.pivotal.io/products/pivotal-cf) (PCF).

<p class="note"><strong>Note</strong>: Before you upgrade to Ops Manager 1.4.x, you must first upgrade DataStax Enterprise for Pivotal Cloud Foundry&reg; to any version in its 1.3.x minor release, below 1.3.5. This allows DataStax Enterprise for Pivotal Cloud Foundry&reg; upgrades after you install OpsManager 1.4.x. </p>

For more information, refer to the full [Product Version Matrix](../compatibility-matrix.pdf).

<table border="1" class="nice">
<tr>
  <th>Ops Manager Version</th>
  <th>Supported Upgrades from Imported DataStax Enterprise Installation</th>
</tr>
<tr>
  <th>1.3.x</th>
  <td><ul>
      <li>From 1.3.2 to 1.3.3</li>
      <li>From 1.3.2 to 1.3.4</li>
      <li>From 1.3.3 to 1.3.4</li>
    </ul>
  </td>
</tr>
<tr>
  <th>1.6.x, 1.5.x and 1.4.x</th>
  <td><ul>
      <li>From 1.3.2 to 1.3.5, 1.3.6, 1.3.7, 1.3.8, 1.4.0</li>    
      <li>From 1.3.3 to 1.3.5, 1.3.6, 1.3.7, 1.3.8, 1.4.0</li>
      <li>From 1.3.4 to 1.3.5, 1.3.6, 1.3.7, 1.3.8, 1.4.0</li>
      <li>From 1.3.5 to 1.3.6, 1.3.7, 1.3.8, 1.4.0</li>
      <li>From 1.3.6 to 1.3.7, 1.3.8, 1.4.0</li>
      <li>From 1.3.7 to 1.3.8, 1.4.0</li>
      <li>From 1.3.8 to 1.4.0</li>
    </ul>
  </td>
</tr>
</table>

## Install via Pivotal Operations Manager

To install DataStax Enterprise for PCF, follow the procedure for installing Pivotal Ops Manager tiles:

1. Download the product file from [Pivotal Network](https://network.pivotal.io/).
1. Upload the product file to your Ops Manager installation.
1. Click **Add** next to the uploaded product description in the Available Products view to add this product to your staging area.
1. Click the newly added tile to review any configurable options.
1. Click **Apply Changes** to install the service.

## Available Plans

There is one available plan:

<table border="1" class="nice">
<tr>
<th><strong>Plan Name</strong></th>
<th><strong>Suitable for</strong></th>
<th><strong>Tenancy Model per Instance</strong></th>
<th><strong>Highly Available</strong></th>
<th><strong>Backup Functionality</strong></th>
</tr>

<tr>
<td><b>Development</b></td>
<td>Development and testing workloads</td>
<td>Shared Cluster</td>
<td>Yes</td>
<td>No</td>
</tr>

</table>

## Provisioning and Binding via Cloud Foundry

Once you have installed the product, it automatically registers itself with your Elastic Runtime. At this point, the product is available to your application developers, either in the Marketplace in the web based console, or via `cf marketplace`. They can add, provision, and bind the service to their applications like any other CF service:

```
$ cf create-service p-cassandra development datastax
$ cf bind-service my-application datastax
$ cf restart my-application
```

## Example Application

To help your application developers get started with DataStax Enterprise for PCF, we have provided an example application, which can be [downloaded here](https://github.com/pivotal-cf/cf-cassandra-example-app/archive/master.zip).

## Drivers
DataStax recommends that you use one of their [certified drivers](http://www.datastax.com/download#dl-datastax-drivers) in your application to connect to your instance.

## Licensing
Obtain a licence to use DataStax Enterprise [directly from DataStax](http://www.datastax.com/company#contact)

## Feedback

Please provide any bugs, feature requests, or questions to [the Pivotal Cloud Foundry&reg; Feedback list](mailto:pivotal-cf-feedback@pivotal.io).

## Further Reading

* [DataStax Enterprise Documentation](http://www.datastax.com/docs)
