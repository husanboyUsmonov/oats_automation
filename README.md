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
| Get Hourly Weather                | Keyword returns 12 hourly's forecast data | `robot --i hourly main.robot `| **None** |

