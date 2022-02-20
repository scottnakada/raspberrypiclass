# USB Camera Class
## Install OpenCV software
https://www.circuitbasics.com/introduction-to-computer-vision-using-opencv-and-raspberry-pi/

## How to use a webcam
https://raspberrypi-guide.github.io/electronics/using-usb-webcams

sudo apt install fswebcam
fswebcam -r 1280x720 --no-banner ./mypic.jpg
v4l2-ctl --list-formats-ext
sudo apt install ffmpeg
ffmpeg -f v4l2 -video_size 1280x720 -i /dev/video0 -frames 1 ./image2.jpg

### Access your webcam with a python program
Use your editor to create this file: read_image_usb_camera.py
```commandline
import cv2

cam = cv2.VideoCapture(0)

while True:
	ret, image = cam.read()
	cv2.imshow('Imagetest',image)
	k = cv2.waitKey(1)
	if k != -1:
		break
cv2.imwrite('/home/pi/testimage.jpg', image)
cam.release()
cv2.destroyAllWindows()
```