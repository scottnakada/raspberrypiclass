# USB Camera Class
How to use a webcam
https://raspberrypi-guide.github.io/electronics/using-usb-webcams
Install OpenCV software
https://raspberrypi-guide.github.io/programming/install-opencv.html

# Install OpenCV software in a virtual environment
```buildoutcfg
# Create a virtual environment called venv
python3 -m venv venv
# start using the virtual environment
source venv/bin/activate
# Upgrade the version of the Python Package manager
pip install --upgrade pip
# Install the opencv library
https://github.com/opencv/opencv-python/issues/571

sudo apt update
pip install --upgrade pip setuptools wheel
CMAKE_ARGS="-DOPENCV_ENABLE_NONFREE=ON" pip install -v --no-binary=opencv-contrib-python opencv-contrib-python==4.5.3.56

```

