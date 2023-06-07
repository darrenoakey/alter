# README for alter

![Alter header](./alter.png)

`alter` is a command-line tool that takes a list of files followed by instructions on what to do with them. It leverages the OpenAI API and the GPT-4 model to modify the files based on the provided instructions. When finished, it displays to the console every file that was changed and a message detailing the changes. Most importantly, altered files will have their old versions backed up in a `bak` directory underneath the current one, allowing for easy rollback if necessary.

## Usage

1. Place your OpenAI API key in a file called `openai_api_key.txt` within the `~/.openai/` directory.
2. Run the `alter` command in your terminal: `./alter <list_of_files> <instructions>`

## Examples

### Single file example

To alter a file named `example.txt`, run the command:

```
./alter example.txt "Change this sentence to something else."
```

### Multiple files example - HTML and CSS

To alter an HTML file named `index.html` and a CSS file named `styles.css`, run the command:

```
./alter index.html styles.css "Update the header to a different color and replace the main headline with 'Welcome to Our Website'."
```

### Multiple files example - JavaScript

To alter two JavaScript files named `script1.js` and `script2.js`, run the command:

```
./alter script1.js script2.js "Modify the function in script1.js to return the sum of two numbers and update the event listener in script2.js to call this new function."
```

Once the script has successfully completed running, the changed files will be updated accordingly, a reply message will be displayed in the terminal, and backup versions of the altered files will be stored in the `bak` directory.

## Note

The files can be any format and do not have to be JSON. The content of the files should be plain text so that it can be correctly processed by the script. 