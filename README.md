#installation 
to install the module you need to type:

pip install hand-tracker, or you can install the tar.gz file on the pypi website:

link for my project file:https://pypi.org/project/hand-tracker/

please paste the above link in your browser because there can be many modules of this name soo t can confuse between my and theirs module so please use this link.

by typing it You will be able to Install our Hand Tracking Module.

#How To Use The Module
To use the module You need to type:

from hand-tracker import*; By using this command You can use it in your projects.

#Making Of The Project
To make Your Project usong my hand-tracking module first of all you need to import, how to import is told above.

After that You Need To Always Paste This Code In Your Project First OtherWise It Will Not Work:

Code Is:

Please type : def main(): and after That write the below code or paste the below code.

     pTime = 0
     cTime = 0
     cap = cv2.VideoCapture(0)
     detector = handDetector()
     while True:
        success, img = cap.read()
        img = detector.findHands(img)
        lmList, bbox = detector.findPosition(img)
        if len(lmList) != 0:
            print(lmList[4])

        cTime = time.time()
        fps = 1 / (cTime - pTime)
        pTime = cTime

        cv2.putText(img, str(int(fps)), (10, 70), cv2.FONT_HERSHEY_PLAIN, 3,
        (255, 0, 255), 3)

        cv2.imshow("Image", img)
        cv2.waitKey(1)

#Thanks
Thank You Everyone to install my module have great projects ahead.

