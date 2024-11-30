# regmonkey_repository_document

## Description

This project provides a shell script to set up developer documentation and lincese for a project.
It allows you to choose a template, update the document date, and set the project name in the documentation files.

## Installation

Clone the repository to your local machine:

```bash
git clone <repository-url>
cd <repository-directory>
```

After installation,

1. give the permission for each scripts located at `script/` directory
2. export `script/` PATH at your terminal

## How to use the script

### `set_license` script

```bash
set_developer_document.sh [-d target_directory] [-p project_name]
```

<strong > &#9654;&nbsp; Options</strong>

- `-d` target_directory: The directory where the documentation will be set up. Default is `./docs`.
- `-p` project_name: The name of the project. Default is the name of the current directory.

<strong > &#9654;&nbsp; How it works</strong>

1. Choose Template: The script lists available templates from the `document_template` directory and prompts you to choose one.
2. Update Document Date: The script updates the date-modified field in the documentation files to the current date.
3. Update Project Name: The script replaces the placeholder `<default-package-name-for-rename>` with the provided project name in the documentation files.

### `set_license` script

<strong > &#9654;&nbsp; How it works</strong>

1. **List Available Licenses**: The script lists available license templates from the `license_template` directory.
2. **Choose License**: You will be prompted to choose a license type from the listed templates.
3. **Validate License File**: The script checks if the chosen license file exists.
4. **Confirm Writing License**: You will be prompted to confirm if you want to write the new LICENSE file.
5. **Input License Details**: If confirmed, you will be prompted to enter the following details:
    - **Year**: The year from which your license is valid.
    - **Owner**: The copyright owner.
    - **Program Name**: The program name (only required for GPL 3.0).
6. **Write LICENSE File**: The script customizes the chosen license template with the provided details and writes it to a `LICENSE` file in the current directory.

- **Choose License**:

    ```sh
    please choose your license type from the above: 
    ```

- **Confirm Writing License**:

    ```sh
    Are you sure to newly write $LICENSEFILE LICENSE? (y/N): 
    ```

- **Year**:

    ```sh
    From what year your license is valid (yyyy): 
    ```

- **Owner**:

    ```sh
    Who is copyright owner: 
    ```

- **Program Name** (only for GPL 3.0):

    ```sh
    What is the program name (only in GPL 3.0): 
    ```

<strong > &#9654;&nbsp; Example Run</strong>

```bash
$ ./set_license
MIT.txt
GPL-3.0.txt
please choose your license type from the above: MIT
Are you sure to newly write MIT LICENSE? (y/N): y
From what year your license is valid (yyyy): 2023
Who is copyright owner: John Doe
What is the program name (only in GPL 3.0): MyProgram
```

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.

References
----------

- [spdx/license-list-data](https://github.com/spdx/license-list-data/tree/main)
