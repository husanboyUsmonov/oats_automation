 ## Description
This file includes Documentation, Installtion and Debugging tips for weatherdotcom library.

### Prerequisites
[Robot Framework](https://robotframework.org/) is implemented using [Python](https://www.python.org/), and a precondition to install it is having Python or its alternative implementation [PyPy](https://www.pypy.org/) installed. Another recommended precondition is having the [pip](https://pip.pypa.io/en/stable/) package manager available.
Robot Framework requires Python 3.6 or newer.

## Installation
In order to install all dependencies you have to create virtualevironment first.

Install venv
```
pip3 install virtualenv
python3 -m venv venv_name
```
Actvate venv in Windows Shell
```
venv/Scripts/activate.ps1
```
Actvate venv in Mac terminal
```
source venv/bin/activate
```
#Install dependencies from requirements.txt
```
pip3 install -r requirements.txt
```
or install from distrubuted wheel package
```
cd dist
pip3 install WeatherDotLibrary-0.1.tar.gz
```
## Running main Robot files

In order to run all Suites located in main.robot file
```
cd Tests
robot main.robot
```
to run with tags
```
robot --i <tag_name> main.robot
```
to run locating all results to Results folder
```
robot -d cd ../Results main.robot
```
## Robot Keywords

| Name                      | Description                                                                                                                                                                                                                                                                                                              | Example                                                                                                                                            | Arg                                 |
|:-------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------|
| Get Today Weather                 | Keyword returns today's forecast data | `robot --i today main.robot ` | **None** |
| Get Hourly Weather                | Keyword returns 12 hourly's forecast data | `robot --i hourly main.robot `| **None** |
| Get Hourly Weather                | Keyword returns 12 hourly's forecast data | `robot --i hourly main.robot `| **None**|
| Get 10 Day Weather                | Keyword returns 10 day's forecast data | `robot --i 10days main.robot `| **None**|
| Get Monthly Weather               | Keyword returns monthly forecast data | `robot --i monthly main.robot ` | **None** |
| Get Weekend Weather               | Keyword returns weekendly forecast data | `robot --i weekend main.robot `| **None** |
| Get Radar View                    | Keyword returns output as png and saves to Result folder | `robot --i radar main.robot `| **None** |
| Get Latest Weather News           | Keyword returns number of recent news given as param | `robot --i news main.robot `| **amount** |
| Translate String Keywod Example   | It is just a example keyword in order illustrate how we can use addition python keyword in any other robot keywords or Suites | `robot --i tr-example main.robot `| **from,  to, text** |

## Python Keywords
| Name                      | Description                                                                                                                                                                                                                                                                                                              | Example                                                                                                                                            | Arg                                 |
|:-------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------|
| translate_messages                | Extra python keyword to translate any string to any lanugages | Can be called both as py and robot | **from_lan, to_lang, text** |

## Support Keywords for Robot suites
| Name                      | Description                                                                                                                                                                                                                                                                                                              | Example                                                                                                                                            | Arg                                 |
|:-------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------|
| add_strings_to_list                | Extra python keyword to cast 2 strings to list so we can use during robot | Can be called both as py and robot | **str1, str2** |
| get_current_datetime                | Extra python keyword to return current time in a spesefic format | Can be called both as py and robot | **None** |

## Unittest for WeatherDotLibrary
```
cd Library
pytest -m test_library
```
## Checking python code quality
```
pylint ../Library WeatherDotLibrary.py
```
## Checking robot code quality
```
robocop ../Tests main.robot
```
## Debugging
If you are encountering some problems with main.robot files first try:
```
cd Test
robot --dryrun main.robot
```
check mistakes accordingl by installing all robor requirements
If you still have problems with running robot or python files try:
```
pip3 install -r requirements.txt
or
pip install -r requirements.txt
```
Screenshoots
