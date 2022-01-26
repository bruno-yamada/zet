# Vault - getting started

## Start local vault and create a generic secret:

```
vault server -dev
```

It will print the server address and root token
eg.
```
WARNING! dev mode is enabled! In this mode, Vault runs entirely in-memory
and starts unsealed with a single unseal key. The root token is already
authenticated to the CLI, so you can immediately begin using Vault.

You may need to set the following environment variable:

    $ export VAULT_ADDR='http://127.0.0.1:8200'

The unseal key and root token are displayed below in case you want to
seal/unseal the Vault or re-authenticate.

Unseal Key: zakrv6t8TlqEtW47PvBsj+EXzMX2QxmjYmqK9X2QiRA=
Root Token: s.uwIwihUs6nrruxHgyeY8xDjv

Development mode should NOT be used in production installations!
```

You can login to this local vault with:
```
vault login token=$TOKEN_PROVIDED_ABOVE
```

It will save a temporary token to this file: ~/.vault-token and vault will read
from it automatically (alternativelly you can provide the token as the env
variable $VAULT_TOKEN)

## Enable a generic secret backend

```
vault secrets enable --path my-test generic
```

Write a value to it
```
vault write my-test/my-secret my-key=my-value
# or
vault write my-test/my-secret @path/to/secrets.json
```

## Read and list your secrets
```
vault list my-test
vault read my-test/my-secret
vault read -format json my-test/my-secret
```

Alternatively, use the cli [safe](https://github.com/starkandwayne/safe), it has
some commands that are much easier to use than vault's defaults and also add a
few that are good to have, eg:
```
safe paths my-test
safe set my-test/my-secret a=1 b=2
```

> tags: vault; devops

> uid: 20220107105527Z

> links: 

