# Project-3-DeFiBank-Solidity-Files

DeFiBankAccountModel documentation & direction for button operation

This instance of LoanModel functions as a standard contract between the Bank and patron.
Memory: Data will only be stored during the execution of the function.
Storage: the data will persist even after the function executes.
Favorite Number will start off as zero.
Deploy
addPerson: “Patrick”, 2
Click addPerson button.
In the “people” button, put 0, then click the button and you should get
0: uint256: accountNumber 2
1: string: name Patrick
This means at the 0th index in this people array, we’ll get string Patrick.
The next person that you put in will be at “people” button, 1.  Remember to add and click the people button before you put in 1 and click “people”.
nameToAccount button - put in “Becca”, click the button, and you’ll see what her account number pops up as.
Connect to InjectedWeb3 to run test transactions on your test ethereum account.
Redeploy the contract, hit confirm on the metamask pop up, and you will see the contract pop up on the ganache webpage.
Let’s say that you put 123 in the store button, meta mask will pop up and the transaction will appear to store the information, and the retrieve function will show 123.  In this sense, ‘store’ and ‘retrieve’ are linked to each other and later used for inheritance for the DeFiBankStorageFactory.sol file, where as ‘addPerson’, ‘nameToAccountNumber’, ‘accountNumber’, and ‘people’ are buttons that interact with each other. 
The below images show the creation of the contract and its history on the ganache block chain. 

![image](https://user-images.githubusercontent.com/90321433/156669926-5d5d22c5-931f-4c49-899a-b65192cab67d.png)


DeFiBankStorageFactory documentation & direction for button operation

Create LoanModel Contract by hitting the createLoanModel contract button.  By doing this, I create a new transaction that’s going to create a new Loan Model contract and push it onto our StorageFactory array.
If you were to put 0 in the loanModelArray, you’d get the address for the newly created contract on the array.

![image](https://user-images.githubusercontent.com/90321433/156670099-7532910e-8c1d-4197-8e07-bdc7badd305a.png)

For the sfStore button, first create the contract, and then on the sfStore button enter in 0.  0 is the array that the contract from LoanModel exists on.
On loanModelArray, enter 0, click the button, and the account number from LoanModel will pop up.
On sfGet, enter 0, click the button, and you will get a return of how many contracts exist on that array.
The following screenshot displays this information:

![image](https://user-images.githubusercontent.com/90321433/156670245-474cd715-5d20-47d6-9f0c-acb5eaeca94c.png)

Looking at inheritance.  StorageFactory now has all the buttons that Loan Model has in addition to the original buttons Storage Factory possessed:

![image](https://user-images.githubusercontent.com/90321433/156671316-ac4df6d9-f046-492d-a58e-839b2f468a82.png)

Keep in mind that StorageFactory is keeping record of the instances on LoanModel, so if you work and deploy on LoanModel, it will be seen in StorageFactory.  For this demo of inheritance, we have one contract deployed on the 0 Array for LoanModel as is seen on StorageFactory.


DeFiBankLoanContract documentation & direction for button operation

This instance of a loan model works as a classic loan contract between the Bank and patron.
Before, we haven’t been working with value, with this demo we will be working with wei.
Let’s first work with the ‘fund’ button.  Deploy the contract, enter in 1000000000 wei, enter in the address of the account the money will be given to, and click ‘addressToAmountGiven’, and you’ll see this transaction happen:

![image](https://user-images.githubusercontent.com/90321433/156671425-ed1c5e59-7b0b-47fb-8464-ab52dc295ba5.png)

![image](https://user-images.githubusercontent.com/90321433/156671509-a1194f97-8cde-4dbf-b16d-a9e6259a74a2.png)

![image](https://user-images.githubusercontent.com/90321433/156671537-97844417-7963-4a66-a737-a32fb9470b65.png)

 Because Tether is the equivalent of the US Dollar, if you see 1 Dollar, then it’s 1 Tether.If we want to check the current value of Tether, we can simply click the button and it will return the value:
 
 ![image](https://user-images.githubusercontent.com/90321433/156671594-fddd7346-45d3-493d-8e81-1cd20bfcdfd4.png)

On a technical note, people can come in and subscribe to a contract for the purpose of potentially purchasing the loan from the bank in the future.  This is accomplished with this code here:

![image](https://user-images.githubusercontent.com/90321433/156671630-7c22c133-14c0-4326-ba9e-4044d97ebc24.png)

And people subscribed to the contract will be (for example) able to see the following transaction history:

![image](https://user-images.githubusercontent.com/90321433/156671660-72801d7b-ec10-499d-8a5b-f51e673e7f81.png)






