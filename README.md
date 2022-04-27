# gha-npm-safe-install-from-private-repo
Allows to install packages from a private npm repository while protecting NPM credentials

## Usage

```

```

# Parameters

## Motivation
Installing packages the intuitive way may hold the inherent risk of exposing the NPM-Token to malicious packages.
Therefore this actions ensures that precationairy steps are taken to prevent this from happening while providing the normal ease of use. 

https://github.com/actions/setup-node/blob/main/docs/advanced-usage.md#publish-to-npmjs-and-gpr-with-npm

## Design
Wrapper around `setup-node`default action.