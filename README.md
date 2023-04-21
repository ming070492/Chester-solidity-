# solidity 
 
  Solidity is a purposefully slimmed down, loosely-typed language with a syntax very similar to JavaScript. Solidity-coded smart contracts can be easily executed in the Ethereum Virtual Machine or the EVM.   
 
#Description 
  
 Ethereum is a decentralized blockchain platform that establishes a peer-to-peer network that securely executes and verifies application code, called smart contracts. Smart contracts allow participants to transact with each other without a trusted central authority.  
  
 ## Getting Started 
  
 ### Executing program 
  
 To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/. 
  
 Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file: 
  
 ```javascript 
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


  
 ``` 
  
 To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "myToken.sol" button. 
  
 Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Mytoken" contract from the dropdown menu, and then click on the "Deploy" button. 
  
 Once the contract is deployed, you can interact function. 
  
 ## Authors 
  
 Chester Villardo
  
  
 ## License 
  
 This project is licensed under the MIT License - see the LICENSE.md file for details
