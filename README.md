# Cyclotomic-polynomials
..are special formulas that help us find points on a circle where, if you go around enough times, you return to where you started.


#### cp.octave

```

Analysis of Distances Between Points on Unit Circle
================================================

n   Product         Theory (n^n/2)  Sum             Theory (asymp) 
-   -------         -------------   ---             -------------  
3   5.1962          5.1962          5.1962          6.2946         
4   16.0000         16.0000         9.6569          14.1207        
5   55.9017         55.9017         15.3884         25.6150        
6   216.0000        216.0000        22.3923         41.0641        
7   907.4927        907.4927        30.6690         60.7014        
8   4096.0000       4096.0000       40.2187         84.7241        
9   19683.0000      19683.0000      51.0415         113.3025       
10  100000.0000     100000.0000     63.1375         146.5871       

```

![image](https://github.com/user-attachments/assets/cad302f7-83d8-41b7-8800-cda86121da23)

#### cp.mint

1. Main Organization:
- Uses capital letters A-Z for functions
- Variables a-z store values and array pointers
- Uses APU-like commands (FSIN, FCOS, etc.) for floating point math
- Arrays store points and distances
- All FP results go into variables, never on stack
- Stack only used for 16-bit integers

2. Key Functions:
- I: Initializes constants (pi, two, two_pi)
- A: Creates arrays for x-coords, y-coords, distances
- B: Calculates point positions on circle
- D: Calculates distance between two points
- L: Computes all distances between points
- M: Multiplies all distances together 
- U: Sums all distances
- T: Calculates theoretical values
- R: Prints results for one n
- Y: Original output routine
- Z: Table formatted output

3. Program Flow:
1. Initialize constants and arrays (I and A)
2. For each n (3 to 10):
   - Calculate n points on circle (B)
   - Find all distances between points (L)
   - Calculate product of distances (M)
   - Calculate sum of distances (U)
   - Calculate theoretical values (T)
   - Display results (either Y or Z format)

4. Key Calculations:
- Points: Uses sin/cos to place points evenly on circle
- Distances: Uses Pythagorean theorem between points
- Products: Multiplies all distances together
- Sums: Adds all distances
- Theory: Calculates n^(n/2) and 2n²ln(n)/π

5. Arrays Used:
- x array: x-coordinates
- y array: y-coordinates
- d array: distances between points

6. Memory Usage:
- All values stored in variables
- Temporary calculations use spare variables
- Arrays sized for max 10 points
- Distance array sized for 45 distances (max needed)

7. Mathematical Properties Shown:
- Product equals n^(n/2)
- Sum approaches 2n²ln(n)/π
- All distances are unit circle based

#### cp_am9511.mint3




