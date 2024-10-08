# toml_cfg_tool  

## Table of Contents

- [Prerequisites](#prerequisites)
- [Description](#description)
- [Features](#features)
  - [Arguments](#arguments)
  - [Examples](#examples)
    - [Screenshots](#screenshots)
- [Installation and Setup](#installation-and-setup)
  - [Requirements.txt](#requirements.txt)
  - [Virtual Environment](#virtual-environment)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

- [Python](https://www.python.org/downloads/)

## Description

A tool to create toml and cfg files for use in python projects, it can also simultaneously update aspects that are common between the two files.

## Features

### Arguments 

The tool accepts the following arguments:

- `--show`: Show the current configuration. (only shows the options that can be updated)
- `--author`: Update the project author.
- `--name`: Update the project name.
- `--version`: Update the project version.
- `--description`: Update the project description.
- `--requires-python`: Update the required Python version.
- `--license`: Update the project license.
- `--workflow_files`: Add GitHub Actions workflow files, and scripts.
- `--create-templates`: Create template setup.cfg and pyproject.toml files if they do not exist.
- `--backup`: Backup existing configuration files before making changes.
- `--dry-run`: Show changes without writing to files.

### Examples 

- Show the current configuration:

```shell
toml_cfg_tool --show
```

- Create template configuration files:

```shell
toml_cfg_tool --create-templates
```

- Create the workflow files:

```shell
toml_cfg_tool --workflow_files
```

- Show changes without writing to files:

```shell
toml_cfg_tool --dry-run --name "New Project Name" --author "New Project Author" --version "1.0.0" --description "New Project Description" --requires-python ">=3.6" --license "MIT"
```

- Update the project version:

```shell
pip install toml_cfg_tool
```

- Update the project name:

```shell
toml_cfg_tool --name "New Project Name"
```

- Update the project author and backup existing files:

```shell
toml_cfg_tool --author "New Project Author" --backup path/to/backups.bak
```

- Create template configuration files and workflow files while updating the project name, author, and version:

```shell
toml_cfg_tool --create-templates --workflow_files --name "New Project Name" --author "New Project Author" --version "1.0.0"
```

### Screenshots

- Show the current configuration (only shows the options that can be updated):

![](https://github.com/VinnyVanGogh/toml_cfg_tool/blob/main/.github/images/show_example.png?raw=true)

- Create template configuration files:

![Create the template .toml and .cfg files](https://github.com/VinnyVanGogh/toml_cfg_tool/blob/main/.github/images/create_templates_example.png?raw=true)

- Create the CONTRIBUTING.md file:

![CONTRIBUTING.md](https://github.com/VinnyVanGogh/toml_cfg_tool/blob/main/.github/images/contrib_example.png?raw=true)

- Update all available fields:

![](https://github.com/VinnyVanGogh/toml_cfg_tool/blob/main/.github/images/all_example.png?raw=true)

## Installation and Setup

### To install the tool, run the following command:

```shell
pip install toml_cfg_tool
```

### To check if the tool is installed, run the following command:

```shell
pip show toml_cfg_tool
```

**or** 

```shell
toml_cfg_tool --help
```

### Run the application:

**Any of the arguments can be used or excluded from the command below. The tool will only update the specified fields.**
    - Use dry-run to see changes without writing to files
    - Use backup to backup existing files before making changes
    - Use create-templates to create template configuration files
    - Use workflow_files to create GitHub Actions workflow files

```shell
toml_cfg_tool --name "New Project Name" --author "New Project Author" --version "1.0.0" --description "New Project Description" --requires-python ">=3.6" --license "MIT"
```

## Contributing

![Contributing](.github/CONTRIBUTING.md)

## License

This project is licensed under the [MIT License](MIT_LICENSE). You can find the full text of the license in the [LICENSE](MIT_LICENSE) file.
