# Electricity-Bill-Generation-using-C-Language
A C program to Generate Electricity bill (Replica of Karnataka state electricity Bill) Based on the Standards Provided by CESC (KPTCL) ,2022.

The entire C file is divided into 3 parts:
1. Preprocessor directive.
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
Both of them should be less than 31 Characters.

## Connection details 
The connection details further classified into **tariff** and **sanction load**. Both of them are treated as constant for the particular position and taken directly from the original electricity bill.
	
## Consumption details
The connection details is further classified into four factors namely:
- Previous meter reading 
- Present meter reading 
- Consumption in units and 
- Power factor.

The previous meter reading and present meter reading will be taken as input by the user and the difference between these two readings gives the consumption in units. Power factor is kept constant which is equal to 1.
It should be noted that present meter reading should always be greater than that of previous meter reading.

## Fixed charges
The fixed charges depends on the units consumed by the customer. If the units consumed is less than 50 then Rs 85 is considered as Fixed charge and if the units consumed is 50 or more then Rs 100 is taken as Fixed Charge. it should be noted that even if the units consumed is 0, the fixed charges will be applied.

## Energy charges
The Information of Energy charges will be explained by the below table:
| Units Consumed             | Fixed rate in Rs |
| -------------------------- | ------------- |
| For first 50 units. (0-50) | 4.10 |
| For Next 50 units. (51-100) | 5.55 |
| For next 100 units. (101-200) | 7.10  |
| For Next further consumed units. (201-∞) | 8.15  |

Let us understand it with an example. let the units consumed is 350. The entire units is divided into 4 parts as mentioned in the table.
- First - 50*4.10 = 205
- Second - 50*5.55 = 277.5
- Thirdly - 100*7.1 = 710
- Fourthly - 150*8.15 = 1222.5
- Total Energy charges = 205+277.5+710+1222.5 = 2415

if the amount of units consumed is 125, then it is divided into 3 parts.
- First - 50*4.10 = 205
- Second - 50*5.55 = 277.5
- Thirdly - 25*7.1 = 177.5
- Total Energy charges = 205+277.5+177.5 = 660

## FAC charges 
FAC Charge is calculated as the product of Number of units consumed and the constant 0.19.
if total units consumed is 350 units then FAC charge will be:
- FAC = 350*0.19 = 66.5

## Additional charges

The additional charges are further classified into 
- Solar rebate 
- Interest 
- Arrears 
- Tax 
- Bill amount and 
- Others

### Solar rebate
Solar utilization is an optional parameter which is asked to the user. If user select No For solar utilization then the solar utilization amount becomes 0 and nothing will be deducted from bill amount and if the user select yes for the solar utilization then a subsidy of 0.5 Rs per unit will be deducted from the bill amount to a maximum of 50 Rs per bill.

### Interest
Interest is applied only if the arrear is present. a Interest of 5% is applied on the Arrear amount.

### Arrear
It is the Amount needs to be paid in case of any left unpaid money from the previous bills. its input is taken by the user.

### Tax 
A tax of 5% is applied on the Bill Amount.

### Bill Amount 
It is the sum of Fixed charges, Total Energy charges and FAC charges.

### Others
It is an optional charges applied on specific cases only.

## The Total net amount
It is the total amount Required to be paid by the customer. it is given by the formula:
* Total Net Amount = (Bill Amount + Tax + Arrears(if any) + Interest(if any) ) - Solar Rebate 
