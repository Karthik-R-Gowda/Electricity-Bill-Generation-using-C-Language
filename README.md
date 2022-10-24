# Electricty-Bill-Generation-using-C-Language
A C program to Generate Electricty bill (Replica of Karnataka state electricty Bill) Based on the Standards Provided by CESC (KPTCL) ,2022.

The entire C file is Divided into 3 parts:
1. Preprocessor directive
2. main function int as type.
3. User defined function called "elc_bill" with return type float.

The entire electricity bill is divided into 9 parts namely:
- Account details 
- Personal details 
- Connection details 
- Consumption details 
- Fixed charges 
- Energy charges 
- FAC charges 
- Additional charges and 
- The total net amount.

## Account details
It consists of 10 digit Account ID which will be taken by user as input.

## Personal details 
It consists of two strings namely **owners name** and **address** which will be taken as input by the user. 
Both of them should be less than 31 Charecters.

## Connection details 
The connection details further classified into **tariff** and **sanction load**. Both of them are treated as constant for the particular position and taken directly from the original electricity bill.
	
## Consumption details
The connection details is further classified into four factors namely:
- previous metre reading 
- present metre reading 
- consumption in units and 
- power factor.

The previous matter reading and present metre reading will be taken as input by the user and the difference between these two readings gives the consumption in units. Power factor is kept constant which is equal to 1.
It should be noted that present metre reading should always be greater than that of previous metre reading.

## Fixed charges
The fixed charges depends on the units consumed by the customes. If the units consumed is less than 50 then Rs 85 is concidered as Fixed charge and if the units consumed is 50 or more then Rs 100 is taken as Fixed Charge. it should be noted that even if the units consumed is 0, the fixed charges will be applied.

## Energy charges
The Information of Energy charges will be explained by the below table:
| Units Consumed             | Fixed rate |
| -------------------------- | ------------- |
| For first 50 Units.(0-50) | 4.10 |
| For Next 50 units.(51-100) | 5.55 |
| For next 100 units.(101-200) | 7.10  |
| For Next further consumed units  | 8.15  |



