# PlaywrightTest with GitHub Copilot Agent Mode

This repository demonstrates how to use GitHub Copilot in agent mode to iteratively build a Playwright-based browser automation project in C#.

## Prerequisites
- .NET 9 SDK
- PowerShell 7 (pwsh) installed
  - To install PowerShell 7, run the following command in an elevated (Administrator) PowerShell window:```powershell
winget install --id Microsoft.Powershell --source winget```
	- GitHub Copilot agent mode enabled in your IDE (see instructions below)

## Enabling GitHub Copilot Agent Mode
1. Make sure you have the latest version of Visual Studio or VS Code.
2. Install the GitHub Copilot extension.
3. Enable "Copilot Agent Mode" in your IDE settings or extension options.
4. Sign in with your GitHub account and ensure you have access to Copilot agent features.

## Feeding Prompts to Copilot Agent Mode
Feed the following prompts to Copilot agent mode, one at a time and in order:

### Prompt 1
Add Playwright and generate code to open the browser and navigate to www.clearmeasure.com and test all available hyperlinks by clicking on them.

### Prompt 2
When clicking on a link, have the code wait until the page has loaded before looking for additional links. Then click on the next link.  make the program recursive.

### Prompt 3
Now make it run against all available browsers, not just Chromium, and do it in parallel (multiple browsers executing in parallel)

## What Happens
- The agent will add the Playwright package, generate the required C# code, and update it as you provide each prompt.
- The final result will be a C# console app that recursively tests all hyperlinks on www.clearmeasure.com in parallel across Chromium, Firefox, and WebKit browsers.

## Running the Project
1. Restore dependencies:dotnet restore
2. Run the project:dotnet run --project PlaywrightTest/PlaywrightTest.csproj
---

For more information on GitHub Copilot agent mode, see the [official documentation](https://docs.github.com/en/copilot).
