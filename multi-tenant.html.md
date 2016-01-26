---
title: DataStax Enterprise for Pivotal Cloud Foundry&reg;
---

This is documentation for the DataStax Enterprise service for [Pivotal Cloud Foundry&reg;](https://network.pivotal.io/products/pivotal-cf) (PCF), which provides a Cassandra key-value and table store.

## Development plan features
Key features of this plan are:

* Ability to provision an instance in a shared Cassandra cluster
* Offers redundancy across a 4-node cluster
* Powered by DataStax Enterprise release of Cassandra
* Repair functionality powered by DataStax OpsCenter to ensure your cluster remains healthy
* Suitable for workloads which do not require a dedicated cluster
* Automated upgrades of DataStax Enterprise and migrations of data
* Rolling deployments across the cluster ensuring minimal downtime

## Architecture
By default the **multi-tenant** plan will configure `3` *seed nodes* and `1` *node* to give you a `4` node cluster in total.

You can increase these values through `OpsManager` on the `Resource Config` tab.

## Known Limitations

Limitations with the current Cassandra product include:

* Users are able to see the names of all other keyspaces in the cluster (though these names are essentially random). This is a limitation in Cassandra, and cannot be addressed without their assistance.
* **Users are able to see the names of all tables inside another user's keyspace.**  This is a limitation in Cassandra, and cannot be addressed without their assistance.
* Users cannot provision multiple keyspaces in a single service instance,
  though they can easily provision multiple instances, each with their own
  keyspace.
* Constraining CPU, memory and/or disk usage is not supported.

We hope to address all of these limitations in future releases.
