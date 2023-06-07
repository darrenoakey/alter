# README for alter

`alter` is a Python script to automatically modify a list of existing files according to a specified request by leveraging the power of the OpenAI API and the GPT-4 model. This script accepts input as a JSON object which must include existing files and a request for modification.

The response will be JSON formatted which includes:

- `reply`: a message to be shown to the user after the script is created.
- `files`: an array of {filename, content} objects.

Only files that are changed will be returned in the JSON response.

## Usage

1. Place your OpenAI API key in a file called `openai_api_key.txt` within the `~/.openai/` directory.
2. Prepare the input JSON object as described above, with existing files and a request for modification.
3. Run the script in your terminal with the input JSON object: `python3 alter.py <input_json>`

## Example

Using the following input JSON object:

```
{
  "files": {
    "alter": "<content_of_your_python_file>"
  },
  "request": "<your_modification_request_here>"
}
```

Run the script:

```
python3 alter.py <input_json>
```

Once the script has successfully completed running, the changed files will be updated accordingly and a reply message will be output in the terminal.

## Note

The content of the files should be properly formatted as a JSON object so that it can be correctly processed by the script. Invalid JSON or other tokens may cause the script to fail.