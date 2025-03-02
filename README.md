# Combo File Checker

## Description
This is a command-line tool designed for Termux in Python that functions as a Combo File Checker. It processes one or more text files containing combinations of email/username and password, separated by a delimiter. 

## Features
- **Input**: Accepts one or more file paths as command-line arguments.
- **Format Detection**: Automatically detects the delimiter in the combo file.
- **Validation**: Checks each line for a valid format and validates email addresses.
- **Duplicate Removal**: Removes duplicate entries, ignoring case sensitivity.
- **Output**: Displays the count of valid, invalid, and duplicate entries.
- **Optional**: Saves cleaned entries and invalid entries to separate files.

## Usage

### Command-line Arguments
- `files`: Input file paths.
- `-d` or `--delimiter`: Specify the delimiter.
- `-o` or `--output`: Output file for cleaned entries.
- `-i` or `--invalid`: Output file for invalid entries.

### Example
```sh
python combo_checker.py file1.txt file2.txt -d ':' -o cleaned.txt -i invalid.txt
```

## Installation
Ensure you have Python 3 installed on your system. This tool requires the `tqdm` library for the progress bar:
```sh
pip install tqdm
```

## How It Works
1. **Input Files**: The tool accepts multiple text files as input.
2. **Delimiter Detection**: If a delimiter is not specified, the tool detects the most common delimiter in the file.
3. **Validation**: Each line is checked for a valid email/username and password format. Email addresses are further validated for a basic format.
4. **Duplicate Removal**: Entries are normalized to lowercase and duplicates are removed.
5. **Output**: The counts of valid, invalid, and duplicate entries are displayed. Optionally, valid entries and invalid entries can be saved to separate files.

## Performance
The tool is designed to handle large files efficiently and uses the `tqdm` library for a progress bar to track the processing status.

## Code Quality
The code is structured for readability and maintainability, with clear comments and modular functions.

## Future Enhancements
- **Proxy Support**: Integrate proxy support for checking passwords against online services.
- **Custom Filters**: Add support for filtering entries based on custom patterns.
- **Progress Display**: Improve the progress display with more detailed information.
- **Encoding Support**: Automatically detect and process various text encodings (UTF-8, ASCII, etc.).

## License
This project is licensed under the MIT License.
