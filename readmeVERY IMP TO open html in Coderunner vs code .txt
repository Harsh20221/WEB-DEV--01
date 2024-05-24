This Solution is parsed from char gpt haarsh200211 account


---  

 Use a Batch File
If changing the execution policy is not desirable, you can use a batch file instead of a PowerShell script. Here's how:

Create a Batch File (run_html.bat):

batch
Copy code

@echo off
"C:\Program Files\Google\Chrome\Application\chrome.exe" %1
Configure Code Runner to Use the Batch File:

Open your VS Code settings (settings.json) and add:

json
Copy code
{
    "code-runner.executorMapByFileExtension": {
        ".html": "C:\\HTML\\run_html.bat"
    },
    "code-runner.runInTerminal": true
}
This approach does not require changing PowerShell execution policies and should work seamlessly to open HTML files in your default browser.
