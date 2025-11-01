Installation on Ubuntu
========

Installation of DragonLog while using the Ubuntu system libraries.

Requirements
-----
Install required packages

    apt install python3-pyqt6 qt6-tools-dev-tools python3-openpyxl python3-setuptools python3-requests python3-xmltodict python3-keyring python3-matplotlib python3-numpy python3-flake8 python3-packaging python3-opencv python3-pyzbar python3-xmlschema python3-pip python3-venv pipenv qt6-tools-dev-tools

Install virtual environment
-------
    cd DragonLog
    virtualenv --system-site-packages .venv
    source .venv/bin/activate
    make ubuntu
    ./run.sh