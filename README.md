# Utility to update android device's location

This uses android [ADB's](https://developer.android.com/studio/command-line/adb?hl=es-419) command `geo fix` to change the device's location. 

## Requirements
1. [python 2.7](https://www.python.org/downloads/release/python-2715/)
2. [virtualenv](https://virtualenv.pypa.io/en/latest/)

## Usage

Note: To work, this needs a connected device or a emulated virtual device running

1. `git clone git@github.com:SergioRosello/mockgeofix.git`
2. In project root directory: `source ENV/bin/activate`
3. In project root directory: `pip install -r requirements.txt`
4. In project root directory: `python run_sim.py -i targetIP -g path/to/gpx/file.gpx -t emulatorConsoleAuthToken`

## `run_sym.py`'s parameters

Below is a list of parameters used by `run\_sym.py` script.

### Required parameters

* `-i` or `--ip`: The ip address where it will find the device
* `-g` or `--gpx-file`: The `.gpx` file used to trace the route
* `-t` or `--auth`: Auth token for telnet authentication

### Not required parameters

* `-p` or `-port`: The port used to connect. Default value: 5554
* `-S` or `--sleep`: Sleep between track points. Default value: 0.5
* `-s` or `--speed`: Speed in km/h (Takes precedence over -S)
* `-I` or `--listen-ip`: Run a HTTP server visualizing mocked locations on this ip
* `-P` or `--listen-port`: HTTP server's port. Default value: 80
