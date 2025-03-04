# Part 2 - Java development using GitHub Copilot
## Workshop: AI-Driven Development: Enhancing Java with the latest AI Innovations

### Great reference for copilot instructions: 

https://github.com/bbenz/awesome-copilot-instructions/tree/main?tab=readme-ov-file

---

#### **Objective:**
By the end of this lab, participants will have GitHub Copilot installed in VS Code and use it to scaffold a Java project in a GitHub repository.

---


#### **Visual Studio Code Insiders:**
In order to take advantage of the latest features of GitHub Copilot, we will be using **Visual Studio Code Insiders**. This is a separate version of Visual Studio Code that includes the latest features and updates. 

Visual Studio Code Insiders is a separate installation from the regular Visual Studio Code, so you can have both installed on your machine at the same time. 

It is updated daily with the latest features and bug fixes, so you can test out new features before they are released in the stable version of Visual Studio Code.

To install Visual Studio Code Insiders, go to the Visual Studio Code website and download the Insiders version for your operating system at the following link: https://code.visualstudio.com/insiders/

Once installed, open Visual Studio Code Insiders and sign in with your GitHub account.

---

### **Step-by-Step Instructions**

#### **1. Install Visual Studio Code Insiders (VS Code)**

- If not already installed, download and install **VS Code Insiders** from [here](https://code.visualstudio.com/insiders/).
- Follow the installation instructions for your operating system (Windows, macOS, or Linux).

#### **2. Redeem GitHub Pro Coupon (If Needed)**

If you don't already have GitHub Pro, you can redeem a coupon code:

1. Navigate to [github.com/redeem](https://github.com/redeem)
2. Look for the "Redeem a coupon" option
3. Enter your workshop coupon code: (will be provided)
4. Follow the prompts to complete the redemption process

**Note:** If you already have GitHub Pro, you can skip this step.

---

#### **3. Install the GitHub Copilot Extension for VS Code**
To install the GitHub Copilot extension in Visual Studio Code Insiders, follow these steps:
1. **Open VS Code Insiders**.
2. Go to the **Extensions** view by clicking on the Extensions icon in the Activity Bar on the side of the window (or press `Ctrl+Shift+X` on Windows/Linux, `Cmd+Shift+X` on macOS).
3. In the Extensions search bar, type "GitHub Copilot".
4. Find the **GitHub Copilot** extension by GitHub, and click **Install**.
5. Once installed, click **Sign in to GitHub** if prompted to authenticate GitHub Copilot with your GitHub account.
6. Follow the sign-in instructions in the pop-up browser window to authenticate with GitHub and authorize Copilot.

---

#### **3. work wth prompts - chat and edit**

Because we will working with the new edit feature of Copilot, let's back up our working copy of the spring-ai-azure-workshop repo:
  
Copy your local copy of spring-ai-azure-workshop and make a copy with a new name
Open the new copy in VS Code Insiders.

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
 

