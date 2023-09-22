## MetaCrafters - Solidity beginner [Token Creation]

Creating a solidity token named "Apple" and demonstrating minting and burning

## Description

This projects demonstrates how to create a token with unique name, its abbreviation and its total supply. Once a token has been created two functions named mint and burn to add or subtract values.

## Getting Started

### Installing

This program can be executed on https://remix.ethereum.org/ or an Offline ide

### Executing program

contract MyToken {
    // public variables here
    string public TokenName = "Apple";
    string public tokenAbbrev = "APL";
    uint public totalSupply = 300;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address mntaddress,uint mntvalue) public  {
        totalSupply += mntvalue;
        balances[mntaddress] += mntvalue;
    }
    
    // burn function
        function burn(address brnaddress,uint brnvalue) public  {
        if (balances[brnaddress] >= brnvalue) {
            totalSupply -= brnvalue;
            balances[brnaddress] -= brnvalue;
        }
        
    }
}

A token named "Apple" has been created with the abbreviation "APL". The total supply of this token is set to 300. We have two functions: function "mint" , to add value to the balance and to the total supply here the token "APPLE" and function "burn" this is used to subract values from the balance of the address as well the total supply of the token "APPLE". 
## Help

The variable totalsupply must be **uint** of postive value. 
In the burn function we must necessarily add a conditional statement to make sure the balance is **greater** than the burn value. 
## Authors

Bharath C
Email : bharathchandru5459@gmail.com



## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
