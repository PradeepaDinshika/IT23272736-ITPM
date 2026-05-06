# Singlish to Sinhala Transliteration Test Automation

This project contains an automated testing script to verify the accuracy of a Singlish-to-Sinhala chat translator. The automation is built using Python, Playwright for browser automation, and OpenPyXL for reading and writing test cases from an Excel file.

## Prerequisites

Ensure you have the following installed on your system:
- [Python 3.8+](https://www.python.org/downloads/)
- pip (Python package installer)

## Installation

The repository includes clear instructions on how to install dependencies and run the tests.

1. Clone the repository or download the project files.
   ```bash
   git clone https://github.com/PradeepaDinshika/IT23272736-ITPM.git
   cd IT23272736-ITPM
   ```

2. Install the required Python packages:
   ```bash
   pip install playwright openpyxl
   ```
   *(Alternatively, if using the provided requirements file: `pip install -r it23272736_Requirements.txt`)*

3. Install the Playwright browsers required for automation:
   ```bash
   playwright install
   ```

## Running the Tests

To execute the test automation script and process the test cases in the Excel file, run the following command in your terminal:

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Command-Line Arguments Explained:
- `--excel`: Specifies the path to the Excel file containing the test cases (`Assignment 1 - Test cases.xlsx`).
- `--url`: The target URL of the chat translator frontend.
- `--wait-ms`: The delay time in milliseconds to wait for the output to generate (e.g., `5000` for 5 seconds).
- `--type-delay-ms`: The delay between keystrokes in milliseconds to simulate human typing (`80`).
- `--slow-mo-ms`: Slows down Playwright operations to make the UI execution visible (`200`).
- `--save-every`: Specifies how frequently to save the Excel output (e.g., `1` saves after every test case).
- `--keep-open`: Keeps the browser window open after the tests have finished running.

## Project Structure

- `test_automation.py`: The main Python script that contains the Playwright automation logic.
- `Assignment 1 - Test cases.xlsx`: The Excel file containing the Singlish inputs and expected Sinhala outputs. The script reads from this file and writes the actual outputs and pass/fail status back into it.
- `it23272736_Requirements.txt`: Contains the dependencies and the test execution command.

## Assignment Details
This project was created as part of the ITPM Module Assessment.
