# Chester-solidity-

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

