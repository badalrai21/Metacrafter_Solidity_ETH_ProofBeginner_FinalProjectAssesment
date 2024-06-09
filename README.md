# Metacrafter_Solidity_ETH_ProofBeginner_FinalProjectAssesment

This Solidity program have simple contract which is for minting and burning token. The purpose of the program is to demonstrate the mechanism of minting , burning and supply of the tokens

# Description
It is a Solidity Smart Contract. There are 4 public State variables (Token Name, Token Abbrv., Total Supply and balances) of this contract. There is the mapping of senders to balances. Additionally, there are two functions: MintTokens & BurnTokens. MintTokens requires two parameter ( address and value). Again the value will not be added directly to minted token but mintedToken will be increased afterwards also increase the TotalSuppy and Balances of the sender by calling of MintToken. Next, BurnTokens which also mandatory needs two parameters (address and value) along with one conditional statement to check whether toknes to burn are exist in senders balance or not. If the condition is true then the value will get subtract from TotalSupply as well as in balance in address.
