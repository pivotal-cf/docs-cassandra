---
title: DataStax Enterprise for Pivotal Cloud Foundry
---

This is documentation for the DataStax Enterprise service for Pivotal Cloud Foundry, which provides a Cassandra key-value and table store.

## Development plan features
Key features of this plan are:

* Ability to provision an instance in a shared Cassandra cluster
* Offers redundancy across a 4-node cluster
* Powered by DataStax Enterprise release of Cassandra
* Repair functionality powered by DataStax OpsCenter to ensure your cluster remains healthy
* Suitable for development and testing workloads

We **do not** recommend using this in a production environment.

## Architecture
By default the **development** plan will configure `3` *seed nodes* and `1` *node* to give you a `4` node cluster in total.

You can increase these values through `OpsManager` on the `Resource Config` tab.

## Known Limitations

Limitations with the current Cassandra product include:

* Users are able to see the names of all other keyspaces in the cluster (though these names are essentially random). This is a limitation in Cassandra, and cannot be addressed without their assistance.
* **Users are able to see the names of all tables inside another user's keyspace.**  This is a limitation in Cassandra, and cannot be addressed without their assistance.
* It has no backup and restore capabilities.
* Users cannot provision multiple keyspaces in a single service instance,
  though they can easily provision multiple instances, each with their own
  keyspace.
* Constraining CPU, memory and/or disk usage is not supported.

We hope to address all of these limitations in future releases.

