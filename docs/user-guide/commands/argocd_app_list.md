## argocd app list

List applications

```
argocd app list [flags]
```

### Examples

```
  # List all apps
  argocd app list

  # List apps by label, in this example we listing apps that are children of another app (aka app-of-apps)
  argocd app list -l app.kubernetes.io/instance=my-app
```

### Options

```
  -N, --app-namespace string   Only list applications in namespace
  -h, --help                   help for list
  -o, --output string          Output format. One of: wide|name|json|yaml (default "wide")
  -p, --project stringArray    Filter by project name
  -r, --repo string            List apps by source repo URL
  -l, --selector string        List apps by label
```

### Options inherited from parent commands

```
      --auth-token string               Authentication token
      --client-crt string               Client certificate file
      --client-crt-key string           Client certificate key file
      --config string                   Path to Argo CD config (default "/home/user/.config/argocd/config")
      --core                            If set to true then CLI talks directly to Kubernetes instead of talking to Argo CD API server
      --grpc-web                        Enables gRPC-web protocol. Useful if Argo CD server is behind proxy which does not support HTTP2.
      --grpc-web-root-path string       Enables gRPC-web protocol. Useful if Argo CD server is behind proxy which does not support HTTP2. Set web root.
  -H, --header strings                  Sets additional header to all requests made by Argo CD CLI. (Can be repeated multiple times to add multiple headers, also supports comma separated headers)
      --http-retry-max int              Maximum number of retries to establish http connection to Argo CD server
      --insecure                        Skip server certificate and domain verification
      --kube-context string             Directs the command to the given kube-context
      --logformat string                Set the logging format. One of: text|json (default "text")
      --loglevel string                 Set the logging level. One of: debug|info|warn|error (default "info")
      --plaintext                       Disable TLS
      --port-forward                    Connect to a random argocd-server port using port forwarding
      --port-forward-namespace string   Namespace name which should be used for port forwarding
      --server string                   Argo CD server address
      --server-crt string               Server certificate file
```

### SEE ALSO

* [argocd app](argocd_app.md)	 - Manage applications

