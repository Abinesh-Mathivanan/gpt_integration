# gpt_integration

You could fetch ChatGPT responses directly to the Google Sheets with the help of OpenAI API

Step 1:

To begin, if you're not already registered with OpenAI, you should sign up for an account. Once you have an account, navigate to the API keys section located in the User tab.
Click on the button labeled "Create new secret key," and once it's generated, make sure to copy the key. Remember that this API key won't be visible again, so ensure you save it in a secure location.

Step 2:

Let's begin by accessing the app script associated with your spreadsheet. Rename the script to "GPT_integration". Additionally, rename the current file to "utils.gs". Within the "GPT_integration" script, establish a new function named "fetchData".

Step 3:

Next, let's proceed with setting up the custom formula. Start by creating a new file named "formula". Within this file, you'll establish a function called "GPT_SIMPLIFY".

The purpose of the "GPT_SIMPLIFY" formula is to simplify any given text input. The input data is retrieved from the spreadsheet. This function automatically receives data when you select a cell, a range of cells, or multiple cells in the spreadsheet.

The "systemContent" is defined as the first parameter passed to the "fetchData(systemContent, userContent)" function.

It's important to check whether the input is an Array. This step is necessary because the data provided to this function can either be a nested array or a simple string, depending on whether you've selected multiple cells or a single cell in the spreadsheet.


Step 4:

To proceed, let's create a new file named "menu". Within this file, we'll establish the function "gptSimplifyMenu." This function will serve as an alternative to the "GPT_SIMPLIFY" formula.

Take note of these specific aspects in the code:

Data sources are hardcoded using expressions like data[i][1]. This references the second column ("Simplified Passage") as depicted in the spreadsheet image above. In case you're utilizing different columns for storing data from ChatGPT, you'll need to adjust these expressions accordingly.

Data retrieval occurs only when the target cell is either empty or contains an error message. This approach is employed to prevent unnecessary API calls, optimizing the process.

If you encounter any variations in your data structure or usage, remember to tailor the code according to your specific requirements.

Step 5:

The function is now prepared for testing, but in order to make it visible within the spreadsheet, we'll need to provide the following guidelines. These instructions are meant to be implemented within the createCustomMenu() function:

To establish the menu, begin by defining it as follows: SpreadsheetApp.getUi().createMenu("GPT Functions"). This sets "GPT Functions" as the title that will appear in the spreadsheet tab.

Incorporate a function into the menu using menu.addItem("GPT SIMPLIFY", "gptSimplifyMenu"). In this line, the first parameter signifies the display title, while the second parameter specifies the function to be executed upon pressing.

Finally, add the newly created menu to the user interface using menu.addToUi().

The "onOpen" trigger executes automatically whenever the script-attached document is reloaded. As a result, it adds the menu to the spreadsheet, visible as depicted in the accompanying image.












