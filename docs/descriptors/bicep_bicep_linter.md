---
title: bicep_linter configuration in MegaLinter
description: How to use bicep_linter (configure, ignore files, ignore errors, help & version documentations) to analyze BICEP files
---
<!-- markdownlint-disable MD033 MD041 -->
<!-- @generated by .automation/build.py, please do not update manually -->
# <a href="https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/linter" target="blank" title="Visit linter Web Site"><img src="https://raw.githubusercontent.com/Azure/bicep/main/docs/images/BicepLogoImage.png" alt="bicep_linter" height="100px" class="megalinter-logo"></a>bicep_linter
[![GitHub stars](https://img.shields.io/github/stars/Azure/bicep?cacheSeconds=3600)](https://github.com/Azure/bicep) [![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/Azure/bicep?sort=semver)](https://github.com/Azure/bicep/releases) [![GitHub last commit](https://img.shields.io/github/last-commit/Azure/bicep)](https://github.com/Azure/bicep/commits) [![GitHub commit activity](https://img.shields.io/github/commit-activity/y/Azure/bicep)](https://github.com/Azure/bicep/graphs/commit-activity/) [![GitHub contributors](https://img.shields.io/github/contributors/Azure/bicep)](https://github.com/Azure/bicep/graphs/contributors/)

By default, Bicep linter errors are set as warnings. To customize linter settings,
use a `bicepconfig.json` file. For more information, see the [documentation for the Bicep Linter](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/bicep-config-linter#customize-linter)

## bicep_linter documentation

- Version in MegaLinter: **0.14.85**
- Visit [Official Web Site](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/linter){target=_blank}
- See [How to configure bicep_linter rules](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/bicep-config){target=_blank}
- See [How to disable bicep_linter rules in files](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/linter#silencing-false-positives){target=_blank}
- See [Index of problems detected by bicep_linter](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/linter#default-rules){target=_blank}

[![bicep - GitHub](https://gh-card.dev/repos/Azure/bicep.svg?fullname=)](https://github.com/Azure/bicep){target=_blank}

## Configuration in MegaLinter

- Enable bicep_linter by adding `BICEP_BICEP_LINTER` in [ENABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)
- Disable bicep_linter by adding `BICEP_BICEP_LINTER` in [DISABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)

| Variable                                       | Description                                                                                                                                                                                  | Default value      |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| BICEP_BICEP_LINTER_ARGUMENTS                   | User custom arguments to add in linter CLI call<br/>Ex: `-s --foo "bar"`                                                                                                                     |                    |
| BICEP_BICEP_LINTER_FILTER_REGEX_INCLUDE        | Custom regex including filter<br/>Ex: `(src\|lib)`                                                                                                                                           | Include every file |
| BICEP_BICEP_LINTER_FILTER_REGEX_EXCLUDE        | Custom regex excluding filter<br/>Ex: `(test\|examples)`                                                                                                                                     | Exclude no file    |
| BICEP_BICEP_LINTER_CLI_LINT_MODE               | Override default CLI lint mode<br/>- `file`: Calls the linter for each file<br/>- `project`: Call the linter from the root of the project                                                    | `file`             |
| BICEP_BICEP_LINTER_FILE_EXTENSIONS             | Allowed file extensions. `"*"` matches any extension, `""` matches empty extension. Empty list excludes all files<br/>Ex: `[".py", ""]`                                                      | `[".bicep"]`       |
| BICEP_BICEP_LINTER_FILE_NAMES_REGEX            | File name regex filters. Regular expression list for filtering files by their base names using regex full match. Empty list includes all files<br/>Ex: `["Dockerfile(-.+)?", "Jenkinsfile"]` | Include every file |
| BICEP_BICEP_LINTER_PRE_COMMANDS                | List of bash commands to run before the linter                                                                                                                                               | None               |
| BICEP_BICEP_LINTER_POST_COMMANDS               | List of bash commands to run after the linter                                                                                                                                                | None               |
| BICEP_BICEP_LINTER_DISABLE_ERRORS              | Run linter but consider errors as warnings                                                                                                                                                   | `false`            |
| BICEP_BICEP_LINTER_DISABLE_ERRORS_IF_LESS_THAN | Maximum number of errors allowed                                                                                                                                                             | `0`                |

## IDE Integration

Use bicep_linter in your favorite IDE to catch errors before MegaLinter !

|                                                                  <!-- -->                                                                   | IDE                                                  | Extension Name                                                                                 |                                                                                     Install                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------:|------------------------------------------------------|------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/vscode.ico" alt="" height="32px" class="megalinter-icon"></a> | [Visual Studio Code](https://code.visualstudio.com/) | [VSCode Bicep](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-bicep) | [![Install in VSCode](https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/btn_install_vscode.png)](vscode:extension/ms-azuretools.vscode-bicep){target=_blank} |

## MegaLinter Flavours

This linter is available in the following flavours

|                                                                         <!-- -->                                                                         | Flavor                                               | Description                                   | Embedded linters |                                                                                                                                                                                     Info |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------|:----------------------------------------------|:----------------:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/mega-linter-square.png" alt="" height="32px" class="megalinter-icon"></a> | [all](https://megalinter.io/beta/supported-linters/) | Default MegaLinter Flavor                     |       112        |               ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter) |
|       <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/dotnet.ico" alt="" height="32px" class="megalinter-icon"></a>        | [dotnet](https://megalinter.io/beta/flavors/dotnet/) | Optimized for C, C++, C# or VB based projects |        59        | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-dotnet/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-dotnet) |

## Behind the scenes

### How are identified applicable files

- File extensions: `.bicep`

<!-- markdownlint-disable -->
<!-- /* cSpell:disable */ -->
### How the linting is performed

- bicep_linter is called one time by identified file (`file` CLI lint mode)

### Example calls

```shell
# Bicep CLI 
bicep build infra.bicep;

# Azure CLI 
az bicep build -f infra.bicep

```


### Help content

```shell
Bicep CLI version 0.14.85 (f4a4d485ba)

Usage:
  bicep build [options] <file>
    Builds a .bicep file.

    Arguments:
      <file>        The input file

    Options:
      --outdir <dir>    Saves the output at the specified directory.
      --outfile <file>  Saves the output as the specified file path.
      --stdout          Prints the output to stdout.
      --no-restore      Builds the bicep file without restoring external modules.

    Examples:
      bicep build file.bicep
      bicep build file.bicep --stdout
      bicep build file.bicep --outdir dir1
      bicep build file.bicep --outfile file.json
      bicep build file.bicep --no-restore

    bicep format [options] <file>
    Formats a .bicep file.

    Arguments:
      <file>        The input file

    Options:
      --outdir <dir>        Saves the output at the specified directory.
      --outfile <file>      Saves the output as the specified file path.
      --stdout              Prints the output to stdout.
      --newline             Set newline char. Valid values are ( Auto | LF | CRLF | CR ).
      --indentKind          Set indentation kind. Valid values are ( Space | Tab ).
      --indentSize          Number of spaces to indent with (Only valid with --indentKind set to Space).
      --insertFinalNewline  Insert a final newline.

    Examples:
      bicep format file.bicep
      bicep format file.bicep --stdout
      bicep format file.bicep --outdir dir1
      bicep format file.bicep --outfile file.json
      bicep format file.bicep --indentKind Tab

  bicep decompile [options] <file>
    Attempts to decompile a template .json file to .bicep.

    Arguments:
      <file>        The input file

    Options:
      --outdir <dir>    Saves the output at the specified directory.
      --outfile <file>  Saves the output as the specified file path.
      --stdout          Prints the output to stdout.
      --force           Allows overwriting the output file if it exists (applies only to 'bicep decompile').

    Examples:
      bicep decompile file.json
      bicep decompile file.json --stdout
      bicep decompile file.json --outdir dir1
      bicep decompile file.json --force
      bicep decompile file.json --outfile file.bicep

  bicep generate-params [options] <file>
    Builds .parameters.json file from the given bicep file, updates if there is an existing parameters.json file.

    Arguments:
      <file>        The input file

    Options:
      --no-restore      Generates the parameters file without restoring external modules.
      --outdir <dir>    Saves the output at the specified directory.
      --outfile <file>  Saves the output as the specified file path.
      --stdout          Prints the output to stdout.

    Examples:
      bicep generate-params file.bicep
      bicep generate-params file.bicep --no-restore
      bicep generate-params file.bicep --stdout
      bicep generate-params file.bicep --outdir dir1
      bicep generate-params file.bicep --outfile file.parameters.json


  bicep publish <file> --target <ref>
    Publishes the .bicep file to the module registry.

    Arguments:
      <file>        The input file (can be a Bicep file or an ARM template file)
      <ref>         The module reference

    Options:
      --documentationUri  Module documentation uri

    Examples:
      bicep publish file.bicep --target br:example.azurecr.io/hello/world:v1
      bicep publish file.json --target br:example.azurecr.io/hello/world:v1
      bicep publish file.json --target br:example.azurecr.io/hello/world:v1 --documentationUri https://github.com/hello-world/README.md

  bicep restore <file>
    Restores external modules from the specified Bicep file to the local module cache.

    Arguments:
      <file>        The input file

 bicep [options]
    Options:
      --version              -v   Shows bicep version information
      --help                 -h   Shows this usage information
      --license                   Prints license information
      --third-party-notices       Prints third-party notices


  bicep build-params <file>
    Builds .bicepparam file.

    Arguments:
      <file>        The input Bicepparam file

    Options:
      --bicep-file <file> Verifies if the bicep file reference in the params file using declaration matches the specified file path.
      --outfile-params <file>  Saves the param output as the specified file path.
      --outfile-bicep <file>  Saves the bicep output as the specified file path.
      --stdout          Prints the output to stdout.
      --no-restore      Builds the bicep file without restoring external modules.

    Examples:
      bicep build-params params.bicepparam
      bicep build-params params.bicepparam --stdout
      bicep build-params params.bicepparam --outfile-params otherParams.json --outfile-bicep otherMain.json
      bicep build-params params.bicepparam --no-restore


```

### Installation on mega-linter Docker image

- Dockerfile commands :
```dockerfile
ARG BICEP_EXE='bicep'
ARG BICEP_URI='https://github.com/Azure/bicep/releases/latest/download/bicep-linux-musl-x64'
ARG BICEP_DIR='/usr/local/bin'
RUN curl --retry 5 --retry-delay 5 -sLo ${BICEP_EXE} "${BICEP_URI}" \
    && chmod +x "${BICEP_EXE}" \
    && mv "${BICEP_EXE}" "${BICEP_DIR}"

```
