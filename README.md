# Whatsapp Automation Using Selenium

The code within this repository is tailored for sending messages to multiple contacts in a repetitive manner, utilizing Selenium and the Chrome WebDriver. There are just two constraints to consider:
1. Upon the initial run, you'll be required to scan the WhatsApp Web QR code.
2. The contact names must precisely match the saved names on your phone, including letter case sensitivity.

This code will run perfectly in MacOS. If you're using Windows or Linux, make sure to change the webdriver path accordingly.

## Install

<b>Install Selenium:</b> Begin by installing the Selenium Python package. You can do this using pip, the Python package manager:
```bash
pip install selenium
```
<b>Download WebDriver:</b> You'll need to download the WebDriver executable for the specific web browser you intend to automate (e.g., Chrome WebDriver, Firefox GeckoDriver, Microsoft Edge WebDriver). Ensure you download the correct version that matches your browser's version. In the provided code example, I've utilized Chrome WebDriver as an illustration, but you have the flexibility to select any WebDriver based on your personal preference.
Here's how to install the Chrome WebDriver as an example:
```bash
brew install chromedriver
```
This command installs the Chrome WebDriver using Homebrew. Replace chromedriver with the name of the specific web driver you want to install (e.g., geckodriver for Firefox or msedgedriver for Microsoft Edge).
Make sure you have Homebrew installed on your macOS system before using the brew command. If you haven't installed Homebrew yet, you can find installation instructions on the Homebrew website: https://brew.sh/.

<b>WebDriver Configuration:</b> After downloading WebDriver, specify its location in your Selenium script. You can set the path to the WebDriver executable like this (Python example):
```python
from selenium import webdriver
driver = webdriver.Chrome(executable_path='/path/to/chromedriver')
```
You have the option to simplify the process by relocating your WebDriver file to the `/usr/local/bin/` directory. This eliminates the need to specify the path every time you use it, as I have done in my code. In order to do so, you've to run the following command in your terminal.
```bash
sudo mv <path to chromedriver>  /usr/local/bin/
```
p.s. you don't have to add the `<` or`>` in your bash command.

## Simple Demo

Execute the code provided in the `main.py` file from this repository. When you run it, a new Chrome window will open. You'll need to manually scan the WhatsApp QR code using your phone. Afterward, follow the prompts displayed in the code output section, and you can send messages to multiple contacts as many times as you specify. Ensure that you keep both the Chrome window and the Python script running until the code execution is complete.
