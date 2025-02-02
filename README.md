# Ollama AI Blender Add-on

## Overview
The **Ollama AI Blender Add-on** integrates AI-assisted scripting into Blender, allowing users to generate Python scripts directly within Blender's UI using models such as `qwen2.5-coder`, `llama3.2`, and `deepseek-coder-v2`. The add-on provides an intuitive panel for interacting with the AI model, sending prompts, receiving responses, and executing scripts seamlessly in the Scripting workspace.

![OllamaBridge](https://github.com/SurgeonTalus/OllamaBlenderBridge/blob/main/Skjermbilde%202025-02-01%20kl.%2000.43.09.png)

## Features
- **Customizable AI Model**: Select from predefined models or specify a custom model.
- **Prompt Customization**: Define system prompts and user prompts for generating code.
- **Library Support**: Specify external libraries for AI-generated scripts.
- **Code Execution**: Run AI-generated scripts directly in the Blender Scripting workspace.
- **Non-Blocking Requests**: Send and receive prompts asynchronously to avoid UI freezing.
- **Response Enhancements**: Automatically enhance prompts with additional instructions.

## Installation
1. Download the Python script from this repository.
2. Open Blender and navigate to `Edit > Preferences > Add-ons`.
3. Click `Install...`, select the downloaded script, and enable the add-on.

## How to Use
### 1. Accessing the Add-on
- The add-on panel is located in the 3D View sidebar under the **Ollama** tab.

### 2. Configuring the AI Model
- Select a predefined AI model from the dropdown menu.
- Optionally, enter a custom model name.

### 3. Sending a Prompt
- Enter a **System Prompt** and **User Prompt**.
- (Optional) Specify a library that should be used.
- Click **Run & Execute** to send the prompt and receive a response.

### 4. Receiving and Executing Responses
- AI-generated Python scripts appear in the **Response** field.
- Click **Run Response in Scripting Tab** to execute the script.

### 5. Asynchronous Requests
- Use **Send Prompt** to send the request without blocking Blender.
- Use **Receive Prompt** to fetch the response later.

### 6. Resetting Defaults
- Click **Reset to Default** to restore the original settings.

## Technical Details
### Panel (`OLLAMA_PT_Panel`)
- Displays UI elements for user input, options, and actions.
- Allows users to configure AI prompts, select models, and execute commands.

### Operators
- **OLLAMA_OT_RunPrompt**: Sends a request and retrieves the AI-generated script.
- **OLLAMA_OT_SendPrompt**: Sends a request asynchronously.
- **OLLAMA_OT_ReceivePrompt**: Receives a previously sent response.
- **OLLAMA_OT_EnhancePrompt**: Enhances prompts with step-by-step instructions.
- **OLLAMA_OT_RunInScripting**: Executes the response in Blender’s scripting tab.

### Registration
- Registers and unregisters UI components and properties within Blender.
- Defines scene properties for storing user input and AI responses.

## Requirements
- **Blender**: 4.2 or later
- **Python**: 3.10 or later
- **Ollama AI Server**: Running on `localhost:11434`

## Troubleshooting
- **No response received?** Ensure the Ollama AI server is running and accessible.
- **UI freezing?** Use `Send Prompt` instead of `Run & Execute`.
- **Script errors?** Check the AI-generated script for syntax issues and modify it as needed.

## License
This project is licensed under the MIT License.

## Contributing
Feel free to submit pull requests or report issues to improve this add-on!
![BlenderAI12](https://raw.githubusercontent.com/SurgeonTalus/Blender-Scripting-AI-for-LM-Studio-Server/main/LM%20Studio%20BlenderBridge%20Images/BlenderAI12.png)
