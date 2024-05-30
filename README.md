# solidityProject
This Solidity program is a simple program that demonstrates contract making in the Solidity programming language. The goal of this program is to provide a starting point for individuals who are new to Solidity and wish to understand how it works.

## Discription
This software is a simple contract built in Solidity, a programming language for creating smart contracts on the Ethereum blockchain. The contract contains a two functions mint and burn.Mint function uses addition assignment operators to increase the total supply and balance while burn function uses
a conditional statement "if" in which substraction assignment operator is performed to deduct the value from total supply and balance. This program provides a simple and uncomplicated introduction to Solidity programming that can be used as a foundation for more sophisticated projects in the future.

## Getting Started

### Program Execution
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension.Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here
    string public tokenName = "JASNOOR KAUR";
    string public tokenAbbrevation = "JKR";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => unit) public balance;

    // mint function
    function mint(address _address, uint _value) public{
        totalSupply += _value;
        balance[_address] += value;
    }

    // burn function
    function burn(address _address, uint _value) public{
        if(balance[_address]>=_value)
        totalSupply -= _value;
        balance[_address] -= _value;
    }
    
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the both functions. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" function. Then you can copy the address from account that's given by default above and paste in _address and give _value of your choice and then click on "transact" button.We can check our results by clicking on "totalSupply" button and can retrieve value we wrote.We can also fetch tokenName and tokenAbbrevation but clicking those two buttons.We can also check balance by putting the address we copied.For "burn" function we will again paste address to the "_address" button and write amount we want to burn.Finally we click on "transact" button and retreive the remaining value.
