Here are the detailed instructions for the 30-minute lab in Part 3, including the setup process for GitHub Copilot in VS Code, and some sample prompts for working with a Java project in a GitHub repository.

---

### **Lab 1: Getting Started with GitHub Copilot (30 minutes)**

#### **Objective:**
By the end of this lab, participants will have GitHub Copilot installed in VS Code and use it to scaffold a Java project in a GitHub repository.

---

### **Step-by-Step Instructions**

#### **1. Install Visual Studio Code (VS Code)**

- If not already installed, download and install **VS Code** from [here](https://code.visualstudio.com/Download).
- Follow the installation instructions for your operating system (Windows, macOS, or Linux).

---

#### **2. Install GitHub Copilot Extension for VS Code**

1. **Open VS Code**.
2. Go to the **Extensions** view by clicking on the Extensions icon in the Activity Bar on the side of the window (or press `Ctrl+Shift+X` on Windows/Linux, `Cmd+Shift+X` on macOS).
3. In the Extensions search bar, type "GitHub Copilot".
4. Find the **GitHub Copilot** extension by GitHub, and click **Install**.
5. Once installed, click **Sign in to GitHub** if prompted to authenticate GitHub Copilot with your GitHub account.
6. Follow the sign-in instructions in the pop-up browser window to authenticate with GitHub and authorize Copilot.

---

#### **3. work wth prompts**

#### Useful GitHub Copilot Prompts for the Spring AI Repository

1. **Generate a new Spring REST Controller to handle AI requests:**
  Sure! Here are the prompts formatted for a markdown file:

markdown
## Useful GitHub Copilot Prompts for Spring AI Repository

1. **Generate a new Spring REST Controller to handle AI requests:**

   Generate a new Spring REST Controller named `NewAiController` that handles HTTP GET requests at `/ai/new` and uses the `ChatClient` to process a message parameter.


2. **Create a unit test for `StuffController`:**

   Create a unit test for the `StuffController` class to test the `/ai/stuff` endpoint with different `message` and `stuffit` parameters.


3. **Add a new prompt template for generating AI responses:**

   Add a new prompt template file named `new-prompt.st` in the `resources/prompts` directory and update `PromptTemplateController` to use this new template.


4. **Document the `PromptTemplateController` functionality:**

   Document the functionality of the `PromptTemplateController` class, explaining how it uses the `PromptTemplate` class and the `joke-prompt.st` file to generate AI responses.


5. **Explain how to configure Azure OpenAI deployments:**

   Explain how to configure Azure OpenAI deployments for this project, including setting the necessary environment variables and updating the `application.properties` file.


6. **Add a new endpoint to `RagController` for detailed bike information:**

   Add a new endpoint to the `RagController` class that accepts a `bikeName` parameter and returns detailed information about the specified bike using the `bikes.json` data.


7. **Create a new README section for the `StuffController`:**

   Create a new section in the `README.md` file that explains the functionality of the `StuffController` class and provides examples of how to use the `/ai/stuff` endpoint.


8. **Implement a new service class for handling AI requests:**

   Implement a new service class named `AiRequestService` that handles AI requests by interacting with the `ChatClient` and `PromptTemplate` classes.


9. **Add logging to `PromptTemplateController`:**

   Add logging to the `PromptTemplateController` class to log incoming requests and the generated AI responses.


10. **Update the `CONTRIBUTING.md` file with AI-specific guidelines:**
 
    Update the `CONTRIBUTING.md` file to include guidelines for contributing to the AI-related code, including best practices for working with the `ChatClient` and `PromptTemplate` classes.
 


   Generate a new Spring REST Controller named `NewAiController` that handles HTTP GET requests at `/ai/new` and uses the `ChatClient` to process a message parameter.


2. **Create a unit test for `StuffController`:**

   Create a unit test for the `StuffController` class to test the `/ai/stuff` endpoint with different `message` and `stuffit` parameters.


3. **Add a new prompt template for generating AI responses:**

   Add a new prompt template file named `new-prompt.st` in the `resources/prompts` directory and update `PromptTemplateController` to use this new template.


4. **Document the `PromptTemplateController` functionality:**

   Document the functionality of the `PromptTemplateController` class, explaining how it uses the `PromptTemplate` class and the `joke-prompt.st` file to generate AI responses.


5. **Explain how to configure Azure OpenAI deployments:**

   Explain how to configure Azure OpenAI deployments for this project, including setting the necessary environment variables and updating the `application.properties` file.


6. **Add a new endpoint to `RagController` for detailed bike information:**

   Add a new endpoint to the `RagController` class that accepts a `bikeName` parameter and returns detailed information about the specified bike using the `bikes.json` data.


7. **Create a new README section for the `StuffController`:**

   Create a new section in the `README.md` file that explains the functionality of the `StuffController` class and provides examples of how to use the `/ai/stuff` endpoint.


8. **Implement a new service class for handling AI requests:**

   Implement a new service class named `AiRequestService` that handles AI requests by interacting with the `ChatClient` and `PromptTemplate` classes.


9. **Add logging to `PromptTemplateController`:**

   Add logging to the `PromptTemplateController` class to log incoming requests and the generated AI responses.


10. **Update the `CONTRIBUTING.md` file with AI-specific guidelines:**
 
    Update the `CONTRIBUTING.md` file to include guidelines for contributing to the AI-related code, including best practices for working with the `ChatClient` and `PromptTemplate` classes.
 

