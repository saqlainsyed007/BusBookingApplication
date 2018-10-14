# BusBookingApplication


This Application requires `Python3 and Pip3`


Python 3 can be downloaded from https://www.python.org/downloads/. If you are using python 3.4 or higher, pip3 is already installed. Otherwise download and install manually from https://pip.pypa.io/en/stable/installing/.


Use of virtual environment is recommended. Python 3 comes with built in mechanism to create virtualenv. The documentation can be found at https://docs.python.org/3/library/venv.html

### Steps to create Virtual Env

1. Create a master virtual env directory. This directory could be used to store all your virtual envs.

    `mkdir ~/my_virtual_envs`
    
2. Within your master virtual env directory, create a directory to store your project virtual env. This directory will contain your installations and the script to activate your virtualenv.

    `mkdir ~/my_virtual_envs/bus_booking`
    
3. Create virtual env

    `python3 -m venv bus_booking ENV_DIR ~/virtualenvs/bus_booking/`
    
    **Note** that `~/virtualenvs/bus_booking/` is the path to your project virtual env directory.
    
4. Activate virtual env

    `source ~/virtualenvs/bus_booking/bin/activate`


### Download Application

Please download this in a location other than you virtual envs directory

```
git clone https://github.com/saqlainsyed007/BusBookingApplication.git

cd BusBookingApplication/BusBooking/
```

### Install Application
```
pip3 install -r requirements.txt

python3 manage.py migrate

python3 manage.py runscript seed_data
```

Seed data creates dummy schedules from today to three days from today.


### Run Application
```
python3 manage.py runserver 0:8000
```

### View Application
Go to `http://localhost:8000/booking/` and search for some buses. A `DummyLocation` is added to view the empty results state.


Go to `http://localhost:8000/admin/` and login with username `admin` and password `changeme` to view all objects that have been created and validate results in the UI.


**Note**: 


Some features may not work in Internet Explorer and Microsoft Edge.

CDNs do not load sometimes. Please hard refresh untill all CDNs are loaded and there are no 403, 404 errors in the browser console
