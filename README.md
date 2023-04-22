# Smart Contract 
  On blockchain, the goal of a smart contract is to simplify business and trade between both anonymous and identified parties, sometimes without the need for a middleman. A smart contract scales down on formality and costs associated with traditional methods, without compromising on authenticity and credibility.
 
  
 ## Description 
  Smart contracts are code written into a blockchain that executes the terms of an agreement or contract from outside the chain. It automates the actions that would otherwise be completed by the parties in the agreement, which removes the need for both parties to trust each other.
 An in-depth paragraph about your project and overview of use. 
  
 ## Getting Started 
  
 ### Executing program 

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:
  
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    
string public TokenName = "Coin";
string public TokenAbbrv = "Eth";
uint public  TotalSupply = 0;

    mapping(address => uint) public balances;
     
    function mint (address _address, uint _value) public {
       TotalSupply += _value;
       balances[_address] += _value;
    }
    
    function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
          TotalSupply -= _value;
          balances[_address] -= _value;
       }
    }
}

  To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile SmartContract.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "SmartContract" from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the Mytoken function. Click on the "SmartContract"  in the left-hand sidebar, and then click on the "Mytoken" function. Finally, click on the "transact" button to execute the function and retrieve the Mytoken value.
 
  
 ## Author
 Chester Villardo 
 
  
 ## License 
  
 This project is licensed under the MIT  License - see the .README.mdfile for details
