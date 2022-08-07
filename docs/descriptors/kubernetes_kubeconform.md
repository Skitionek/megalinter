<!-- markdownlint-disable MD033 MD041 -->
<!-- @generated by .automation/build.py, please do not update manually -->

<div align="center">
  <a href="https://github.com/yannh/kubeconform#readme" target="blank" title="Visit linter Web Site">
    <img src="https://user-images.githubusercontent.com/19731161/142411871-f695e40c-bfa8-43ca-97c0-94c256749732.png" alt="kubeconform" height="150px" class="megalinter-banner">
  </a>
</div>

[![GitHub last commit](https://img.shields.io/github/last-commit/yannh/kubeconform)](https://github.com/yannh/kubeconform/commits)

`kubeconform` is a schema-aware Kubernetes manifest validation tool, that tends to have more up-to-date schema definitions than `kubeval`.

## kubeconform documentation

- Version in MegaLinter: **0.4.12**
- Visit [Official Web Site](https://github.com/yannh/kubeconform#readme){target=_blank}

[![kubeconform - GitHub](https://gh-card.dev/repos/yannh/kubeconform.svg?fullname=)](https://github.com/yannh/kubeconform){target=_blank}

## Configuration in MegaLinter

- Enable kubeconform by adding `KUBERNETES_KUBECONFORM` in [ENABLE_LINTERS variable](https://oxsecurity.github.io/megalinter/latest/configuration/#activation-and-deactivation)
- Disable kubeconform by adding `KUBERNETES_KUBECONFORM` in [DISABLE_LINTERS variable](https://oxsecurity.github.io/megalinter/latest/configuration/#activation-and-deactivation)

| Variable                                           | Description                                                                                                                                                                                                         | Default value                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| KUBERNETES_KUBECONFORM_ARGUMENTS                   | User custom arguments to add in linter CLI call<br/>Ex: `-s --foo "bar"`                                                                                                                                            |                              |
| KUBERNETES_KUBECONFORM_FILTER_REGEX_INCLUDE        | Custom regex including filter<br/>Ex: `(src\|lib)`                                                                                                                                                                  | Include every file           |
| KUBERNETES_KUBECONFORM_FILTER_REGEX_EXCLUDE        | Custom regex excluding filter<br/>Ex: `(test\|examples)`                                                                                                                                                            | Exclude no file              |
| KUBERNETES_KUBECONFORM_CLI_LINT_MODE               | Override default CLI lint mode<br/>- `file`: Calls the linter for each file<br/>- `list_of_files`: Call the linter with the list of files as argument<br/>- `project`: Call the linter from the root of the project | `list_of_files`              |
| KUBERNETES_KUBECONFORM_FILE_EXTENSIONS             | Allowed file extensions. `"*"` matches any extension, `""` matches empty extension. Empty list excludes all files<br/>Ex: `[".py", ""]`                                                                             | `[".yml", ".yaml", ".json"]` |
| KUBERNETES_KUBECONFORM_FILE_NAMES_REGEX            | File name regex filters. Regular expression list for filtering files by their base names using regex full match. Empty list includes all files<br/>Ex: `["Dockerfile(-.+)?", "Jenkinsfile"]`                        | Include every file           |
| KUBERNETES_KUBECONFORM_PRE_COMMANDS                | List of bash commands to run before the linter                                                                                                                                                                      | None                         |
| KUBERNETES_KUBECONFORM_POST_COMMANDS               | List of bash commands to run after the linter                                                                                                                                                                       | None                         |
| KUBERNETES_KUBECONFORM_DISABLE_ERRORS              | Run linter but consider errors as warnings                                                                                                                                                                          | `false`                      |
| KUBERNETES_KUBECONFORM_DISABLE_ERRORS_IF_LESS_THAN | Maximum number of errors allowed                                                                                                                                                                                    | `0`                          |
| KUBERNETES_DIRECTORY                               | Directory containing KUBERNETES files                                                                                                                                                                               | `kubernetes`                 |

## MegaLinter Flavours

This linter is available in the following flavours

|                                                                         <!-- -->                                                                         | Flavor                                                                                 | Description                                           | Embedded linters |                                                                                                                                                                                                 Info |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------|:------------------------------------------------------|:----------------:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/mega-linter-square.png" alt="" height="32px" class="megalinter-icon"></a> | [all](https://oxsecurity.github.io/megalinter/latest/supported-linters/)               | Default MegaLinter Flavor                             |       105        |                             ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter) |
|    <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/documentation.ico" alt="" height="32px" class="megalinter-icon"></a>    | [documentation](https://oxsecurity.github.io/megalinter/latest/flavors/documentation/) | MegaLinter for documentation projects                 |        45        | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-documentation/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-documentation) |
|       <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/dotnet.ico" alt="" height="32px" class="megalinter-icon"></a>        | [dotnet](https://oxsecurity.github.io/megalinter/latest/flavors/dotnet/)               | Optimized for C, C++, C# or VB based projects         |        54        |               ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-dotnet/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-dotnet) |
|         <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/go.ico" alt="" height="32px" class="megalinter-icon"></a>          | [go](https://oxsecurity.github.io/megalinter/latest/flavors/go/)                       | Optimized for GO based projects                       |        47        |                       ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-go/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-go) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/java.ico" alt="" height="32px" class="megalinter-icon"></a>         | [java](https://oxsecurity.github.io/megalinter/latest/flavors/java/)                   | Optimized for JAVA based projects                     |        47        |                   ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-java/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-java) |
|     <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/javascript.ico" alt="" height="32px" class="megalinter-icon"></a>      | [javascript](https://oxsecurity.github.io/megalinter/latest/flavors/javascript/)       | Optimized for JAVASCRIPT or TYPESCRIPT based projects |        54        |       ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-javascript/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-javascript) |
|         <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/php.ico" alt="" height="32px" class="megalinter-icon"></a>         | [php](https://oxsecurity.github.io/megalinter/latest/flavors/php/)                     | Optimized for PHP based projects                      |        49        |                     ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-php/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-php) |
|       <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/python.ico" alt="" height="32px" class="megalinter-icon"></a>        | [python](https://oxsecurity.github.io/megalinter/latest/flavors/python/)               | Optimized for PYTHON based projects                   |        53        |               ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-python/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-python) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/ruby.ico" alt="" height="32px" class="megalinter-icon"></a>         | [ruby](https://oxsecurity.github.io/megalinter/latest/flavors/ruby/)                   | Optimized for RUBY based projects                     |        46        |                   ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-ruby/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-ruby) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/rust.ico" alt="" height="32px" class="megalinter-icon"></a>         | [rust](https://oxsecurity.github.io/megalinter/latest/flavors/rust/)                   | Optimized for RUST based projects                     |        46        |                   ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-rust/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-rust) |
|     <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/salesforce.ico" alt="" height="32px" class="megalinter-icon"></a>      | [salesforce](https://oxsecurity.github.io/megalinter/latest/flavors/salesforce/)       | Optimized for Salesforce based projects               |        48        |       ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-salesforce/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-salesforce) |
|      <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/security.ico" alt="" height="32px" class="megalinter-icon"></a>       | [security](https://oxsecurity.github.io/megalinter/latest/flavors/security/)           | Optimized for security                                |        21        |           ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-security/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-security) |
|        <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/swift.ico" alt="" height="32px" class="megalinter-icon"></a>        | [swift](https://oxsecurity.github.io/megalinter/latest/flavors/swift/)                 | Optimized for SWIFT based projects                    |        46        |                 ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-swift/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-swift) |
|      <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/terraform.ico" alt="" height="32px" class="megalinter-icon"></a>      | [terraform](https://oxsecurity.github.io/megalinter/latest/flavors/terraform/)         | Optimized for TERRAFORM based projects                |        51        |         ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter-terraform/v6) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter-terraform) |

## Behind the scenes

### How are identified applicable files

- Activated only if sub-directory `kubernetes` is found. (directory name can be overridden with `KUBERNETES_DIRECTORY`)
- File extensions: `.yml`, `.yaml`, `.json`
- Detected file content (regex): `apiVersion:`, `kustomize\.config\.k8s\.io`, `tekton`

<!-- markdownlint-disable -->
<!-- /* cSpell:disable */ -->
### How the linting is performed

- kubeconform is called once with the list of files as arguments (`list_of_files` CLI lint mode)

### Example calls

```shell
kubeconform myfile.yml
```

```shell
kubeconform -ignore-missing-schemas -skip SomeCRD,AnotherCRD -kubernetes-version '1.18.0' -strict myfile.yml
```


### Help content

```shell
Usage: kubeconform [OPTION]... [FILE OR FOLDER]...
  -cache string
      cache schemas downloaded via HTTP to this folder
  -cpu-prof string
      debug - log CPU profiling to file
  -exit-on-error
      immediately stop execution when the first error is encountered
  -h  show help information
  -ignore-filename-pattern value
      regular expression specifying paths to ignore (can be specified multiple times)
  -ignore-missing-schemas
      skip files with missing schemas instead of failing
  -insecure-skip-tls-verify
      disable verification of the server's SSL certificate. This will make your HTTPS connections insecure
  -kubernetes-version string
      version of Kubernetes to validate against, e.g.: 1.18.0 (default "master")
  -n int
      number of goroutines to run concurrently (default 4)
  -output string
      output format - json, junit, tap, text (default "text")
  -reject string
      comma-separated list of kinds to reject
  -schema-location value
      override schemas location search path (can be specified multiple times)
  -skip string
      comma-separated list of kinds to ignore
  -strict
      disallow additional properties not in schema
  -summary
      print a summary at the end (ignored for junit output)
  -verbose
      print results for all resources (ignored for tap and junit output)
```

### Installation on mega-linter Docker image

- Dockerfile commands :
```dockerfile
RUN ML_THIRD_PARTY_DIR="/third-party/kubeconform" \
    && KUBECONFORM_VERSION=v0.4.12 \
    && mkdir -p ${ML_THIRD_PARTY_DIR} \
    && wget -P ${ML_THIRD_PARTY_DIR} -q https://github.com/yannh/kubeconform/releases/download/$KUBECONFORM_VERSION/kubeconform-linux-amd64.tar.gz \
    && tar xf ${ML_THIRD_PARTY_DIR}/kubeconform-linux-amd64.tar.gz --directory ${ML_THIRD_PARTY_DIR} \
    && mv ${ML_THIRD_PARTY_DIR}/kubeconform /usr/local/bin \
    && find ${ML_THIRD_PARTY_DIR} -type f -not -name 'LICENSE*' -delete -o -type d -empty -delete

```
