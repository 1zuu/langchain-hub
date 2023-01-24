# LangChainHub

[Warning: very beta, may change drastically]

Taking inspiration from Hugging Face Hub, this is collection of all artifacts useful for working with LangChain chains.
To start, this focuses on prompts.
This is intended to be a central place to upload and share prompts.
It is intended to be very community driven and we hope that people will contribute their own prompts.
Please see below for instructions on loading and uploading prompts.

## Loading

All prompts can be loaded from LangChain by specifying the desired path.
The path should be relative to the `prompts` folder here.
For example, if there is a file at `prompts/qa/stuff/basic/prompt.yaml`, the path you want to specify is `qa/stuff/basic/prompt.yaml`

Once you have that path, you can load it in the following manner:

```python
from langchain.prompts import load_prompt
prompt = load_prompt('lc://prompts/qa/stuff/basic/prompt.yaml')
```

## Uploading

There are three methods for uploading prompts: `json`, `yaml`, and `python`.
The suggested options are `json` and `yaml`, but we provide `python` as an option for more flexibility.
Please see the below sections for instructions for uploading each format.

You should upload your prompt file to a folder in the appropriate use case section.
In addition to the prompt file, you should also add a README.md for that folder, including any relevant information about prompt.
This can be how it was created, what it should be used for, what the variables mean, etc.

### `json`
To get a properly formatted json file, if you have prompt in memory in Python you can run:
```python
prompt.save("file_name.json")
```

Replace `"file_name"` with the desired name of the file.

### `yaml`
To get a properly formatted yaml file, if you have prompt in memory in Python you can run:
```python
prompt.save("file_name.yaml")
```

Replace `"file_name"` with the desired name of the file.


### `python`
To get a properly formatted Python file, you should upload a Python file that exposes a `PROMPT` variable.
This is the variable that will be loaded.
This variable should be an instance of a subclass of BasePromptTemplate in LangChain.
