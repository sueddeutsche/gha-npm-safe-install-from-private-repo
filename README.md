# gha-npm-safe-install-from-private-repo
Allows to install packages from a private npm repository while protecting the NPM token.

## Usage

### Minimal Config
```yaml
name: Install NPM Packages
  uses: sueddeutsche/gha-npm-safe-install-from-private-repo@v3
  with:
    NPM_TOKEN: ${{ secrets.NPM_TOKEN }} # NPM token stored in a secret
```

### Full config
```yaml
name: Install NPM Packages
  uses: sueddeutsche/gha-npm-safe-install-from-private-repo@v3
  with:
    NPM_TOKEN: ${{ secrets.NPM_TOKEN }} # NPM token stored in a secret
    registry-url: 'https://registry.npmjs.org' # optioonal defaults to https://registry.npmjs.org
    node-version: '18' #optional: defaults to '18', for options see https://github.com/actions/setup-node#supported-version-syntax
```

## Motivation
Installing packages the intuitive way may hold the inherent risk of exposing the NPM-Token to malicious packages.
Therefore this actions ensures that precautionairy steps are taken to prevent this from happening while providing the normal ease of use for the developer. 

see https://github.com/actions/setup-node/blob/main/docs/advanced-usage.md#use-private-packages

## Design
Wrapper around `setup-node`default action.
