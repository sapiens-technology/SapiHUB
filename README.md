Proprietary software developed by Sapiens Technology®️ to partition, move, repair, delete, download, and upload models in the Sapiens standard.

# SapiHUB

The SapiHUB is a computer program used to manage Sapiens Technology®️ models that exceed the conventional size of popular language models.

## Recommendation

Install Python 3.11 and create a virtual environment with that version.

Here's an example of how to do this on Linux or Mac:
---
<sub>On Linux and macOS:</sub>
```bash
python3.11 -m venv sapihub
```
```bash
cd sapihub
```
```bash
source bin/activate
```
<sub>On Windows:</sub>
```bash
python -m venv sapihub
```
```bash
cd sapihub
```
```bash
.\Scripts\activate
```
---

```bash
python3 --version
```

If version 3.11 is displayed, your environment was successfully created with the correct version. After that, simply install the package within the created environment.
```bash
Python 3.11.4
```
Linux:
```bash
Python 3.11.8
```

Update the pip package manager:
---
<sub>On Linux and macOS:</sub>
```bash
python3.11 -m pip install --upgrade pip --timeout 120
```
<sub>On Windows:</sub>
```bash
python -m pip install --upgrade pip --timeout 120
```
---


## Installation

Click [here](sapihub.md) to download the sapihub installer for your operating system.

```bash
pip install sapihub-1.0.0-py3-none-any.whl
```

## Usage

### Execution arguments

Aqui está a documentação dos argumentos em formato de tabela Markdown:

| Argument  | Type  | Default | Description                                                                 |
|-----------|-------|---------|-----------------------------------------------------------------------------|
| --div     | str   | ''      | Splits a model into multiple smaller parts.                                 |
| --parts   | int   | 2       | Number of files generated from the split.                                   |
| --save    | str   | ''      | Path where the result will be saved.                                        |
| --merge   | str   | ''      | Path to the first file of the split.                                        |
| --up      | str   | ''      | Path to the model that will be uploaded to the repository.                  |
| --repo    | str   | ''      | Username followed by "/" and the repository name.                           |
| --token   | str   | ''      | Hugging Face account access token.                                          |
| --user    | str   | ''      | Repository owner username.                                                  |
| --type    | str   | ''      | Repository type (model or dataset).                                         |
| --restart | flag  | False   | Enables periodic restart during large file loading.                         |
| --get     | str   | ''      | Username followed by "/" and the repository name to download.               |
| --move    | str   | ''      | Path of the model to be moved.                                              |
| --to      | str   | ''      | Destination folder path for the moved model.                                |
| --list    | flag  | False   | Lists models in the default directory.                                      |
| --repair  | str   | ''      | Path to the defective model that should be repaired.                        |
| --remove  | str   | ''      | Path to the model that should be removed.                                   |

### Examples

### Download model

```bash
sapihub --get sapiens-technology/model_name
```
Or:
```bash
sapihub --get model_name
```

### Model repair
In some cases, the model may become corrupted if there is not enough memory in the system at the time of execution or if the model is abruptly terminated in a non-conventional manner. If this happens, your model will not load in the next execution, or if it does, it will start returning nonsensical responses. In these cases, it is possible to repair the model so that it works correctly again:
```bash
sapihub --repair model_name
```

### Listing downloaded models

```bash
sapihub --list
```

### Deleting a model
```bash
sapihub --remove model_name
```

## Contributing

We do not accept contributions that may result in changing the original code.

Make sure you are using the appropriate version.

## License

This is proprietary software and its alteration and/or distribution without the developer's authorization is not permitted.
