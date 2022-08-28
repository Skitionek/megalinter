<!-- markdownlint-disable MD033 MD041 -->
<!-- @generated by .automation/build.py, please do not update manually -->
# <a href="https://remark.js.org/" target="blank" title="Visit linter Web Site"><img src="https://raw.githubusercontent.com/remarkjs/remark-lint/02295bc/logo.svg?sanitize=true" alt="remark-lint" height="100px" class="megalinter-logo"></a>remark-lint [![GitHub last commit](https://img.shields.io/github/last-commit/remarkjs/remark-lint)](https://github.com/remarkjs/remark-lint/commits)

_This linter has been temporary disabled in this version_

## remark-lint documentation

- Version in MegaLinter: **14.0.2**
- Visit [Official Web Site](https://remark.js.org/){target=_blank}
- See [How to configure remark-lint rules](https://github.com/remarkjs/remark-lint#configuring-remark-lint){target=_blank}
  - If custom `.remarkrc` config file is not found, [.remarkrc](https://github.com/oxsecurity/megalinter/tree/main/TEMPLATES/.remarkrc){target=_blank} will be used
- See [How to disable remark-lint rules in files](https://github.com/remarkjs/remark-message-control#markers){target=_blank}
- See [Index of problems detected by remark-lint](https://github.com/remarkjs/remark-lint/blob/main/doc/rules.md#list-of-rules){target=_blank}

[![remark-lint - GitHub](https://gh-card.dev/repos/remarkjs/remark-lint.svg?fullname=)](https://github.com/remarkjs/remark-lint){target=_blank}

## Configuration in MegaLinter

- Enable remark-lint by adding `MARKDOWN_REMARK_LINT` in [ENABLE_LINTERS variable](https://oxsecurity.github.io/megalinter/6.7.1/configuration/#activation-and-deactivation)
- Disable remark-lint by adding `MARKDOWN_REMARK_LINT` in [DISABLE_LINTERS variable](https://oxsecurity.github.io/megalinter/6.7.1/configuration/#activation-and-deactivation)

- Enable **auto-fixes** by adding `MARKDOWN_REMARK_LINT` in [APPLY_FIXES variable](https://oxsecurity.github.io/megalinter/6.7.1/configuration/#apply-fixes)

| Variable                                         | Description                                                                                                                                                                                                         | Default value                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| MARKDOWN_DEFAULT_STYLE                           | For remark-lint to be active, MARKDOWN_DEFAULT_STYLE must be `remark-lint`                                                                                                                                          | `markdownlint`                                  |
| MARKDOWN_REMARK_LINT_ARGUMENTS                   | User custom arguments to add in linter CLI call<br/>Ex: `-s --foo "bar"`                                                                                                                                            |                                                 |
| MARKDOWN_REMARK_LINT_FILTER_REGEX_INCLUDE        | Custom regex including filter<br/>Ex: `(src\|lib)`                                                                                                                                                                  | Include every file                              |
| MARKDOWN_REMARK_LINT_FILTER_REGEX_EXCLUDE        | Custom regex excluding filter<br/>Ex: `(test\|examples)`                                                                                                                                                            | Exclude no file                                 |
| MARKDOWN_REMARK_LINT_CLI_LINT_MODE               | Override default CLI lint mode<br/>- `file`: Calls the linter for each file<br/>- `list_of_files`: Call the linter with the list of files as argument<br/>- `project`: Call the linter from the root of the project | `file`                                          |
| MARKDOWN_REMARK_LINT_FILE_EXTENSIONS             | Allowed file extensions. `"*"` matches any extension, `""` matches empty extension. Empty list excludes all files<br/>Ex: `[".py", ""]`                                                                             | `[".md"]`                                       |
| MARKDOWN_REMARK_LINT_FILE_NAMES_REGEX            | File name regex filters. Regular expression list for filtering files by their base names using regex full match. Empty list includes all files<br/>Ex: `["Dockerfile(-.+)?", "Jenkinsfile"]`                        | Include every file                              |
| MARKDOWN_REMARK_LINT_PRE_COMMANDS                | List of bash commands to run before the linter                                                                                                                                                                      | None                                            |
| MARKDOWN_REMARK_LINT_POST_COMMANDS               | List of bash commands to run after the linter                                                                                                                                                                       | None                                            |
| MARKDOWN_REMARK_LINT_CONFIG_FILE                 | remark-lint configuration file name</br>Use `LINTER_DEFAULT` to let the linter find it                                                                                                                              | `.remarkrc`                                     |
| MARKDOWN_REMARK_LINT_RULES_PATH                  | Path where to find linter configuration file                                                                                                                                                                        | Workspace folder, then MegaLinter default rules |
| MARKDOWN_REMARK_LINT_DISABLE_ERRORS              | Run linter but consider errors as warnings                                                                                                                                                                          | `true`                                          |
| MARKDOWN_REMARK_LINT_DISABLE_ERRORS_IF_LESS_THAN | Maximum number of errors allowed                                                                                                                                                                                    | `0`                                             |

## IDE Integration

Use remark-lint in your favorite IDE to catch errors before MegaLinter !

|                                                                   <!-- -->                                                                   | IDE                                                  | Extension Name                                                                                            |                                                Install                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------:|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------:|
|  <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/atom.ico" alt="" height="32px" class="megalinter-icon"></a>   | [Atom](https://atom.io/)                             | [linter-remark](https://github.com/wooorm/linter-remark)                                                  |               [Visit Web Site](https://github.com/wooorm/linter-remark){target=_blank}                |
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/sublime.ico" alt="" height="32px" class="megalinter-icon"></a> | [Sublime Text](https://www.sublimetext.com/)         | [SublimeLinter-contrib-remark-lint](https://packagecontrol.io/packages/SublimeLinter-contrib-remark-lint) | [Visit Web Site](https://packagecontrol.io/packages/SublimeLinter-contrib-remark-lint){target=_blank} |
|   <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/vim.ico" alt="" height="32px" class="megalinter-icon"></a>   | [vim](https://www.vim.org/)                          | [ale](https://github.com/w0rp/ale)                                                                        |                     [Visit Web Site](https://github.com/w0rp/ale){target=_blank}                      |
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/vscode.ico" alt="" height="32px" class="megalinter-icon"></a>  | [Visual Studio Code](https://code.visualstudio.com/) | [vscode-remark-lint](https://github.com/drewbourne/vscode-remark-lint)                                    |           [Visit Web Site](https://github.com/drewbourne/vscode-remark-lint){target=_blank}           |

## MegaLinter Flavours

This linter is available in the following flavours

|                                                                         <!-- -->                                                                         | Flavor                                                                  | Description               | Embedded linters |                                                                                                                                                                     Info |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------|:--------------------------|:----------------:|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/mega-linter-square.png" alt="" height="32px" class="megalinter-icon"></a> | [all](https://oxsecurity.github.io/megalinter/6.7.1/supported-linters/) | Default MegaLinter Flavor |       106        | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter) |

## Behind the scenes

### How are identified applicable files

- File extensions: `.md`

<!-- markdownlint-disable -->
<!-- /* cSpell:disable */ -->
### How the linting is performed

- remark-lint is called one time by identified file (`file` CLI lint mode)

### Example calls

```shell
remark --frail myfile.md
```

```shell
remark --frail --rc-path .remarkrc myfile.md
```

```shell
remark --frail -o --rc-path .remarkrc myfile.md
```


### Help content

```shell
Usage: remark [options] [path | glob ...]

  Command line interface to inspect and change markdown files with remark

Options:

  -h  --help                              output usage information
  -v  --version                           output version number
  -o  --output [path]                     specify output location
  -r  --rc-path <path>                    specify configuration file
  -i  --ignore-path <path>                specify ignore file
  -s  --setting <settings>                specify settings
  -e  --ext <extensions>                  specify extensions
  -u  --use <plugins>                     use plugins
  -w  --watch                             watch for changes and reprocess
  -q  --quiet                             output only warnings and errors
  -S  --silent                            output only errors
  -f  --frail                             exit with 1 on warnings
  -t  --tree                              specify input and output as syntax tree
      --report <reporter>                 specify reporter
      --file-path <path>                  specify path to process as
      --ignore-path-resolve-from dir|cwd  resolve patterns in `ignore-path` from its directory or cwd
      --ignore-pattern <globs>            specify ignore patterns
      --silently-ignore                   do not fail when given ignored files
      --tree-in                           specify input as syntax tree
      --tree-out                          output syntax tree
      --inspect                           output formatted syntax tree
      --[no-]stdout                       specify writing to stdout (on by default)
      --[no-]color                        specify color in report (on by default)
      --[no-]config                       search for configuration files (on by default)
      --[no-]ignore                       search for ignore files (on by default)

Examples:

  # Process `input.md`
  $ remark input.md -o output.md

  # Pipe
  $ remark < input.md > output.md

  # Rewrite all applicable files
  $ remark . -o
```

### Installation on mega-linter Docker image

- NPM packages (node.js):
  - [remark-cli](https://www.npmjs.com/package/remark-cli)
  - [remark-preset-lint-recommended](https://www.npmjs.com/package/remark-preset-lint-recommended)