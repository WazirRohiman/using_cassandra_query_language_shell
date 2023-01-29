Starting the Cassandra server
```
start_cassandra
```

Save the command that you will need to use later to connect to the Cassandra instance

Use the command you saved to connect to the Cassandra Server

Once connected to the CQLSH use the command below to get more information on the server you connected to
```
show host
```

Use the following command to find the version of the Cassandra server
```
show version
```

To print a list of the keyspaces on the server
```
describe keyspaces
```

The following defautl keyspaces will appear
```
system_traces  system_schema  system_auth  system  system_distributed
```

You can use ```cls ``` to clear the terminal screen

You can use ``` exit ``` to exit the server
