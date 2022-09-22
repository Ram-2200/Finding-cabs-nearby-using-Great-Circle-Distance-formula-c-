# Finding-cabs-nearby-using-Great-Circle-Distance-formula-C++ 

Given GPS co-ordinates(in degrees) of a person who needs a cab and co-ordinates of all the cabs in the city stored in a text file in JSON format, find the user-id and name of all the cab drivers available in 50 km proximity.

**Instruction to run the program**
 ============= 
* Compile the code using cmd: g++ main.cpp.

* After successful compilation, run it along with passing the file name customers.json using cmd: ./a.out ./customers.json

* A new file named result.json will be created on the same directory where the code and customers.json file is existing.

Approach Used
==============

* Obtain latitude and longitude of each cab in string format along with their user-id and name from the JSON encoded input file.

* Convert latitude and longitude of the cab present in string format to double.

* Convert latitude and longitude of both, the user and the cab present in degrees to radians.

* Calculate distance between the user’s location and the cab using Great Circle Distance formula.

* If distance is found to be less than or equal to 50 kms then output the user- id and name of the cab driver to a new file else take no action.


Great-circle distance
===========
* It is the shortest distance between two points on the surface of a sphere, measured along the surface of the sphere (as opposed to a straight line through the sphere's interior). The distance between two points in Euclidean space is the length of a straight line between them, but on the sphere there are no straight lines. In spaces with curvature, straight lines are replaced by geodesics. Geodesics on the sphere are circles on the sphere whose centers coincide with the center of the sphere, and are called 'great circles'.

**Formulae**

![image](https://user-images.githubusercontent.com/85600318/191788842-b4a01f8f-87ba-45f1-a4cf-1c776f3161c2.png)

The largest circle that can be drawn on the sphere surface is the great circle. The shortest distance between any two points on the sphere surface is the Great Circle distance. Historically, the Great circle is also called as an Orthodrome or Romanian Circle.

The diameter of any sphere coincides with the diameter of the great circle. The great circle is used in the navigation of ship or aircraft. The idea that is the Earth is somewhat spherical helps in navigating as we come to know for the shortest distance in the sphere.
Great circle formula is given by,
![image](https://user-images.githubusercontent.com/85600318/191789820-360f27d2-e6ad-42be-a40c-e91ae8a29148.png)

The problem is normally expressed in terms of finding the central angle {\displaystyle \Delta \sigma }\Delta \sigma . Given this angle in radians, the actual arc length d on a sphere of radius r can be trivially computed as

![image](https://user-images.githubusercontent.com/85600318/191790285-90c3c8ae-5cb2-49d5-ae8e-83f4c32e91a0.png)

Where,
r is the radius of the earth/sphere/circle

σ  is the latitude
∆ is the longitude
