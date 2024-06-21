# Installation and Setup Guide

## Installing Requirements

The code works with Python >= 3.10 (possibly also earlier versions but this was not tested).
The code was tested using the Visual Studio Code IDE. Issues have been reported with other IDEs.

### Steps to Install

1. **Create a virtual environment in the root folder of the project (Python 3):**
    ```sh
    python -m venv myenv
    ```

2. **Activate the virtual environment:**

    - On Windows:
      ```sh
      myenv\Scripts\activate
      ```
    - On macOS and Linux:
      ```sh
      source myenv/bin/activate
      ```

3. **Install the requirements:**
    ```sh
    pip install -r requirements.txt
    ```

## Using OpenAI API

### Quick Setup

A quick way to use the OpenAI key is to create a `.env` file in the main project folder with the following content:
OPENAI_API_KEY=sk-your-api-key-here



### Secure Setup

#### Set OpenAI key on MacOS

1. **Open Terminal:** You can find it in the Applications folder or search for it using Spotlight (Command + Space).

2. **Edit Bash Profile:** Use the command to open the profile file in a text editor:
    ```sh
    nano ~/.bash_profile
    ```
    or for newer MacOS versions:
    ```sh
    nano ~/.zshrc
    ```

3. **Add Environment Variable:** In the editor, add the line below, replacing `your-api-key-here` with your actual API key:
    ```sh
    export OPENAI_API_KEY=your-api-key-here
    ```

4. **Save and Exit:** Press `Ctrl+O` to write the changes, followed by `Ctrl+X` to close the editor.

5. **Load Your Profile:** Use the command to load the updated profile:
    ```sh
    source ~/.bash_profile
    ```
    or
    ```sh
    source ~/.zshrc
    ```

6. **Verification:** Verify the setup by typing in the terminal. It should display your API key:
    ```sh
    echo $OPENAI_API_KEY
    ```

#### Set OpenAI key on Windows

1. **Open Command Prompt:** You can find it by searching "cmd" in the start menu.

2. **Set environment variable in the current session:** Use the command below, replacing `your-api-key-here` with your actual API key:
    ```sh
    setx OPENAI_API_KEY "your-api-key-here"
    ```

3. **Permanent setup:**

    - Right-click on 'This PC' or 'My Computer' and select 'Properties'.
    - Click on 'Advanced system settings'.
    - Click the 'Environment Variables' button.
    - In the 'System variables' section, click 'New...' and enter `OPENAI_API_KEY` as the variable name and your API key as the variable value.

4. **Verification:** To verify the setup, reopen the command prompt and type the command below. It should display your API key:
    ```sh
    echo %OPENAI_API_KEY%
    ```
