# Image-Capture_BGRtoGRAY
Image Capture and BGR to GRAY Using OpenCV
"""
Created on Fri Sep  8 20:01:56 2017

@author: kiran
"""
import numpy as np
import cv2

cap = cv2.VideoCapture(0)

while(True):
    # Capture frame-by-frame
    ret, frame = cap.read()

    # Our operations on the frame come here
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

    # Display the resulting frame
    cv2.imshow('frame',gray)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# When everything done, release the capture
cap.release()
cv2.destroyAllWindows()
cap.get(3)
ret = cap.set(3,320) 
