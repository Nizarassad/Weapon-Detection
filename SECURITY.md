# Security policy

## Credentials

Never store API keys, access tokens, passwords, service-account files, or private configuration in notebooks or repository files. Use environment variables or an approved secret store.

If a credential is ever committed publicly:

1. revoke and rotate it at the provider immediately;
2. remove it from the current tree;
3. verify the replacement is not exposed;
4. assess logs and account activity;
5. decide separately whether repository-history rewriting is necessary.

Deleting a value from the latest commit does not remove it from Git history, forks, caches, or prior downloads.

## Reporting

Please report security concerns privately to the repository owner rather than opening a public issue containing exploit details or credentials.

## Model and data security

Treat model weights, datasets, predictions, and camera imagery as potentially sensitive. Validate external files, restrict access, document provenance, and consider adversarial manipulation and model-extraction risks before deployment.
