# Metacrafter_Solidity_ETH_ProofBeginner_FinalProjectAssesment

This Solidity program have simple contract which is for minting and burning token. The purpose of the program is to demonstrate the mechanism of minting , burning and supply of the tokens

# Description
It is a Solidity Smart Contract. There are 4 public State variables (Token Name, Token Abbrv., Total Supply and balances) of this contract. There is the mapping of senders to balances. Additionally, there are two functions: MintTokens & BurnTokens. MintTokens requires two parameter ( address and value). Again the value will not be added directly to minted token but mintedToken will be increased afterwards also increase the TotalSuppy and Balances of the sender by calling of MintToken. Next, BurnTokens which also mandatory needs two parameters (address and value) along with one conditional statement to check whether toknes to burn are exist in senders balance or not. If the condition is true then the value will get subtract from TotalSupply as well as in balance in address.

# Getting Started
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ETHProofBeginnerFinalProject.sol). Copy and paste the following code into the file:

----
    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.18;

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
    string public TokenName = "BitCoin";
    string public TokenAbbrv = "BTC";
    uint public TotalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function MintTokens(address _address, uint _value) public 
    {
        TotalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function BurnTokens(address _address, uint _value) public 
    {
        if  (balances[_address] >= _value) 
        {            
         TotalSupply -= _value;
         balances[_address] -= _value;  

        }
    }
    }
        /* 
        Few Addresses for Testing Purposes
        0x5B38Da6a701c568545dCfcB03FcB875f56beddC4
        0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2
        */
----
