---
title: Reshard reversetraffic
series: vtctldclient
commit: 0f751fbb7c64ca5280c5d4f58d038e1df5477c67
---
## vtctldclient Reshard reversetraffic

Reverse traffic for a Reshard VReplication workflow.

```
vtctldclient Reshard reversetraffic
```

### Examples

```
vtctldclient --server localhost:15999 Reshard --workflow cust2cust --target-keyspace customer reversetraffic
```

### Options

```
  -c, --cells strings                          Cells and/or CellAliases to switch traffic in.
      --dry-run                                Print the actions that would be taken and report any known errors that would have occurred.
      --enable-reverse-replication             Setup replication going back to the original source keyspace to support rolling back the traffic cutover. (default true)
  -h, --help                                   help for reversetraffic
      --max-replication-lag-allowed duration   Allow traffic to be switched only if VReplication lag is below this. (default 30s)
      --tablet-types strings                   Tablet types to switch traffic for.
      --timeout duration                       Specifies the maximum time to wait, in seconds, for VReplication to catch up on primary tablets. The traffic switch will be cancelled on timeout. (default 30s)
```

### Options inherited from parent commands

```
      --action_timeout duration   timeout to use for the command (default 1h0m0s)
      --compact                   use compact format for otherwise verbose outputs
      --format string             The format of the output; supported formats are: text,json. (default "text")
      --server string             server to use for the connection (required)
      --target-keyspace string    Target keyspace for this workflow.
  -w, --workflow string           The workflow you want to perform the command on.
```

### SEE ALSO

* [vtctldclient Reshard](../)	 - Perform commands related to resharding a keyspace.
