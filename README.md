# springboot-cassandra-docker

# Before running application, run docker-compose and up Cassandra Database:
-> docker-compose up

# Then run cassandra on bash
-> docker exec -it 'container id' bash
 
 or 
 (windows) 
 -> winpty docker exec -it 'container id' bash
 
 
 # Enter on CQLSH
 -> cqlsh

# Creating a Keyspace using Cqlsh
# A keyspace in Cassandra is a namespace that defines data replication on nodes. A cluster contains one keyspace per node. Given below is the syntax for creating a keyspace using the statement CREATE KEYSPACE.

CREATE KEYSPACE mykeyspace
WITH replication = {'class':'SimpleStrategy', 'replication_factor' : 3};

# Set the keyspace
use mykeyspace

# Create a Table using Cqlsh

CREATE TABLE Product( id int PRIMARY KEY, name text);

# Describe Keyspaces − This command lists all the keyspaces in a cluster. Given below is the usage of this command.

 describe keyspaces;

# Describe tables − This command lists all the tables in a keyspace. Given below is the usage of this command.

 describe tables:

# Describe table − This command provides the description of a table. Given below is the usage of this command.

 describe table product;
