## License

This project is licensed under a custom **Academic Non-Commercial License (ANCL)**.

📌 Use is permitted for **academic and research purposes only**.  
🚫 **Commercial use is strictly prohibited** without prior written permission.  
© 2025 [Said Mousa Sajadi]

# English Assistant Form		 
This project is related to the implementation of the English Assistant Application, which helps us to learn English as an assistant. And, Also this package has the ability to translate from English to Persian.

<p align="center">
  <img src="https://github.com/yasharsajadi/EnglishAssistantForm/blob/master/Application_Tabs.png" width="800">
</p>

## Instruction

1. Install [Python](https://www.python.org/).


> ### ⚠ WARNING:
> After install EnglishAssistantForm, ```pip install EnglishAssistantForm```, Don't forget install *en_core_web_sm* data. ```pip install "https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-3.6.0/en_core_web_sm-3.6.0-py3-none-any.whl"```

2. Install [English Assistant Form](https://github.com/yasharsajadi/EnglishAssistantForm)

2. Install [English Assistant Core](https://github.com/yasharsajadi/EnglishAssistantCore) and [SpaCy-English Core Web Small (en_core_web_sm)](https://github.com/explosion/spacy-models/releases/)

    **Windows:**
    ```
    pip install EnglishAssistantForm & pip install "https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-3.6.0/en_core_web_sm-3.6.0-py3-none-any.whl"
    ```
    **Linux:**
    ```
    pip3 install EnglishAssistantForm && pip3 install https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-3.6.0/en_core_web_sm-3.6.0-py3-none-any.whl
    ```


## Usage
In the Python file(.pyw):
```
from EnglishAssistantForm.EnglishAssistantForm import App

if __name__ == "__main__":
	app = App()
	app.mainloop()
```
#### Or
In the Batch file(.bat):
```
@echo off

REM Check to Installed en_core_web_sm or not? 
::
set DATA_PACKAGE=en_core_web_sm
pip show %DATA_PACKAGE% >nul 2>&1

if %errorlevel% neq 0 (
    echo %DATA_PACKAGE% not installed. Installing...
	pip install "https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-3.6.0/en_core_web_sm-3.6.0-py3-none-any.whl"
) else (
	echo %DATA_PACKAGE% is already installed.
)
::

REM Check to Installed EnglishAssistantForm or not? 
::
set PACKAGE_NAME=EnglishAssistantForm
pip show %PACKAGE_NAME% >nul 2>&1

if %errorlevel% neq 0 (
    echo %PACKAGE_NAME% not installed. Installing...
	pip install %PACKAGE_NAME%
) else (
	echo %PACKAGE_NAME% is already installed.
)
::

REM Write a pyw file to Run Application. 
echo from EnglishAssistantForm.EnglishAssistantForm import App>> "%~dp0%EnglishAssistantApplication.pyw"
echo app = App()>> ""%~dp0%EnglishAssistantApplication.pyw"
echo app.mainloop()>> "%~dp0%EnglishAssistantApplication.pyw"

REM Run!!!
start pythonw "%~dp0%EnglishAssistantApplication.pyw"
timeout /T 1

REM Delete exectuer file
del /f "%~dp0%EnglishAssistantApplication.pyw"

REM Do you need pause to see the steps?
::pause
```




