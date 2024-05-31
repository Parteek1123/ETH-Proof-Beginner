Project


The MyToken smart contract is a basic implementation of an ERC-20 like token on the Ethereum blockchain. It allows for minting and burning of tokens, with public visibility of the token details such as name, abbreviation, and total supply. This contract is written in Solidity and compatible with the Ethereum Virtual Machine (EVM).

Getting Started


Executing Program


To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension . Copy and paste the following code into the file:

pragma solidity 0.8.25;
contract MyToken {
   // public variables here
    string public name="Token";
    string public abbrv="MTA";
    uint public totalsupply=0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint(address _add, uint _value) public {
      totalsupply+= _value;
    balances[_add] +=_value;
    }

    // burn function
    function burn(address _add, uint _value) public {
      if(balances[_add]>=_value) {
         totalsupply-= _value;
         balances[_add]-= _value;
      }
    }

}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile solidity.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "solidity.sol" contract from the dropdown menu, and then click on the "Deploy" button.
Enter the values of the function and call them respectively.

Author


Parteek
