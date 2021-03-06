## kconnect to

Re-connect to a previously connected cluster using your history

### Synopsis

use is for re-connecting to a previously connected cluster using your history.
You can use the history id or alias as the argument.
You can also supply - or LAST to connect to last cluster in history (current cluster), or LAST~N for previous clusters

```
kconnect to [historyid/alias/-/LAST/LAST~N] [flags]
```

### Examples

```
  # Re-connect based on an alias
  kconnect to uat-bu1

  # # Re-connect based on an history id - history id can be found using kconnect ls
  kconnect to 01EM615GB2YX3C6WZ9MCWBDWBF

  # Re-connect to current cluster (this is useful for renewing credentials)
  kconnect to -
  OR 
  kconnect to LAST

  # Re-connect to cluster used before current one
  kconnect to LAST~1

  # Re-connect based on an alias supplying a password
  kconnect to uat-bu1 --password supersecret

  # Re-connect based on an alias supplying a password via env var
  KCONNECT_PASSWORD=supersecret kconnect to uat-bu1

```

### Options

```
  -h, --help                      help for to
      --history-location string   Location of where the history is stored. (default "$HOME/.kconnect/history.yaml")
  -k, --kubeconfig string         Location of the kubeconfig to use. (default "$HOME/.kube/config")
      --password string           Password to use
      --set-current               Sets the current context in the kubeconfig to the selected cluster (default true)
```

### Options inherited from parent commands

```
      --config string     Configuration file for application wide defaults. (default "$HOME/.kconnect/config.yaml")
      --non-interactive   Run without interactive flag resolution
  -v, --verbosity int     Sets the logging verbosity. Greater than 0 is debug and greater than 9 is trace.
```

### SEE ALSO

* [kconnect](index.md)	 - The Kubernetes Connection Manager CLI

