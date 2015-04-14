---
title: DataStax Enterprise for Pivotal Cloud Foundry
---

This is documentation for the [DataStax Enterprise service for Pivotal Cloud Foundry](https://network.pivotal.io/products/p-cassandra), which provides a Cassandra key-value and table store. 

## Install via Pivotal Operations Manager

To install DataStax Enterprise for PCF, follow the procedure for installing Pivotal Ops Manager tiles:

1. Download the product file from [Pivotal Network](https://network.pivotal.io/).
1. Upload the product file to your Ops Manager installation.
1. Click **Add** next to the uploaded product description in the Available Products view to add this product to your staging area.
1. Click the newly added tile to review any configurable options.
1. Click **Apply Changes** to install the service.

## Product snapshot

<table border="1" class="nice">
<tr>
        <th>Current tile version</th>
        <th>Released on</th>
        <th>Software component version</th>
        <th>Supported migrations</th>
        <th>vSphere support?</th>
        <th>AWS support?</th>
</tr>
<tr>
        <td>1.3.5</td>
        <td>17th April 2015</td>
        <td>4.5</td>
        <td>
        From: <br />
        * 1.3.4 <br />
        * 1.3.3 <br />
        * 1.3.2 <br />
        </td>
        <td>Yes</td>
        <td>Yes</td>

</tr>
</table>


### Dependencies
This product requires [Pivotal Cloud Foundry](https://network.pivotal.io/products/pivotal-cf):

* Elastic Runtime version 1.4.0 or greater
* Ops Manager version 1.4.0 or greater

These must be installed first, before upgrading from a previous version. 

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

Please provide any bugs, feature requests, or questions to [the Pivotal Cloud Foundry Feedback list](mailto:pivotal-cf-feedback@pivotal.io).

## Further Reading

* [DataStax Enterprise Documentation](http://www.datastax.com/docs)

