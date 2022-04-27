# Crypto ICO: Arcade (ARC) Token
Smart Contract for deploying a crypto ICO called Arcade

# CREATE TOKEN COIN
## Implementing a ERC20 compliant token 
● ERC20 interface for applications used by wallets, decentralized exchange and other tokens. 
● Implements 6functions and 2 events 

////ERC 20 interface //////
interface ERC20Interface {
    function totalSupply() external view returns (uint);
    function balanceOf(address tokenOwner) external view returns (uint balance);
    function transfer(address to, uint tokens) external returns (bool success);

    function allowance(address tokenOwner, address spender) external view returns (uint remaining);
    function approve(address spender, uint tokens) external returns (bool success);
    function transferFrom(address from, address to, uint tokens) external returns (bool success);

    event Transfer(address indexed from, address indexed to, uint tokens);
    event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
}
</br>

## Create the token constructor with name of coin and coin symbol.
 contract Arcade is ERC20Interface {
     string public name ="Arcade";
     string public symbol = "ARC";
     uint public decimals = 0; //18
     uint public override totalSupply;

 ....totalSupply = 1000000; //total supply of ARC in ecosystem is 1mil ARC available.

 ## Deploy to Rinkeby testnet through Remix EVM
 To deploy your custom COIN on Rinkeby, connect to your Metamask and head over to asset and import tokens. 
 
 ● Add the token address for ARC coin: 
0x6cc04a47dc035297188343e0dc4751905cd626b1 <br/>



# ICO - Initial Coin Offering
●1Eth = 1000 ARC </br>
● The ICO Hardcap is 300 ETH; </br>
● The ICO will have an admin that specifies when the ICO starts and ends; </br>
● The ICO ends when the Hardcap or the end time is reached (whichever comes first); </br>
● The ARC token will be tradable only after a specific time set by the admin; </br>

To deploy the ICO, use a primary wallet associated with admin/Founder, </br>
address of the ICO contract: </br>
0x6Cc04A47dC035297188343E0DC4751905cd626B1 </br>

When an investor invest 1 eth to the contract address, the investor will receive 1000 ARC tokens in return.
