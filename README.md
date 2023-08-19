# Google Sheets Integration with ChatGPT

This project demonstrates how to integrate ChatGPT responses directly into Google Sheets using the OpenAI API and Google Apps Script.

## Overview

The goal of this project is to fetch ChatGPT responses and populate a Google Sheets spreadsheet with the simplified text. The integration is achieved through Google Apps Script and the OpenAI API.

## Prerequisites

- Google Account
- OpenAI API Key (Sign up for OpenAI and generate a secret key)
- Access to Google Sheets

## Getting Started

1. Clone this repository:
   ```
   git clone https://github.com//gpt_integration.git
   cd gpt_integration
   ```

2. Set up your OpenAI API Key:
   - Sign up for OpenAI and generate an API key.
   - Copy the API key and keep it secure.

3. Set up Google Apps Script:
   - Open your Google Sheets document.
   - Go to Extensions > Apps Script to open the script editor.
   - Rename the project to "GPT Integration" and replace the default code with the code provided in this repository.

4. Create a custom formula:
   - Create a new file named "formula" within the script editor.
   - Define the "GPT_SIMPLIFY" formula to simplify text using ChatGPT API.

5. Add a custom menu to the spreadsheet:
   - Create a new file named "menu" within the script editor.
   - Define the "gptSimplifyMenu" function and add the custom menu to the user interface.

6. Test the functionality:
   - Reload the Google Sheets document.
   - The custom menu "GPT Functions" should appear. Use the "GPT SIMPLIFY" option to fetch and display simplified text.

## Usage

1. Select the cell containing the text you want to simplify.
2. Use the custom menu option "GPT SIMPLIFY" to populate adjacent cells with simplified text.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```










