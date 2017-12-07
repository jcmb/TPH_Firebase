#TPH_Firebase.py

## A tool for storing Temperature, Pressure and Humidity in a Firebase Database 

### Usage

>TPH_Firebase.py [-h] [-P PROJECT] [-N NAME] [-L LOCATION] [-R RATE]
>                       [-D DEVICE] [-S STATUS] [-T] [-v]

>optional arguments:

>-h, --help            show this help message and exit

>-P PROJECT, --Project PROJECT

>      Firebase Project ID (default: test-f72f0)

>-N NAME, --Name NAME 

>      Override Sensor Name (default: None)

>-L LOCATION, --Location LOCATION

>      Location Name (default: None)

>-R RATE, --Rate RATE  

>      Sensor Collection Rate (default: 58)

>-D DEVICE, --Device DEVICE

>      Sensor port (default: ttyACM0)

>-S STATUS, --Status STATUS

>      Status File name. File updated with readings each time  (default: None)

>-T, --Tell            

>      Report Arguments (default: False)

>-v, --Verbose         

>      increase output verbosity (default: None)

### Usage Details

* Project:

  The firebase project that the data will be reported into, at this time the project must be able to be written to without security.

* Name:

  The Sensor name that the data will be reported under. If the sensor name is not given as an argument then it will be read from the device and you should have set this before use. *This is very important if you have more than one sensor logging*

* Location:

  The location that the sensor is located at. This is for display and record keeping later.
  
* Rate:

   The rate that the data should be sampled from the sensor. The sample takes 1-2 seconds so for updates of once a minute use 58 seconds.
   
* Device:

   The device name that the sensor reports as. ttyACM0 is the default and is normally the correct value
   
* Status:

   Report the most recent measurements to a local file
   
* Tell:

   Report the arguments that are in use   
  
  

## Requirements

python-firebase 

>*sudo pip install python-firebase*
  
get\_pa\_linux, which must be install in /usr/local/bin

[Download from GitHub](https://github.com/DogRatIan/USB-Sensor-OpenSource)