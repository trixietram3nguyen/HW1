# HW1 - COSC4370
Name: Trixie Tram Nguyen
PSID: 1518295

1. Objective: Rasterizer - derive and implement a similiar algorithm for rasterizing a circle. The final result will be 2 half of the circle in which the circle is x^2 + y^2 = R^2 where x >= 0 and positive integer R = 100 and the other half is y >= - and positive integer R = 150.
2. Environment: I run my code through Visual Studio Code using Linux base g++ (Ubuntu 9.3.0). Then I use Gimp to view my ppm result.
3. Project details: In order to get 2 different half of circle with different radius, I created 2 while loops in the "raterizeArc" function which one is for R = 100 and the other is for R = 150. Inside the "raterizeArc" function, I used Midpoint Algorithm to raterize the circle. I changed up the "renderPixel" function a little bit to help center the circle. I added the center, and radius variables to help get the center of each circle with different midpoint. For the circle with radius 100, it required to output the right half of the circle so I have image[center - (y - center)][x] and image[center - (x - center)][y] to get the correct midpoint. Also, the same for 150 but in this case, the required output is top half of the circle so I use image[x][center - (y - center)] and image[y][center - (x - center)] instead. Main function stay the same. After I got all my code down, I run g++ hw1.cpp and ./a.out 300 in unbuntu. I use 300 instead of 200 because the diameter of the big circle will be 300, if I use 200x200 then the canvas won't big enough for the output.
4. Result: Displayed half-top of the circle with radius of 150, and half right of the cirlce with radius of 100.
5. Reference: The pdf reading of from "Computer Graphics Principles and Practice - Foleyet. al", section 3.2 "Scan Converting Lines" and section 3.3 "Scan Converting
Circles". Also I got help from classmate to understand the algorithm and the use of it.
