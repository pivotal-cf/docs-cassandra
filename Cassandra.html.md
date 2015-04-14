---
title: DataStax Enterprise for Pivotal CF
---

This is documentation for the DataStax Enterprise service for Pivotal CF, which provides a Cassandra key-value and table store.

### Features
Key features of this product are:

* Ability to provision an instance in a shared Cassandra cluster
* Offers redundancy across a 4-node cluster
* Powered by DataStax Enterprise release of Cassandra
* Repair functionality powered by DataStax OpsCenter to ensure your cluster remains healthy

### Install via Pivotal Operations Manager

To install DataStax Enterprise for Pivotal CF, follow the procedure for installing Pivotal Ops Manager tiles:

1. Download the product file from [Pivotal Network](https://network.pivotal.io/).
1. Upload the product file to your Ops Manager installation.
1. Click **Add** next to the uploaded product description in the Available Products view to add this product to your staging area.
1. Click the newly added tile to review any configurable options.
1. Click **Apply Changes** to install the service.

### Dependencies
This product requires Pivotal CF:

* Elastic Runtime version 1.2 or greater
* Ops Manager version 1.3 or greater

### Provisioning and Binding via Cloud Foundry

Once you have installed the product, it automatically registers itself with your Elastic Runtime. At this point, the product is available to your application developers, either in the Marketplace in Apps Manager, or via `cf marketplace`. They can add, provision, and bind the service to their applications like any other CF service:

```
$ cf create-service p-cassandra multi-tenant cassandra
$ cf bind-service my-application cassandra
$ cf restart my-application
```

### Example Application

To help your application developers get started with DataStax Enterprise for Pivotal CF, we have provided an example application, which can be [downloaded here](https://github.com/pivotal-cf/cf-cassandra-example-app/archive/master.zip).

### Available Plans

#### Multi-tenant
Currently, the only available plan is the **multi-tenant** plan. This plan provisions a single keyspace from the shared Cassandra cluster, suitable for development workloads.

We **do not** recommend using this in a production environment.

##### Architecture
By default the **multi-tenant** plan will configure `3` *seed nodes* and `1` *node* to give you a `4` node cluster in total.

You can increase these values through `OpsManager` on the `Resource Config` tab.

### Drivers
DataStax recommends that you use one of their [certified drivers](http://www.datastax.com/download#dl-datastax-drivers) in your application to connect to your instance.

### Licensing
Obtain a licence to use DataStax Enterprise [directly from DataStax](http://www.datastax.com/company#contact)

### Known Limitations

Limitations with the current Cassandra product include:

* Users are able to see the names of all other keyspaces in the cluster (though these names are essentially random). This is a limitation in Cassandra, and cannot be addressed without their assistance.
* **Users are able to see the names of all tables inside another user's keyspace.**  This is a limitation in Cassandra, and cannot be addressed without their assistance.
* It has no backup and restore capabilities.
* Users cannot provision multiple keyspaces in a single service instance,
  though they can easily provision multiple instances, each with their own
  keyspace.
* Constraining CPU, memory and/or disk usage is not supported.

We hope to address all of these limitations in future releases.


### Feedback

Please provide any bugs, feature requests, or questions to [the Pivotal CF Feedback list](mailto:pivotal-cf-feedback@pivotal.io).

### Version

This product is based on DataStax Enterprise version 4.5.

### Further Reading

* [DataStax Enterprise Documentation](http://www.datastax.com/docs)
