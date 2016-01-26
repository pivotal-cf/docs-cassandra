---
title: DataStax Enterprise for Pivotal Cloud Foundry&reg;
---

# Resource requirements
These are the default resource and IP requirements for installing the tile
<table border="1" class="nice">
	<tr>
		<th>Resource</th>
		<th>Instances</th>
		<th>CPU</th>
		<th>Ram</th>
		<th>Ephemeral</th>
		<th>Persistent</th>
		<th>Static IP</th>
		<th>Dynamic IP</th>
	</tr>
	<tr>
	 	<td>Multitenant Cassandra Seed Node</td>
	 	<td>3</td>
	 	<td>2</td>
	 	<td>4096</td>
	 	<td>4096</td>
	 	<td>8192</td>
	 	<td>1</td>
	 	<td>0</td>
 	</tr>
 	<tr>
 		<td>Multitenant Cassandra Node</td>
 		<td>1</td>
 		<td>2</td>
 		<td>4096</td>
 		<td>4096</td>
 		<td>8192</td>
 		<td>1</td>
 		<td>0</td>
 	</tr>
 	<tr>
 		<td>Cassandra Broker</td>
 		<td>1</td>
 		<td>2</td>
 		<td>1024</td>
 		<td>4096</td>
 		<td>1024</td>
 		<td>1</td>
 		<td>0</td>
 	</tr> 	 	
	<tr>
		<td>Broker Registrar</td>
		<td>1</td>
		<td>1</td>
		<td>1024</td>
		<td>2048</td>
		<td>0</td>
		<td>0</td>
		<td>1</td>
	</tr>
	<tr>
		<td>Broker De-Registrar</td>
		<td>1</td>
		<td>1</td>
		<td>1024</td>
		<td>2048</td>
		<td>0</td>
		<td>0</td>
		<td>1</td>
	</tr>
	<tr>
		<td>Compliation</td>
		<td>2</td>
		<td>2</td>
		<td>1024</td>
		<td>8192</td>
		<td>0</td>
		<td>0</td>
		<td>1</td>
	</tr>
</table>

#### Notes:
* The `multi-tenant` plan consists of the `Multitenant Cassandra Seed Node` and `Multitenant Cassandra Node` resources
