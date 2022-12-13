Maximum number of files: 1
Type of work: Individual work
The circumference of an ellipse can be approximated by:



Calculate the circumference of an ellipse with the given radii a and b.



Input: a=16

          b = 11

Output:85.552

Solution
import math

a = int(input())
b = int(input())

def calculateP(a,b):
    per = round(math.pi * (3*(a+b) - math.sqrt((3*a + b) * (a + 3*b))),3)
    return per
print(calculateP(a,b))

Voltage difference
Maximum number of files: 1
Type of work: Individual work
The voltage difference Vab between points a and b in the Wheatstone bridge circuit is:



Calculate the voltage difference for the given V volts, R1 ohms, R2 ohms, R3 ohms, and R4 ohms.



Input: V=14

R1=120.6

R2=119.3

R3=121.2

R4=118.8

Output: 0.10793

solution
Vvolts = int(input())

r1 = float(input())
r2 = float(input())
r3 = float(input())
r4 = float(input())

voltageDifferenceVab = (((r1*r3-r2*r4))/((r1+r2)*(r3+r4)))*Vvolts

print(voltageDifferenceVab)

Resonant frequency
Maximum number of files: 1
Type of work: Individual work
The resonant frequency j(inHz) for the circuit shown is given by:



Calculate the resonant frequency for the given L henrys, R ohms when C = 2.6 x 10-6 farads.



Input: L=0.15

R=14

Output:
254.42

solution
import math

LHenrys = float(input())
ROhms = int(input())
C = 0.0000026

ResonantFrequency = round((1/(2*math.pi))*(math.sqrt((1/(LHenrys*C))-((ROhms/LHenrys)**2))),2)

print(ResonantFrequency)

Demand for Water
Maximum number of files: 1
Type of work: Individual work
The demand for water during a fire is often the most important factor in the design of distribution storage tanks and pumps. For communities with populations less than 200,000, the demand Q (in gallons/min) can be calculated by:

where P is the population in thousands. Set up a vector for P that starts at 10 and increments by 10 up to 100.

Use element-by-element computations to determine the demand Q for each population in P.  Round P to the nearest integer.

solution
import math

for pi in range(10, 101, 10):
    Q = round(1020*math.sqrt(pi)*(1-(0.01*math.sqrt(pi))))
    print(Q, end=" ")
    
    Limit Proof
Maximum number of files: 1
Type of work: Individual work
Show that 
Do this by first creating a vector x that has the elements 1.0, 0.5, 0.1, 0.01, 0.001, and 0.0001. Then, create a new vector y in which each element is determined from the elements of x by  Compare the elements of y with the value 4.
Output the vector y by rounding to nearest integer.

solution
import math

x = [0.11, 0.5, 0.1, 0.01, 0.001, 0.0001]

for i in x:
    #Output the vector y by rounding to nearest integer.
    vectorY  = round((math.cos(2*i)-1)/(math.cos(i)-1))
    print(vectorY, end =" ")
    
    Twin Primes
Maximum number of files: 1
Type of work: Individual work
A twin primes is a pair of prime numbers such that the difference between them is 2 (for example, 17 and 19). Write a computer program that finds all the twin primes between a and b, where a<b. The program displays the results in a two-column matrix in which each row is a twin prime.

Input1: 15
            35

Output1: 17 19
               29 31
               
               solution
               def is_prime(x):
   for i in range(2, x):
      if x % i == 0:
         return False
   return True

def generate_twins(start, end):
   for i in range(start, end):
      j = i + 2
      if(is_prime(i) and is_prime(j)):
         print("{:d} {:d}".format(i, j))
         
start = int(input())
end = int(input())
generate_twins(start, end)

Quadratic Equation
Maximum number of files: 1
Type of work: Individual work
Write a program in a script file that determines the real roots of a quadratic equation ax2 + bx + c = 0 . Name the file quadroots.m. When the file runs, it asks the user to enter the values of the constants a, b, and c. To calculate the roots of the equation the program calculates the discriminant D, given by: D = b2-4ac

If D > 0, the program displays message "The equation has two roots," and the roots are displayed in the next line in ascending order.

If D = 0, the program displays message "The equation has one root," and the root is displayed in the next line.

If D < 0, the program displays message "The equation has no real roots."

Note: Show roots in 4 digit precision.

solution
#Omurbek
import math

#When the file runs, it asks the user to enter the values of the constants a, b, and c. 
a = float(input())
b = float(input())
c = float(input())

#D, given by: D = b2-4ac
D = (b**2)-(4*a*c)

#If D > 0, the program displays message "The equation has two roots,"
if D>0:
    ans1 = (-b-(math.sqrt(D)))/(2*a)
    ans2 = (-b+(math.sqrt(D)))/(2*a)
    print("The equation has two roots,")
    print(round(ans2, 4))
    print(round(ans1, 4))
    
#If D = 0, the program displays message "The equation has one root,"    
elif D == 0:
    ans1 = (-b-(math.sqrt(D)))/(2*a)
    print("The equation has one root,")
    print(str(ans1)+ '000')

#If D < 0, the program displays message "The equation has no real roots."    
elif D<0:
    print("The equation has no real roots.")
else:
    print("Try again!!!.")
    
    Level of water in a water tower
Maximum number of files: 1
Type of work: Individual work
The tank in a water tower has the geometry shown in the figure (the lower part is a cylinder and the upper part is an inverted frustum of a cone). Inside the tank there is a float that indicates the level of the water. Write a python program that determines the volume of the water in the tank from the position (height h) of the float. The program asks the user to enter a value of h in m, and as output displays the volume of the water in m3.  



Input1:

Please enter the height of the float in meter 10

Output1:

The volume of the water is 4908.739 cubic meter.

Input2:

Please enter the height of the float in meter 20

Output2:

The volume of the water is 9847.519 cubic meter.

Input3:

Please enter the height of the float in meter 40

Output3:

ERROR. The height cannot be larger than 33 m.

Hint: Volume of a frustum of a cone

solution
import math

h = float(input())

if (h > 33):
    print("ERROR. The height cannot be larger than 33 m.")
    
elif h < 0:
    print("ERROR. The height cannot be a negative number.")
    
elif h <= 19:
    v = math.pi * 12.5**2 * h
    print("The volume of the water is ", round(v , 3),  " cubic meter.")
    
else:
    rh= 12.5 + 10.5 * (h-19) / 14
    v2 = math.pi * 12.5**2 * 19 + math.pi * (h-19) * (12.5**2 + 12.5 * rh + rh**2) / 3
    print("The volume of the water is ", round(v2 , 3),  " cubic meter.")
    
    Grade conversion and solution also
    #Grade conversion Omurbek
#Make a MATLAB program that asks the grade of exam result in percent(0-100) and then converts it into Alphabetic, Point and Traditional grades.
avgGrade = int(input())

if avgGrade>=95 and avgGrade<=100:
    print("A+ 4 Excellent")
    
elif avgGrade>=90 and avgGrade<=94:
    print("A 3.75 Excellent")
    
elif avgGrade>=85 and avgGrade<=89:
    print("A- 3.5 Excellent")
    
elif avgGrade>=80 and avgGrade<=84:
    print("B+ 3.25 Good")
    
elif avgGrade>=75 and avgGrade<=79:
    print("B- 3 Good")
    
elif avgGrade>=70 and avgGrade<=74:
    print("B- 2.75 Good")
    
elif avgGrade>=65 and avgGrade<=69:
    print("C+ 2.5 Satisfactory")
    
elif avgGrade>=60 and avgGrade<=64:
    print("C 2.25 Satisfactory")
    
elif avgGrade>=55 and avgGrade<=59:
    print("C- 2 Satisfactory")
    
elif avgGrade>=50 and avgGrade<=54:
    print("D 1.75 Satisfactory")
    
elif avgGrade>=0 and avgGrade<=49:
    print("F 0 Unsatisfactory")
    
else:
    print("Invalid mark")
    
    Number pi
Maximum number of files: 1
Type of work: Individual work
The value of  can be estimated by:



Write a program that determines the expression when n is entered from keyboard.

Input1: 1000

Output1: 3.1406

Input2: 3000

Output2: 3.1413

solution
r = int(input())

pi = 0

for i in range(r):
    pi += 4 * (1 - (i % 2) * 2) / (2 * i + 1)
print(round(pi, 4))

Smallest even integer...
Maximum number of files: 1
Type of work: Individual work
Write a program in a script file that finds the smallest even integer that is divisible by a and by b whose square root is greater than c. Use a loop in the program. The loop should start from 1 and stop when the number is found.

Sample Input: 3 
                       5
                       7

Sample Output: 60

solution
A = int(input())
B = int(input())
C = int(input())
x = 1001
for i in range(1, x):
    if i%A == 0 and i%B == 0 and i > C**2:
        print(i)
        break
print()
