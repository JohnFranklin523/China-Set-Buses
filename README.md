# China-Set-Buses
 The Bus sector of the China Set of OpenTTD.
 Compilation needs NML 0.7.5

## Formulae of comfort and purchase/running costs
### Comfort (cargo age period):

 c = (3KEL/r)(|a-1950|-|a-2025|+275)

 Round to an integer.

 Where: 

 K - 1 if air conditioner is existent, 0 otherwise; 

 E - 1 if the bus is electric vehicle, 0 otherwise;

 L - Luxury index, ranging from (inclusive) 1 to 1.5;

 r - Seats in a row, 6 for city buses with large standing spaces, and 5 for 2+2-style buses with standing spaces;

 a - the introduction year of the bus.


### Purchase cost factor:

 f1 = m+10g+v/2+P/5+R-20

 Round to an integer, or 1 if the result less than 1.

 Where:

 m - the mass (weight) of the vehicle (t);

 g - tractive effort coefficient;

 v - maximum speed of the vehicle (km/h);

 P - power of the vehicle (kW);

 R - reliability decay speed.


### Running cost factor:

 f2 = v + P/2 + sqrt(nc/185)

 Round to an integer, or 1 if the result less than 1.

 Where:

 v - maximum speed (km/h);

 P - power (kW);

 n - passenger capacity;

 c - cargo age period (comfort).