Creates a keyspace called training, using SimpleStrategy and a replication_factor of 3.

SimpleStrategy is used when all the nodes in your cassandra cluster exist in a single data center
```
CREATE KEYSPACE training
WITH replication = {'class':'SimpleStrategy', 'replication_factor': 3};
```

To view the keyspaces - Run the following command
```
describe keyspaces
```

To view more details about the training keyspace use the follopwing command
```
describe training
```

We can alter the class of the replication as follows, in this case changing it from ```simpleStrategy``` to ```NetworkTopologyStrategy```

```
ALTER KEYSPACE training
WITH replication = {'class':'NetworkTopologyStrategy'};
```

See the changes
```
describe training
```

To use the keyspace we create, use the following command
```
use training;
```

You can use the following command to check the tables in the keyspace. Note that because we just created this new keyspace, we will get an empty list if we run the following command
```
describe tables
```

To drop the keyspace, use the following command
```
DROP KEYSPACE training;
```

Verify the changes running this command
```
use system;
describe keyspaces
```

