# TensorWork

Check if your Python environment is already configured:

#Requires Python 3.4, 3.5, or 3.6
*python3 --version
*pip3 --version
*virtualenv --version
*If these packages are already installed, skip to the next step.
*Otherwise, install Python, the pip package manager, and Virtualenv:

#WINDOWS
*Install the Microsoft Visual C++ 2015 Redistributable Update 3. This comes with Visual Studio 2015 but can be installed separately:

*Go to the Visual Studio downloads,
*Select Redistributables and Build Tools,
*Download and install the Microsoft Visual C++ 2015 Redistributable Update 3.
*Install the 64-bit Python 3 release for Windows (select pip as an optional feature).

`pip3 install -U pip virtualenv`
#2. Create a virtual environment (recommended)
*Python virtual environments are used to isolate package installation from the system.

`UBUNTU / MAC OSWINDOWSCONDA`
*Create a new virtual environment by choosing a Python interpreter and making a ./venv directory to hold it:

`virtualenv --system-site-packages -p python3 ./venv`
#Activate the virtual environment:

`.\venv\Scripts\activate`
#Install packages within a virtual environment without affecting the host system setup. Start by upgrading pip:

`pip install --upgrade pip`

`pip list`  # show packages installed within the virtual environment
#And to exit virtualenv later:

`deactivate`  # don't exit until you're done using TensorFlow
#3. Install the TensorFlow pip package
#Choose one of the following TensorFlow packages to install from PyPI:

*tensorflow —Current release for CPU-only (recommended for beginners)
*tensorflow-gpu —Current release with GPU support (Ubuntu and Windows)
*tf-nightly —Nightly build for CPU-only (unstable)
*tf-nightly-gpu —Nightly build with GPU support (unstable, Ubuntu and Windows)
#Package dependencies are automatically installed. These are listed in the setup.py file under REQUIRED_PACKAGES.
*VIRTUALENV INSTALLSYSTEM INSTALL
`pip install --upgrade tensorflow`
#Verify the install:

`python -c "import tensorflow as tf; print(tf.__version__)"`