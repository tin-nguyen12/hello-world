# Code Optimisation and Improvements
Below are the changes that was made to the program and system. The changes are split into two areas: general and specific. The general improvements include areas such as changing of variable names and the system prompt messages. It doesn't change the internal structure of the system, rather it is done to improve readability, making it maintainable, improving overall efficiency without altering the way it operates. The specific improvements includes fixes and additions to the program that will give it a different feel and the way it operates. 

## General Improvements
The general improvements included general class file commenting and the addition of Javadoc. This was done to help improved code legibility and to better understand the code, particularly during the debugging phase. Some system prompt messages were changed from what was originally had. They were changed to make it more understandable and make it more user-friendly. For example, originally when starting the cash register program, a message like below was displayed:
```java
Please enter cash register's float: 
```
To a common user, they wouldn't know what a float was therefore it was changed to:
```java
Please enter starting cash register balance:
```
Another change made was when the user was inputting the items in for transaction, the name wasn't displayed back to the user:
```java
Please enter the item's name: Coke
Please enter the item's cost: 10
 ```
This was changed to reflect that:
```java
Please enter the item's name: Coke
Please enter the Coke's cost: 10
 ```
 Along with this, there were other system prompt changes made to improve the quality of life of the system.


## Specific Improvements

### Dynamic Receipt Names and Transaction Number
The receipt class was modified to include the implementation of dynamic receipt names. Previously, every time a receipt was requested, the program would overwrite the existing file. With this change, the receipt file name will have a unique name (The date and time that the receipt was printed). A transaction number was also included in the receipt file. This is purely for aesthetics reasons as many receipts would keep track of the transaction number. 

### Allow User to Enter Quantity of Items
The user will now be given the option to specific the quantity of the items that is being processed. This change was made so that it'll be more convenient for the user to process the item instead of having to repeatedly enter the same item again. The number of items desired is also reflected in the receipt output. 

# Cash Register Manual  
The cash register software is a program that allows users to process transacation of various items such as groceries and other goods. It includes several important featues such as: an in-built loyalty program where customers can earn points for spending, multiple payment options, printing of receipts (if requested), and an automatically generated summary report of the transacations processed. The software also includes a secure authorisation systems where only authorised users can access the software. 



## Feature - Loyatly Program
The loyalty program is a feature implemented in the CashRegister program which allows customer to have a loyatly account. The amount of loyalty points that can be accrued depends on how much was spent. In this case, it is 1 point for every $10 spent. Points can then be used to redeem offers such as discounts. The program keeps track of the customers that are part of the loyalty program, their membership number, and their current balance. Users of the software will be given the choice to enter a membership number (to update their existing balance), create a new account, or simply skip if they wish.

### Usage

After the last item has been added to the checkout, a prompy will display with the following options underneath:

```java
Do you have a UniSA Loyatly Card?
> Y - Yes | C - Create | Enter - Skip
```
It will ask you to select between three options:
*  **(1) Y - Yes**
    * User will be prompted to enter in the **membership number**.
    * If the username exists, the loyalty points will be added and it will return back to the cash register program.
    * If the username does not exist, it will ask if the user would like to create an account (see below).
    
*  **(2) C - Create**
    * User will be prompted to enter in the customer's **name**.
    * The program will then create an account for that customer.
    * It will then automatically add the required loyatly points to the account and return back to the cash register program.

*  **(3) Enter - Skip**
    * Choosing this option will ignore the first two options and continue with the program

**Note:** Some dummy accounts (with balances) were created for the purpose of testing the loyalty program. Feel free to use them:
 * 000000
 * 000001
 * 000002
