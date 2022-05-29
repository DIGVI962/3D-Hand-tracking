# 3D-Hand-tracking

The main file takes in input from webcam and performs all the methods, it and identifies and labels the key points of the hand. After all the key point positions are recorded in a list containing id, x-coordinate and y-coordinate. It is then transferred to unity engine through a socket plug-in at server port 5052.

The HandTracking c# file contains the code pretaining to taking the x & y coordinates from the list and mapping it to the 21 different sphere objects which make up half the caricrature of hand that appears in the unity gameplay. It gets data from the UDPReceive file uploaded in unity, some methods are performed on the data and then run through a loop to get the coordinates which are then entered in the local position element in the Transform component.

The lineCode c# file contains the code which joins the line assets to the different points on hand completing the Hand object. In this the position of points is used as origin and end points.

The UDPReceive file is a c# file that encodes the data from the socket plug-in and sends it to unity.
