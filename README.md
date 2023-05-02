# Marielle's Token 

This solidity program is about effluvium token, when any transaction on Ethereum is executed, it takes effluvium according to the amount of computational power required to accomplish the transaction's actions.

# Description
The program is a simple contract written in Solidity, a programming language used to develop smart contracts on the Ethereum blockchain. This program serves as a quick and easy introduction to Solidity programming and can be used as a stepping stone for more complex projects in the future. 

# Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., m3.sol). Copy and paste the following code into the file:


```Solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;


contract MyToken {

    // public variables here
    string public tokenName = "Romana";
    string public tokenAbbrv = "Marielle";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```
After the coding that needs to be compiled, the Solidity Compiler will appear in the middle left part. "Please click". Click to show automatic compilation. ”

Once the code is compiled, you can deploy the contract by clicking the Deploy & Run Transactions tab in the left sidebar. Select the m3.sol contract from the dropdown menu and click the Deploy button.

Once the contract is deployed, go to your account and copy it. Then go to the contact provided before pasting. Please check the total inventory first. So after going to values ​​and entering the value you want, go to coins and paste the address or account you are copying and enter the value under it. Then check the total supply. After that, the value you put in the coin will be the same as the total supply.

# Authors
Marielle Romana 421000169@ntc.edu.ph

# License
This project is licensed under the MIT License - see the LICENSE.md file for details
