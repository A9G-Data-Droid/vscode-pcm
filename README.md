# Zeiss PCM

<!-- TOC depthFrom:2 -->

- [Zeiss PCM](#zeiss-pcm)
  - [Syntax Highlighting](#syntax-highlighting)
  - [Installation](#installation)
  - [Contributing](#contributing)

<!-- /TOC -->

## Syntax Highlighting

This package provides syntax highlighting for Zeiss PCM code.


## Installation

Launch VS Code Quick Open (Ctrl+P), paste the following command, and
press enter.

```
ext install pcm
```

## Contributing

Please fork this repository and contribute back using pull requests.

Any contributions, large or small, major features, bugfixes and
integration tests are welcomed and appreciated but will be thoroughly
reviewed and discussed.

## Handy links

I struggled to find how to generate a token after not doing anything
with this project for well over a year:

To get to your token creation, go here:

- https://YOUR_USER_NAME.visualstudio.com/_details/security/tokens

**Create a token:**

- Name: vsce
- Organisation: All accessible organizations
- show all scopes, select:
  - Marketplace
    - Check Acquire and Manage

**Publish with CLI:**

```bash
# login
vsce login <publisher name>
# install the things
npm i
# use the token created in earlier step
vsce package
# myExtension.vsix generated
# bump version
vsce publish minor # | major | patch
# vsce publish major, minor or patch
vsce publish -p <add created token here>
```

If you get `ERROR Failed request: (401)` see here:

- https://github.com/Microsoft/vscode-vsce/issues/11

Some good documentation on publishing with the CLI:

- https://code.visualstudio.com/api/working-with-extensions/publishing-extension


