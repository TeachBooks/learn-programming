(llms-setup-guide)=
# Setting up the environment

LLMs can assist in various aspects of software development, but one of the most effective ways to integrate them into your programming experience is directly within your code editor. Tools like GitHub Copilot allow seamless access to AI-powered suggestions, reducing the need for copy-pasting and enabling the LLM to better understand the context of your entire project or file.

This notebook will guide you through different options for setting up your environment. The following options provide an integrated experience and allow you to access powerful models with your student account.  

## [Option 1, preferred, but GitHub account required] GitHub Copilot Set Up
GitHub Copilot is the industry standard for pair programming, and as a student, you can access it for free. You can request access to it by signing up for the [GitHub Student Developer Pack](https://education.github.com/pack). There is a detailed guide for [how to apply for GitHub Education as a student](https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-education-for-students/apply-to-github-education-as-a-student) which will grant you access to Copilot. Ensure you use your full student email (i.e. \<NetID>@student.tudelft.nl) and note that it may take a few days before your application is processed/ accepted. If you don't want to create a GitHub account (GitHub is part of Microsoft), please consider the other options). After you have access, proceed with the following steps:
* Download [VS Code](https://code.visualstudio.com/download) or any other supported IDE you prefer.
* Under the "Extensions" tab on the left in VS Code, install two extensions:
    * `GitHub Copilot` - this gives you code-generation features
    * `GitHub Copilot Chat` - this is an add-on to Copilot that gives you a ChatGPT-like chat feature that has access to your codebase.

```{admonition} Tip    
:class: tip    
Apply for GitHub Education as soon as possible, as it may take a few days for your application to be processed. Once you have access, you can start using GitHub Copilot in your IDE.
``` 

## [Option 2] Microsoft Copilot
With your student account, you've access to Microsoft Copilot: https://copilot.microsoft.com/. If you are using Microsoft Edge, you can sign in with your student account and use the built-in Copilot feature that is available in the sidebar. This allows you to interact with an LLM directly in your browser, and while it does not provide direct code generation capabilities like GitHub Copilot, it can still be useful for asking questions and getting explanations about code. To access it, simply open Microsoft Edge and look for the Copilot icon in the top right corner.


## [Option 3] Google Colab with Gemini
If you are using [Google Colab](https://colab.research.google.com/) to access their GPUs, you can use the built-in [Gemini](https://ai.google.dev/) chat feature. While this does not come with code generation directly, it serves as an integrated ChatGPT-like interface that can be extremely useful. There is no additional setup here, simply click on the "Gemini" button in the top right and it will open the chat feature. A google account is required for this service.

## [Bonus Option] Cursor Editor Set Up
If you are provided with API keys to advanced models such as the ones provided by OpenAPIT, Cursor is a fork of VS Code that allows full integration with LLMs within the editor like GitHub Copilot and allows using private API keys. To help you set up your environment, we prepared [this video tutorial on setting up and getting started with the Cursor Editor](https://youtu.be/PjFaeqnCgLs) from the DSAIE course. Alternatively, follow the instructions below. Only use this option if API keys are provided.
* Download and install Cursor from the [website](https://www.cursor.com/)
* In Cursor, in the top left tabs select File > Preferences > Cursor Settings. Now on the left vertical tab select Models, scroll down to OpenAI API Key, and paste your API key.
* Download this notebook and open it in Cursor.

Some helpful quick links for Cursor:
* [Documentation](https://docs.cursor.com/chat/overview)
* [Feature List](https://www.cursor.com/features)
* [Migrating from VS Code](https://docs.cursor.com/get-started/migrate-from-vscode)
