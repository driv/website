---
title: Workflow show
series: vtctldclient
commit: d3ff5982ddbbb04da1c9ac3c0bff9b09c904c749
---
## vtctldclient Workflow show

Show the details for a VReplication workflow.

```
vtctldclient Workflow show
```

### Examples

```
vtctldclient --server localhost:15999 workflow --keyspace customer show --workflow commerce2customer
```

### Options

```
  -h, --help              help for show
      --include-logs      Include recent logs for the workflow. (default true)
  -w, --workflow string   The workflow you want the details for.
```

### Options inherited from parent commands

```
      --action_timeout duration   timeout to use for the command (default 1h0m0s)
      --compact                   use compact format for otherwise verbose outputs
  -k, --keyspace string           Keyspace context for the workflow.
      --server string             server to use for the connection (required)
```

### SEE ALSO

* [vtctldclient Workflow](../)	 - Administer VReplication workflows (Reshard, MoveTables, etc) in the given keyspace.

