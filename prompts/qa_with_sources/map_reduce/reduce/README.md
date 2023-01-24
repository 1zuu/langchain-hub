# Description of QA with Sources Map Reduce Prompts

Prompt

## Compatible Chains

Below is a list of chains we expect this prompt to be compatible with.

1. {{Chain Name}}: {{Path to chain in module}}
2. ...

## Inputs

This is a description of the inputs that the prompt expects.

1. {{input_var}}: {{Description}}
2. ...


## Usage

Below is a code snippet for how to use the prompt.

```python
from langchain.prompts import load_prompt
from langchain.chains.qa_with_sources import load_qa_with_sources_chain

llm = ...
prompt = load_prompt('lc://prompts/qa_with_sources/map_reduce/reduce/<file-name>')
chain = load_qa_with_sources_chain(llm, chain_type="map_reduce", combine_prompt=prompt)
```

