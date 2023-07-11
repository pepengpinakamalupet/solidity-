# Project Title

This assessment demonstrates the basic minting and burning of an NFT token. The goal of this program is to give individuals who are unfamiliar with Solidity a place to start learning about it.

## Description

Solidity, a programming language used to create smart contracts for the Ethereum blockchain, was used to create this straightforward contract. This software acts as an easy-to-understand primer on programming in Solidity and can be used as a springboard for more difficult projects in the future.

## Getting Started

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., leb.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT

pragma solidity 0.8.18;

contract LebToken {

// public variables here
    string public name = "LEVI";
    string public abbrv = "LV";
    uint public supply = 0;
// mapping variable here
    mapping(address => uint) public blnc;
// mint function
    function mint(address add, uint val) public {
    supply += val;
    blnc[add] += val;
    }
// burn function
    function burn(address add, uint val) public {
        if(blnc[add] >= val){
            supply -=val;
            blnc[add] -= val;
        }
    }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile leb.sol" button.

Once the code is compiled, go to "Deploy and run transactions" then you will see the contract, just select the "leb.sol" then click the deploy button.

After deploy of the token, you will see now at the bottom part the "Deploy Contracts" click that. In above you will see the "Account Address" copy that then go again in Deploy Contracts where you will see the "burn" and "mint".

In inputing, click the dropdown button in burn then paste the Account Address then put the value you want to put in, after then click the "Transact" button and it will appear that you successfully burned token, same with mint.


## Authors

Alcantara, John Benedict G. 
2.1 Bsit


