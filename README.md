# Electricty-Bill-Generation-using-C-Language
A C program to Generate Electricty bill (Replica of Karnataka state electricty Bill) Based on the Standards Provided by CESC (KPTCL) ,2022.

The entire C file is Divided into 3 parts:
1.Preprocessor directive
2.main function int int as type.
3.user defined function called "elc_bill" with return type float.

At first the input for the owners name and owners address will be taken by the user along with the 10 digit account ID with the help of scannef  function.
Then the information about the previous metre reading and current metre reading will be taken by the user himself using scanf function if the user is unaware of the previous metre reading zero will be taken as input and if the user is an aware of the present metre  then the number of units consumed will be taken as input.
If the previous metre reading is more than that of the present material reading the program will be stopped from executing because both of them cannot be equal and also not the vice versa.
The difference between the previous metre reading and present meta reading gives the amount of units consumed by the user.
The entire electricity bill is divided into 9 parts namely account details personal details connection details consumption details fixed charges energy charges FAC charges additional charges and the total net amount.
The information about the account details and personal details will be taken by the user and printed on the electricity bill as it is
 the connection details are taken as standards from the original electricity bill and are printed as it is.
The consumption details are divided into further parts namely present reading previous reading consumption and power factor the present reading and previous reading will be taken by the user whereas the consumption is the difference between the present and the previous reading the power factor which is constant is taken as 1.
If the amount of units consumed by the customer is less than 50 then fix it charges will be taken as 85 rupee. And if the units consume is 50 or more the fixed charges will be taken as 100 rupees
